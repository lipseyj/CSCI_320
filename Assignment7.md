#Assignment 7 Kotlin List Processing
1. Format
2. Parsing <br>
  a. <br>
     ident = [a-zA-Z]\w <br>
     value = [0-9]+?(.[0-9]*) <br><br>
  b. <br>
     fun fun_stmt(Token) <br>
        &emsp;if Token != "fun" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != ident raise error <br>
        &emsp;identity = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != block raise error <br>
        &emsp;Block = Token <br>
        &emsp;emit("Function", identity, Block) <br>
        <br>
     fun block(Token) <br>
        &emsp;if Token != "{" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != stmt raise error <br>
        &emsp;statement1 = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != "{" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != stmt raise error <br>
        &emsp;statement2 = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != "}" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != "}" raise error <br>
        &emsp;getToken() <br>
        &emsp;emit("Block", statment1, statment2) <br>
        <br>
     fun stmt(Token) <br>
        &emsp;if Token == assignment_stmt <br>
        &emsp;&emsp;Assignment = Token <br>
        &emsp;&emsp;emit("Assignment Statement", assignment_stmt) <br>
        &emsp;else if Token == if_stmt <br>
        &emsp;&emsp;if_stmt = Token <br>
        &emsp;&emsp;emit("If Statement", if_stmt) <br>
        <br>
     fun assignment_stmt(Token) <br>
        &emsp;if Token != ident raise error <br>
        &emsp;identity = ident <br>
        &emsp;getToken() <br>
        &emsp;if Token != "=" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != value raise error <br>
        &emsp;Value = value <br>
        &emsp;emit("Assignment Statement", identity, Value) <br>
        <br>
     fun if_stmt(Token) <br>
        &emsp;if Token != "if" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != "(" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != ident raise error <br>
        &emsp;identity = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != relop raise error <br>
        &emsp;Relop = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != value raise error <br>
        &emsp;Value = Token <br>
        &emsp;getToken() <br>
        &emsp;if Token != ")" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != block raise error <br>
        &emsp;Block1 = block <br>
        &emsp;&emsp;if peekToken.isEmpty() OR peekToken.isNull() <br>
        &emsp;emit("If Statement", identity, Relop, Value, Block1) <br>
        &emsp;getToken() <br>
        &emsp;if Token != "else" raise error <br>
        &emsp;getToken() <br>
        &emsp;if Token != block raise error <br>
        &emsp;Block2 = Token <br>
        &emsp;emit("If Statement", identity, Relop, Value, Block1, Block2) <br><br>
3. Information for program: <br>
       Use commas to separate String input without any spaces.
