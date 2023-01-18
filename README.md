# What is this?
This package is a one of a series packages intended to
support the development of general purpose chess engines and tools.

This package implements a [UCI](https://www.chessprogramming.org/UCI)
compatible _Random Engine_. A _Random Engine_ is a chess engine that
plays according to the following strategy: Every time it is asked to
play a move in a given position it generates the list of legal moves
and pick a random move from the list.

# What's the point of implementing this?

As you might imagine, this engine plays, really, really badly. So you might
as yourself why on Earth this was implemented in the first place. 
The reason is simple: When neural-net engines are trained from scratch they play
nearly randomly, and playing against this engine and assessing the win-rate
helps quantity how much the neural-net is learning.

# How do I build it?

This package uses CMake as a build-tool. In theory, it requires CMake 3.5,
but I haven't tested it with previous versions of CMake. If you manage to
build it with an older version of CMake, let me know or send a pull request
decreasing the required version on line 1 of `/CMakeLists.txt`

To build it:
```sh
mkdir build
cd build
cmake ..
make
```

# Testing
So far there are no tests implemented for this, as the implementation is trivial.
However, feel free to suggest (or send a pull request) any test cases that might
be interesting having.
