# Sound Analysis, Synthesis and Processing - Homework 4

This project is the implementation of Homework #4 from the *SSSP* course (*Wave Digital Filter Modeling*). The task is to design and implement a Wave Digital Filter (WDF) model of a three-way crossover network, starting from an analog reference circuit.

A three-way crossover network splits the input audio signal into three frequency bands to feed different loudspeaker drivers: low frequencies to the woofer, mid frequencies to the midrange, and high frequencies to the tweeter. In this homework, each driver is modeled as an 8 Ω resistor, and the analog circuit consists of low-pass, band-pass, and high-pass filter subcircuits.

The project involves:

* Designing a WDF representation of the crossover network that is **fully explicit** (no iterative solvers), including defining free parameters for reflection-free ports.
* Implementing the WDF in MATLAB using trapezoidal discretization (bilinear transform) for capacitors and inductors.
* Testing the implementation with an exponential sine sweep input (`ExpSweep.wav`) and comparing the outputs with ground-truth LTspice simulations (`outlowsweep.wav`, `outmidsweep.wav`, `outhighsweep.wav`).
* Plotting the error signals between the WDF outputs and the reference signals for different sampling frequencies (Fs = 192 kHz / 4, Fs = 192 kHz / 3, Fs = 192 kHz / 2).
* Providing answers to theoretical questions regarding accuracy, sampling rate effects, computability with nonlinear elements, and alternative discretization methods (e.g., Backward Euler for inductors).

> The WDF scheme are designed to minimize computational complexity while ensuring stability and explicit computability.

**Authors:** Chiara Lunghi, Alice Portentoso
