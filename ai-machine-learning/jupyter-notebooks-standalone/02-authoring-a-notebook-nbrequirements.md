Let's first run the Jupyter Notebook server using our [s2i-minimal-notebook](https://github.com/thoth-station/s2i-minimal-notebook) image stored on [Quay.io](https://quay.io/).

``docker run -p 8888:8888 -d –name jupyter-notebook quay.io/thoth-station/s2i-minimal-notebook``{{execute}}

This image contains built-in extensions which may come in useful for this scenario, in particular `Jupyter NBRequirements`.

### Jupyter NBRequirements

This extension is a Jupyter Notebook dependency manager which provides control over the notebook dependencies.

The main goals of the project are the following:

- To create a notebook with its requirements embedded within it without leaving the notebook
- To provide a unique and optimized<sup>*</sup> environment for each notebook
- To allow for easy sharing, deployment and execution of Jupyter notebooks

<sup>*</sup>The requirements are optimized using the Thoth resolution engine

Let's install the extension by issuing:

``pip install jupyter-nbrequirements``{{execute}}
