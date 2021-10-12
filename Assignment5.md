# Assignment 5 Tokenization
1. Format
2. Regular Expressions <br>
  a. [a-z][a-z0-9]* <br>
  b. [0-9]*\\\\.[0-9] <br>
3. Backus-Naur form <br>
  a. cat myfile && cat yourfile <br><br>
    commandline <br>
    list (1) <br>
    conditional (2) <br>
    conditional && pipeline (3) <br>
    pipeline && pipeline (3) <br>
    command && pipeline (4) <br>
    command word && pipeline (5) <br>
    cat word && pipeline <br>
    cat myfile && pipeline <br>
    cat myfile && command (4) <br>
    cat myfile && command word (5) <br>
    cat myfile && cat word <br>
    cat myfile && cat yourfile <br><br>
  b. ls | grep something > somefile <br><br>
    commandline <br>
    list (1) <br>
    conditional (2) <br>
    pipeline (3) <br>
    pipeline | command (3) <br>
    command | command (5) <br>
    ls | command <br>
    ls | command redirection (5) <br>
    ls | command word redirection (5) <br>
    ls | grep word redirection <br>
    ls | grep something redirection <br>
    ls | grep something redirectionop filename (6) <br>
    ls | grep something > filename (7) <br>
    ls | grep something > somefile <br><br>
  c. somecmd someparm || othercmd; gcc myfile > output <br><br>
    commandline <br>
    list; (1) <br>
    list; conditional (2) <br>
    conditional; conditional (2) <br>
    conditional || pipeline; conditional (3) <br>
    pipeline || pipeline; conditional (3) <br>
    command || pipeline; conditional (4) <br>
    command word || pipeline; conditional (5) <br>
    somecd word || pipeline; conditional <br>
    somecd someparm || pipeline; conditional <br>
    somecd someparm || command; conditional (4) <br>
    somecd someparm || othercmd; conditional <br>
    somecd someparm || othercmd; pipeline (3) <br>
    somecd someparm || othercmd; command (4) <br>
    somecd someparm || othercmd; command redirection (5) <br>
    somecd someparm || othercmd; command word redirection (5) <br>
    somecd someparm || othercmd; command word redirectionop filename (6) <br>
    somecd someparm || othercmd; gcc word redirectionop filename <br>
    somecd someparm || othercmd; gcc myfile redirectionop filename <br>
    somecd someparm || othercmd; gcc myfile > filename (7) <br>
    somecd someparm || othercmd; gcc myfile > output <br><br>
  d. cmd1; cmd2 && cmd3; less output <br><br>
    commandline commandline <br>
    list; commandline (1) <br>
    conditional; commandline (2) <br>
    pipeline; commandline (3) <br>
    command; commandline (4) <br>
    cmd1; commandline <br>
    cmd1; list; (1) <br>
    cmd1; list; conditional (2) <br>
    cmd1; conditional; conditional (2) <br>
    cmd1; conditional && pipeline; conditional (3) <br>
    cmd1; pipeline && pipeline; conditional (3) <br>
    cmd1; command && pipeline; conditional (4) <br>
    cmd1; cmd2 && pipeline; conditional <br>
    cmd1; cmd2 && command; conditional (4) <br>
    cmd1; cmd2 && cmd3; conditional <br>
    cmd1; cmd2 && cmd3; pipeline (3) <br>
    cmd1; cmd2 && cmd3; command (4) <br>
    cmd1; cmd2 && cmd3; command word (5) <br>
    cmd1; cmd2 && cmd3; less word <br>
    cmd1; cmd2 && cmd3; less output
