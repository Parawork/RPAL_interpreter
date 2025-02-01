# RPAL Interpreter

This project is a Java-based interpreter for the RPAL (Right-reference Programming Algorithmic Language) language.

## Features

- **Lexical Analysis:** Tokenizes RPAL source code.
- **Parsing:** Builds a parse tree and an abstract syntax tree (AST).
- **AST Standardization:** Converts the AST to a standardized form.
- **Control Structure Generation:** Produces control structures for the CSE machine.
- **CSE Machine:** Evaluates the program using the Control-Stack-Environment model.
- **Built-in Functions:** Supports RPAL built-ins like `Print`, `Stem`, `Stern`, `Conc`, `Order`, etc.

## Project Structure

```
src/
  Lexar/           # Lexical analyzer and token classes
  Parser/          # Parser, AST, and parse tree classes
  CS/              # Control structure generation
  cse_machine/     # CSE machine and environment management
  tests/           # RPAL test programs
  Main.java        # Entry point
Makefile           # Build and test automation
README.md          # Project documentation
```

## Building

To compile the project, run:

```sh
cd src
make
```

Or, if you do not have a Makefile, compile manually:

```sh
javac Main.java
```

## Running

To interpret an RPAL program, use:

```sh
java Main <flags> <filename>
```

- `<flags>` are optional:
  - `-token` : Print token list
  - `-ast`   : Print abstract syntax tree
  - `-st`    : Print standardized tree

**Examples:**

Print the AST for a file:

```sh
java Main -ast tests/fn1
```

Print tokens and AST:

```sh
java Main -token -ast tests/fn1
```

**Note:**  
The filename (your RPAL source file) must be the last argument.  
Do not add extra arguments after the filename.

## Testing

To run all sample tests and compare outputs (if a Makefile is provided):

```sh
make test
```

## Example

Sample RPAL program (`tests/hello`):

```
Print ('hello')
```

Run it with:

```sh
java Main tests/hello
```

## Authors

Rathnayaka R.M.P.B.     220522A
Maddumage M.M.T.D.      220370E


## License

This project is for educational purposes.