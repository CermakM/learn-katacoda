Now that we have the **dependency manager** installed, let's use it!

Start the Jupyter Notebook:

``jupyter notebook example.ipynb``{{execute}}

You can now notice that the notebook uses some dependencies that might not be present in the Python environment (especially assuming that we're running in a clean one).

These are:
- matplotlib
- mpl_toolkits
- scipy

Let's see how we can deal with that. At the top of the Jupyter Notebook you should see a <i class="fas fa-thumbtack"></i> button.