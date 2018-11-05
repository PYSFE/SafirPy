## RELEASE NOTE

### KNOWN ISSUES AND TASKS LIST

- [ ] Validation.
 
- [ ] Finalise README.md.

- [ ] SAFIR generates comeback file and triggers anti-virus software scan, potentially reduces CPU capacity. it is recommended to disable anti-virus software during simulation.

- [ ] General purpose bisection minimiser, i.e. able to define what parameter to change other than applied loading.

- [ ] Restructure the convergence function to a minimisation function.


### VERSIONS

**04/11/2018 VERSION: 0.0.3**

- New features:
    - Predefined Monte Carlo can be used when 'safirpy_mc_param.csv' file is available in path_work_root_dir folder. An example is provided in 'misc'.

- Feature improvements:
    - Added error handling at multiple locations, i.e. human-friendly error messages will be displayed when something goes wrong.

- Bug fixes:
    - ETA is disabled and replaced with time consumed as it did not work properly.

**22/10/2018 VERSION: 0.0.2**

- New features:

    - Monte Carlo tool can be executed by `python -m safirpy.mc` in a terminal or command line console
    
    - Simulation completion ETA is added.
    
    - All tested loads and time convergence values for individual Monte Carlo entry is recorded and saved as `pyout_seek_trail.txt`.

- Fixes:

    - Final applied load is optimised to take the load with time convergence closest to the defined target. Previously the final applied load was taken as the last calculated load and this is not always numerically correct and the second to last load can be more closer to the time convergence target.


**22/10/2018 VERSION: 0.0.1**

This initial release is pre-alpha stage and consists essential components to run Monte Carlo simulation using SAFIR.

- Pre-process:

    - Function to create random variables (for Monte Carlo simulation) subject to SAFIR problem definition

    - Function to read and parameterise SAFIR problem definition file so a specific variable of the input file can be modified (e.g. MC random variables)

    - Function to create a list of path strings with defined directory structure. This will be used to store SAFIR problem definition files for Monte Carlo simulation.

    - Function to write files (i.e. SAFIR problem definition file) into the previously created folders.

- SAFIR-process:

    - Function to handle SAFIR
    
    - Function to seek time of convergence by modifying load
    
    - Function to call the seeking routine with multiprocessing
    
- Post-process:
  
    - Save sought loading (to a specified time convergence) to a .csv file.
    
- Host routine, i.e. application routine to combine all functions