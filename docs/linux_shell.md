## Shell

[Batsh - A language that compiles to Bash and Windows Batch](http://batsh.org/)

### Expression

<div class="row" markdown="span">
<div markdown="span" class="col-xs-6">


```
# Pseudo Code
a = 1;
b = "string";
c = [1, 2, "str", true, false];
a = 1 + 2
b = a * 7
c = "Con" ++ "cat";
d = c ++ b
```

</div>

<div markdown="span" class="col-xs-6">

```sh
# Bash
a=$((1))
b="string"
c=($((1)) $((2)) "str" $((1)) $((0)))
a=$((1 + 2))
b=$(($a * 7))
c="Con""cat"
d="$c""$b"
```

</div>
</div> <!-- end row -->

### Command


<div class="row" markdown="span">
<div markdown="span" class="col-xs-6">


```
# Pseudo Code
println("Hello world");
print("Hello");
println(" world");

java = "/usr/bin/java";
call(java, "-jar", "closure.jar");
```

</div>

<div markdown="span" class="col-xs-6">

```sh
# Bash
"echo" "-e" "Hello world"
"echo" "-ne" "Hello"
"echo" "-e" " world"

java="/usr/bin/java"
"$java" "-jar" "closure.jar"
```

</div>
</div> <!-- end row -->

### Condition


<div class="row" markdown="span">
<div markdown="span" class="col-xs-6">


```
# Pseudo Code
a = 3;
if (a > 2) {
  println("Yes");
} else {
  println("No");
}
```

```
# else if
a = 10;
if (a > 7) {
  println("Big");
} else if (a > 4) {
  println("Medium");
} else {
  println("Small");
}
```

</div>

<div markdown="span" class="col-xs-6">

```sh
# Bash
a=$((3))
if [ $(($a > 2)) == 1 ]; then
  "echo" "-e" "Yes"
else
  "echo" "-e" "No"
fi
```

```
# elif
a=5
if [ "$a" -gt 7 ]; then
  echo "Big"
elif [ "$a" -gt 4 ]; then
  echo "Medium"
else
  echo "Small"
fi
```

</div>
</div> <!-- end row -->

### Loop


<div class="row" markdown="span">
<div markdown="span" class="col-xs-6">


```
# Pseudo Code: Fibonacci
n = 0;
i = 0;
j = 1;
while (n < 60) {
  k = i + j;
  i = j;
  j = k;
  n = n + 1;
  echo(k);
}
```

</div>

<div markdown="span" class="col-xs-6">

```sh
# Bash: Fibonacci
n=0
i=0
j=1
while [ "$n" -lt 60 ]; do
  k=$(($i + $j))
  i="$j"
  j="$k"
  n=$(($n + 1))
  "echo" "$k"
done
```

</div>
</div> <!-- end row -->

### Arguments

```sh
$ cat myscript
#!/bin/bash
echo "First arg: $1"
echo "Second arg: $2"

$ ./myscript hello world
First arg: hello
Second arg: world
```
