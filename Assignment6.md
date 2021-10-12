1. Format
2. Syntax Processing <br><br>
  a. kotlinc d hello.jar hello.kt && java jar hello.jar <br><br>
    commandline <br>
  (1) list <br>
  (2) conditional <br>
  (3) conditional && pipeline <br>
  (3) pipeline && pipeline <br>
  (4) command && pipeline <br>
  (5) command word && pipeline <br>
  (5) command word word && pipeline <br>
  (5) command word word word && pipeline <br>
    kotlinc word word word && pipeline <br>
    kotlinc d word word && pipeline <br>
    kotlinc d hello.jar word && pipeline <br>
    kotlinc d hello.jar hello.kt && pipeline <br>
  (4) kotlinc d hello.jar hello.kt && command <br>
  (5) kotlinc d hello.jar hello.kt && command word <br>
  (5) kotlinc d hello.jar hello.kt && command word word <br>
    kotlinc d hello.jar hello.kt && java word word <br>
    kotlinc d hello.jar hello.kt && java jar word <br>
    kotlinc d hello.jar hello.kt && java jar hello.jar <br><br>
  b. find name something | grep hello 2> somefile
    commandline
  (1) list <br>
  (2) conditional <br>
  (3) pipeline <br>
  (4) pipeline | command <br>
  (4) command | command <br>
  (5) command word | command <br>
  (5) command word word | command <br>
    find word word | command <br>
    find name word | command <br>
    find name something | command <br>
  (5) find name something | command redirection <br>
  (5) find name something | command word redirection <br>
  (6) find name something | command word redirectionop filename <br>
    find name something | grep word redirectionop filename <br>
    find name something | grep hello redirectionop filename <br>
  (7) find name something | grep hello 2> filename <br>
    find name something | grep hello 2> somefile
