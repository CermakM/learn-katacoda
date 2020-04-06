Switch over to the a new tab, if everything has been deployed successfully and open the following URL:

[notebook-myproject.[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com](https://notebook-myproject.[[HOST_SUBDOMAIN]]-80-[[KATACODA_HOST]].environments.katacoda.com)

> HINT: If the tab doesn't work, you can open up a new window manually and go to `echo $(oc get route notebook -o jsonpath='{@.spec.host}')`{{execute}} to access your notebook server.

When in the notebook server, open the notebook stored at `katacoda-examples/jupyter-notebooks/example.ipynb`.

You can now notice that the notebook uses some dependencies that might not be present in the Python environment (especially assuming that we're running in a clean one).

These are:
- matplotlib
- mpl_toolkits
- scipy

<i class="fas fa-exclamation"></i> Try executing the notebook cells. Does it fail?

Let's see how we can deal with that.