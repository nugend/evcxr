# Evcxr library

An implementation of eval() for Rust.

The main struct in this crate is ```EvalContext```. You create one, then ask it
to eval bits of code. Any defined functions, variables etc are local to that
context.

```rust
let mut context = EvalContext::new();
context.eval("let s = String::new();")?;
context.eval("s.push_str(\"Hello \");")?;
context.eval("s.push_str(\" World\");")?;
context.eval("println!(\"{}\", s);")?;
```

I'll not go into too much detail here, since the purpose of this library is
really to provide functionality to evcxr\_jupyter and evcxr\_repl. If you'd like
to try using this crate for something else, drop me an email, or file an issue
on the repository and we can figure out your use case.

## How it works

See [how it works](HOW_IT_WORKS.md)
