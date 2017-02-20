# Using gdb

## Step 1

Build the code

`go build  -gcflags "-N -l" -o gdb_sandbox debug.go`

The code generated by the gc compiler includes inlining of function invocations and registerization of variables.

These optimizations can sometimes make debugging with gdb harder.

To disable them when debugging, pass the flags -gcflags "-N -l" to the go command used to build the code being debugged.

## Step 2

Start gdb `gdb gdb_sandbox`

## Step 3

define breakpoint `b day47/debug.go:6`

## Step 4

let's start debugging `run`

## Step 5

navigate through lines using `s` until line 11

tip: use `n` inside greet function

## Step 6

print variable `p greetingArg`

## Step 7

learn more comands typing help

## Step 8

type `q` to exit