Switch over to the `Jupyter Notebook` tab, if everything has been deployed successfully, you should be redirected to the `example.ipynb` notebook.

> HINT: If the tab doesn't work, you can open up a new window manually and go to `echo $(oc get route notebook -o jsonpath='{@.spec.host}')`{{execute}} to access your notebook server. When in the notebook server, open the notebook stored at `katacoda-examples/jupyter-notebooks/example.ipynb`.

You can now notice that the notebook uses some dependencies that might not be present in the Python environment (especially assuming that we're running in a clean one).

These are:
- matplotlib
- mpl_toolkits
- scipy

> <i class="fas fa-exclamation"></i> Try executing the notebook cells. Does it fail?

Let's see how we can deal with that. At the top of the Jupyter Notebook you should see this button:

<center>
<img src="../../assets/jupyternotebooks/jupyter-notebooks-standalone-42/ui-logo.png" alt="Jupyter NBRequirements button" align="middle">
</center>

Click that button.

<center>
<img src="" alt="Jupyter NBRequirements widget" align="middle">
</center>

A widget unwraps, which states that there are currently no requirements specified for the notebook.