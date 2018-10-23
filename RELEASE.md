## RELEASE NOTE

### KNOWN ISSUES AND TASKS LIST

 - [ ] Validation to the app.
 
 - [ ] Finalise README.md.

- SAFIR generates comeback file will trigger anti-virus software scan, potentially reduces CPU capacity

### VERSIONS

**22/10/2018 VERSION: 0.0.2**

- Added feature to enable executing the Monte Carlo simulation from `python -m safirpy.mc` in a terminal or command line console.

**22/10/2018 VERSION: 0.0.1**

This is a pre-alpha release.

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