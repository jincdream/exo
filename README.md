<div align="center">

<picture>
  <source media="(prefers-color-scheme: light)" srcset="https://pbs.twimg.com/profile_images/1772318997569998848/si2_A2yj_400x400.jpg">
  <img alt="exo logo" src="https://pbs.twimg.com/profile_images/1772318997569998848/si2_A2yj_400x400.jpg" width="50%" height="50%">
</picture>

exo: Run your own AI cluster at home with everyday devices. Maintained by [exo labs](https://exolabs.net).

Supports iPhone, iPad, Android, Mac, Linux, pretty much any device!

<h3>

[Homepage](https://github.com/exo-explore/exo) | [Documentation](https://github.com/exo-explore/exo/docs) | [Discord](TODO)

</h3>

</div>


---

## Get Involved

We have a list of bounties in [this sheet](https://docs.google.com/spreadsheets/d/1cTCpTIp48UnnIvHeLEUNg1iMy_Q6lRybgECSFCoVJpE/edit?usp=sharing).

## Features

### Wide Model Support

exo supports LLaMA and many other popular models.

### Dynamic Model Partitioning

exo optimally splits up models based on the current network topology and device resources available.

### Automatic Device Discovery

Zero manual configuration. exo will automatically discover other devices using the best method available.

### ChatGPT-compatible API

exo provides a ChatGPT-compatible API for running models. This means it's a one-line change in your application to run models on exo.

## Inference Engines

exo supports the following inference engines:

- [x] [MLX](inference/mlx/sharded_inference_engine.py)
- [x] [tinygrad](inference/tinygrad/inference.py)

## Usage

## Documentation

### Example Usage on Multiple Devices

#### Device 1:

```sh
./run.sh
```

#### Device 2:
```sh
./run.sh
```

That's it! No configuration required - exo will automatically discover the other device(s).

A ChatGPT-like web interface will be available on each device on port 8000 http://localhost:8000.

An API endpoint will be available on port 8001. Example usage:

```sh
curl -X POST http://localhost:8001/api/v1/chat -H "Content-Type: application/json" -d '{"messages": [{"role": "user", "content": "What is the meaning of life?"}]}'
```
