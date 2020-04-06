Let's first run the Jupyter Notebook server using our [s2i-minimal-notebook](https://github.com/thoth-station/s2i-minimal-notebook) image stored on [Quay.io](https://quay.io/).

To import the image to OpenShift, issue:

``oc import-image quay.io/thoth-station/s2i-minimal-notebook s2i-minimal-notebook --confirm``{{execute}}

This image contains built-in extensions which may come in useful for this scenario, in particular `Jupyter NBRequirements`.

Now, as learnt in the prerequisite courses, we will deploy that notebook image using a slightly modified `notebook-deployer` template which is for convenience already stored in the root folder.

To create that template:

``oc create -f notebook-deployer.json``{{execute}}

And to finally serve the notebook:

```
oc process notebook-deployer                                        \
    -p APPLICATION_NAME=notebook                                    \
    -p PRELOAD_REPOS="https://github.com/CermakM/katacoda-examples" \
    -p NOTEBOOK_PASSWORD="developer"                                \
    | oc apply -f -
```{{execute}}

Notice the `PRELOAD_REPOS` parameter, which allows us to populate our repository on notebook server startup with a custom Git Hub repository.

<br>

Now you can switch to the OpenShift console to see whether the notebook has been deployed correctly.

For the credentials, enter:

* **Username:** ``developer``{{copy}}
* **Password:** ``developer``{{copy}}

There should be an application with the Jupyter Notebook server running called `notebook`.