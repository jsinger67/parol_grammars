# parol_grammars

A collection of working grammars ready to use for the `parol` parser generator

## Set up `parol`

For instructions on how to setup `parol` please have a look at
[the book](https://jsinger67.github.io/) or [the video](https://youtu.be/TJMwMqD4XSo).

## How to test

The easiest way to test one of the given grammars is to let parol generate a project for you

```shell
parol new --bin --path <grammar_name>
```

In the command above please replace the <grammar_name> with the basename of the grammar file you're
about to inspect, e.g. if you want to test the regex grammar from `rx.par` use the following
concrete command:

```shell
parol new --bin --path rx
```

Then enter the newly created folder `rx` and overwrite the existing `rx.par` by the one from this
repository.

Having this done you are ready to compile the crate

```shell
cargo build
```

After this please modify the `test.txt` file with content that should be parsed, e.g.

```
(a|b)*abb
```

and call the parser:

```shell
cargo run test.txt
```

## Contributions

Any contributions are welcome. Simply fork the project, add your contributions and create a pull
request.

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in the
work by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any
additional terms or conditions.
