# log

being a logging facade inspired by Rust’s [log crate](https://github.com/rust-lang-nursery/log/).

It is a simple abstraction that enables you to use the same logging functions,
no matter what backend you use. You can use this abstraction to switch out your
logging implementation without stress.

## Usage

There are multiple functions for you to use, depending on how important the
message is:

```clojure
(load "git@github.com:carpentry-org/log@0.0.9")

(defn main []
  (do
    (Log.trace "And now for our main event...")

    (while true
      (if (Bool.random)
        (Log.info "Heads!")
        (Log.warn "Tails!"))))
)
```

The complete set of functions, in order of severity, is:
- `trace`
- `debug`
- `info`
- `warn`
- `error`

## Backends

A non-exhaustive list of logging backends:

- [`simplelog`](https://github.com/carpentry-org/simplelog): A simple logger
  that prints either to `stdout` or `stderror`, depending on the log level.

<hr/>

Have fun!
