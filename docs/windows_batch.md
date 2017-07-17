# Windows Batch

[Batsh - A language that compiles to Bash and Windows Batch](http://batsh.org/)

### Print

```
# print HELLO WORLD
echo HELLO WORLD

# print blank line
echo.
```

### Arguments [^3]

```powershell
echo %1
```

> $ test.bat helloworld
> helloworld

### Sleep

Sleep for 5 seconds [^1]

```powershell
timeout 5 > NUL

# deprecated
ping 127.0.0.1 -n 6 > nul
```

### Conditional [^4]

```powershell
if exist input.dat goto handle_input_file
    echo The file input.dat does not exist
    pause
    exit /b
:handle_input_file
```

### Loop [^2]

```
:while1
echo forever loop
goto :while1
```

> $ test.bat
> forever loop
> forever loop
> forever loop
> ...


[^1]: [How to sleep for 5 seconds in Windows's Command Prompt? (or DOS)](http://stackoverflow.com/questions/1672338/how-to-sleep-for-5-seconds-in-windowss-command-prompt-or-dos)
[^2]: [While loop in batch](http://stackoverflow.com/questions/1788473/while-loop-in-batch)
[^3]: [Command line parameters](http://www.robvanderwoude.com/parameters.php)
[^4]: [Windows Batch Files for Fun and Profit](http://www.quepublishing.com/articles/article.aspx?p=1154761&seqNum=7)

