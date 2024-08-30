# JSON parser

This is a very small-ish example of a relatively simple JSON parser that parses a given json input.
Currently tested on a M3 Macbook Air, it parses a 25MB large json file in ~0.3 seconds on repeat 
benchmarks (maybe because of hot fs, haven't benchmarked that aspect yet).

Not for production use.
Implemented:
- Custom lexer
- Custom recursive-descent parser with some lookahead (to prevent left-recursion, the parser looks
ahead on a token to determine what the next output should be)

If you look at the commit history, you'll find all sorts of wacky stuff - from a LISP repl calculator, 
to a small implementation of a PL I was working on -- grammar using the Chumsky crate in Rust. However,
the focus on that project has since moved to the [Datamod](https://github.com/sandeshbhusal/datamod) project;
I am not sure if Datamod is going to implement a DSL or run a embedded WASM subsystem, but my focus
has since shifted on this project to just implement a JSON parser to see if I could.

Enjoy!
