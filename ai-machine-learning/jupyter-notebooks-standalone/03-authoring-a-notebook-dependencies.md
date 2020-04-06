Now that we have the **dependency manager** installed, let's use it!

Switch over to the `Jupyter Notebook` tab and open a Jupyter Notebook called `example.ipynb`.

You can now notice that the notebook uses some dependencies that might not be present in the Python environment (especially assuming that we're running in a clean one).

These are:
- matplotlib
- mpl_toolkits
- scipy

Let's see how we can deal with that. At the top of the Jupyter Notebook you should see this button:

<center>
<img src="../../assets/jupyternotebooks/jupyter-notebooks-standalone-42/ui-logo.png" alt="Jupyter NBRequirements button" align="middle">
</center>