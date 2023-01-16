load("@rules_rust//rust:defs.bzl", "rust_library")

genrule(
    name = "gen",
    cmd = "echo 'pub fn hello() { println!(\"Hello, world!\"); }' > $(@D)/gen.rs",
    outs = ["src/gen.rs"]
)

rust_library(
    name = "lib-with-gen",
    srcs = ["src/lib.rs", ":gen"],
)
