# Interactive Parallel Computing with IPython

ipyparallel is the new home of IPython.parallel.

To install the `Clusters` tab in Jupyter Notebook, add this to your `jupyter_notebook_config.py`:

```python
c.NotebookApp.server_extensions.append('ipyparallel.nbextension')
```

Current development is adding support for SLURM launchers when starting clusters.
