Rust-natord
===========

Natural ordering for Rust. This allows for the comparison like this:

~~~~ {.rust}
let mut files = vec!("rfc2086.txt", "rfc822.txt", "rfc1.txt");
files.sort_by(|&a, &b| natord::compare(a, b));
assert_eq!(files.as_slice(), ["rfc1.txt", "rfc822.txt", "rfc2086.txt"].as_slice());
~~~~

There are multiple natural ordering algorithms available.
This version of natural ordering is inspired by
[Martin Pool's `strnatcmp.c`](http://sourcefrog.net/projects/natsort/).

