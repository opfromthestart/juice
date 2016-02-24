# [Leaf](https://github.com/autumnai/leaf) Examples

CLI for running [leaf](https://github.com/autumnai/leaf) examples. More examples and benchmark tests can be found at the [leaf examples directory](https://github.com/autumnai/leaf#examples).

## Install CLI

Compile and call the build.
```bash
# install rust, if you need to
curl -sSf https://static.rust-lang.org/rustup.sh | sh
# download the code
git clone git@github.com:autumnai/leaf-examples.git && cd leaf-examples
# build the binary
cargo build --release
# and you should see the CLI help page
target/release/leaf-examples --help
# which means, you can run the examples from below
```

## MNIST

The MNIST Datasets comes not shipped with this repository (it's too big), but you can load it directly via the
CLI.

```bash
# download the MNIST dataset.
target/release/leaf-examples load-dataset mnist

# run the MNIST linear example
target/release/leaf-examples mnist linear --batch-size 10
# run the MNIST MLP (Multilayer Perceptron) example
target/release/leaf-examples mnist mlp --batch-size 5 --learning-rate 0.001
# run the MNIST Convolutional Neural Network example
target/release/leaf-examples mnist conv --batch-size 10 --learning-rate 0.002
```
