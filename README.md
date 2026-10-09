# LIF Neuron Playground

An interactive, browser-based simulator of a **leaky integrate-and-fire (LIF) neuron**, the basic building block of spiking neural networks and neuromorphic computing.

**Live demo:** https://spiyk.github.io/lif-neuron-playground/

The simulator needs no installation, build step or account. It runs in any modern browser, including on older laptops and phones.

## Features

- Sliders for input current, leak (β) and firing threshold
- Live plot of the membrane potential, threshold and spikes
- Pause, reset and temporary input cut-off controls
- Short explanation of the model alongside the simulation
- Light and dark theme, following the system setting

## Model

At each time step the neuron integrates its input, applies a leak, and fires when the threshold is reached:

```js
v = beta * v + input;
if (v >= threshold) {
  spike = true;
  v = 0;
}
```

This is a simplified, discrete-time form of the LIF model used in libraries such as snnTorch, Brian2 and Nengo. It is intended for learning and is not a replacement for research-grade simulators.

## Getting started

1. Clone or download this repository.
2. Open `index.html` in a web browser.

No dependencies are required.

## Roadmap

- [ ] Small network (20 to 100 neurons) with raster plot and spike-rate graph
- [ ] Optional 8-bit fixed-point mode to demonstrate quantization effects
- [ ] Refractory period option
- [ ] Output cross-check against snnTorch
- [ ] Translations (Bengali, Hindi and others)

## Contributing

Contributions are welcome, including bug reports, wording fixes, translations, accessibility improvements and new example presets. Please open an issue to discuss larger changes before submitting a pull request.

## Acknowledgements

Developed with the help of AI tools.

## License

Released under the [MIT License](LICENSE).

