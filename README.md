# simpleflake-rs

Forked from the archived repository [michaelcontento/simpleflake-rs][org-repo].

[![Build Status](https://secure.travis-ci.org/michaelcontento/simpleflake-rs.png?branch=master)](http://travis-ci.org/michaelcontento/simpleflake-rs) [![](https://meritbadge.herokuapp.com/simpleflake)](https://crates.io/crates/simpleflake)

Distributed ID generation in rust for the lazy. Based on the [python implementation][simpleflake-py] from [SawdustSoftware][].

# Installation

Just add this crate as a dependency to your `Cargo.toml`:

```ini
[dependencies.simpleflake]
git = "https://github.com/michaelcontento/simpleflake-rs.git"
```

# Usage

```rust
extern crate simpleflake;

let new_id = simpleflake::new();
println!("generated id: {}", new_id);

let parts = simpleflake::parse(new_id);
println!("timestamp: {}", parts.timestamp);
println!("random bits: {}", parts.random_bits);
```

[org-repo]: https://github.com/michaelcontento/simpleflake-rs
[simpleflake-py]: https://github.com/SawdustSoftware/simpleflake

