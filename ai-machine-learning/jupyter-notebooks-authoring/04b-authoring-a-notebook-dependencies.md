At the top of the Jupyter Notebook you should see this button:

<center>
<img src="../../assets/jupyternotebooks/jupyter-notebooks-authoring-42/nbrequirements-ui-logo.png" alt="Jupyter NBRequirements button" align="middle">
<figcaption><small>Jupyter NBRequirements button</small></figcaption>
</center>

Click that button.

<center>
<img src="../../assets/jupyternotebooks/jupyter-notebooks-authoring-42/nbrequirements-ui-unwrapped.png" alt="Jupyter NBRequirements widget" align="middle">
<figcaption><small>Jupyter NBRequirements widget</small></figcaption>
</center>

A widget unwraps, which states that there are currently no requirements specified for the notebook.

Click on `Detect` to automatically detect notebook dependencies and then click `Save`.

<i class="fas fa-exclamation"></i> Check that the dependencies have been saved successfully:

    oc exec \
        $( oc get pod -l app=notebook -o name | sed -e 's/pod\///' )  \
        cat katacoda-examples/jupyter-notebooks/example.ipynb       \
    | jq -c '.metadata.requirements'