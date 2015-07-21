# Installation notes

1. Make sure IPython is installed
2. Do normal `pip install -e .`
3. Create an ipython profile with `ipython profile create --parallel --profile=slurm`
4. Edit the configuration files in ~/.ipython/profile_slurm
  * in ipcluster_config.py add the following lines
    * ```c = get_config()
	 c.IPClusterStart.controller_launcher_class = 'SLURMControllerLauncher'
	 c.IPClusterEngines.engine_launcher_class = 'SLURMEngineSetLauncher'
      ```
  * in ipcontroller_config.py add the following lines
    * ```c = get_config()
	 c.HubFactory.ip = '*'
	 c.HubFactory.engine_ip = '*'
	 c.HubFactory.client_ip = '*'
      ```
  * in ipython_config.py add `c = get_config()`


