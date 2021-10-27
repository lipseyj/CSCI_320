#Assignment 7 Kotlin List Processing
1. Format
2. Parsing <br><br>
  a. <fun> ::= "fun" <ident> block <br>
     <fun> = <br><br>
     <block> ::= "{" <stmt> { <stmt> } "}" <br>
     <block> = "{" <stmt> { <stmt> } "}" <br><br>
     <stmt> ::= <assignment_stmt> | <if_stmt> <br>
     <stmt> = <assignment_stmt> | <if_stmt> <br><br>
     <assignment_stmt> ::= <ident> = <value> <br>
     <assignment_stmt> = [a-zA-Z]\w = [0-9]+(.[0-9])? <br><br>
     <if_stmt> ::= "if" ( <ident> <relop> <value> ) <block> [ else <block> ] <br>
     <if_stmt> = "if" ( <ident> <relop> <value> ) <block> [ else <block> ] <br><br>
3. Information for program: <br>
       Use commas to separate String input without any spaces.
