# Jupyter CadQuery for Binder

A MyBinder.org configuration of jupyter-cadquery that provides an interactive environment for creating 3D CAD models using Python
using the CadQuery library and the excellent Jupyter CadQuery extension by bernhard-42.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/kws/jupyter-cadquery/HEAD?urlpath=lab/tree/example.ipynb)

## What is this?

This repository provides a ready-to-use Jupyter environment with CadQuery and Jupyter CadQuery pre-installed. It's perfect for:
- Learning 3D CAD modeling with Python
- Creating parametric designs
- Visualizing 3D models interactively
- Exporting models for 3D printing

## Getting Started

1. Click the "launch binder" badge above to start the interactive environment
2. Open `example.ipynb` to see a working example of a parametric box
3. Modify the parameters and re-run cells to see how the design changes
4. Export your models as STL files for 3D printing

## Local Development

You can also run this environment locally using [jupyter-repo2docker](https://repo2docker.readthedocs.io/). This is useful for:
- Offline development
- Customizing the environment
- Creating your own Docker images

To build and run locally:

```bash
# Install repo2docker
pip install jupyter-repo2docker

# Build and run the container
jupyter-repo2docker .
```

The container will be built using the `environment.yml` and `apt.txt` files, and Jupyter Lab will be available at `http://localhost:8888`.

## Learning Resources

- [CadQuery Documentation](https://cadquery.readthedocs.io/en/latest/) - Official documentation
- [Jupyter CadQuery GitHub](https://github.com/bernhard-42/jupyter-cadquery) - Jupyter integration details
- [Jupyter Lab Quickstart](https://justinbois.github.io/bootcamp/2020_fsri/lessons/l01_welcome.html#Launching-a-Jupyter-notebook) - Learn how to use Jupyter Lab

## Technical Details

### Environment Configuration

The environment is configured using two files:

1. `environment.yml` - Conda environment specification:
   - Python 3.10
   - CadQuery 2.2
   - Jupyter CadQuery 3.5.2
   - Additional packages:
     - cadquery-massembly 1.0.0
     - cq_warehouse (from GitHub)
     - cq_gears (from GitHub)

2. `apt.txt` - System dependencies:
   - libgl1 - Required for 3D visualization

### Included Packages

- **cadquery**: Core CAD modeling library - https://cadquery.readthedocs.io/en/latest/
- **jupyter-cadquery**: Jupyter integration for CadQuery - https://github.com/bernhard-42/jupyter-cadquery
- **cadquery-massembly**: Assembly support for CadQuery - https://github.com/bernhard-42/cadquery-massembly
- **cq_warehouse**: Collection of useful CadQuery parts and utilities - https://github.com/gumyr/cq_warehouse
- **cq_gears**: Gear generation utilities for CadQuery - https://github.com/meadiode/cq_gears

## Contributing

Feel free to:
- Submit issues for bugs or feature requests
- Fork the repository and make improvements
- Share your CadQuery designs and examples

## License

This project is open source and available under the MIT License.
