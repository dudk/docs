# Pipe

`pipe` is a framework for floating point signal processing. It utilizes [pipeline](https://blog.golang.org/pipelines) pattern to build fast, asynchronomous and easy-to-extend pipes for signal processing. Each pipe consists of one Pump, zero or multiple Processors and one or more Sinks. `pipe` also offers a friendly API for new pipe components implementations.

![diagram](https://dudk.github.io/post/lets-go/pipe_diagram.png)

## Getting started

The concept is explained in details in [this article on Medium](https://medium.com/@serg.dudk/lets-go-7f51fbde36e4).

Find examples in [example](https://github.com/pipelined/example) repository. For better explanations check its [godoc](https://godoc.org/github.com/pipelined/example).

## Implemented packages

Please, note that since `pipe` is in the active development stage, all packages are in experimental state. One of the main focus points is the stability of all listed and future packages. 

1. `pipelined/audio` - higher-level to manipulate audio signal. Allows to sample and compose tracks.
2. `pipelined/mixer` - mix from to 2 up to N signals with same number of channels and sample rates.
3. `pipelined/mock` - mock pipe components to create integration tests.
4. `pipelined/mp3` - read/write mp3 files.
5. `pipelined/pipe` - `pipe` framework.
6. `pipelined/portaudio` - play signal via [portaudio](http://www.portaudio.com/) API.
7. `pipelined/signal` - manipulate signal on lower level. Allows to convert float/int with different bit depth.
8. `pipelined/vst2` - process signal with vst2 plugins.
9.  `pipelined/wav` - read/write wav files.

## Dependencies

`phono/vst2` and `portaudio` packages do have external non-go dependencies. To use these packages, please check the documentation:

* [vst2](https://github.com/pipelined/vst2#dependencies)
* [portaudio](https://github.com/gordonklaus/portaudio#portaudio)

## Contributing

For a complete guide to contributing to `pipe`, see the [Contribution giude](https://github.com/pipelined/pipe/blob/master/CONTRIBUTING.md)
