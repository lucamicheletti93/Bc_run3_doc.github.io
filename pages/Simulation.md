## Simulation framework

In order to run a Bc simulation within the O2 framework is necessary to do the following steps:
- Clone https://github.com/mcoquet642/O2DPG/tree/Bc_fwd_simu
- Build the O2DPG with:
  ```ruby
  aliBuild build O2 QualityControl O2Physics O2DPG --defaults o2
  ```
- Build EVTGEN with:
  ```ruby
  aliBuild build EVTGEN --defaults o2
  ```
- Load the environment:
  ```ruby
  alienv enter O2/latest O2Physics/latest O2DPG/latest-Bc_fwd_simu-o2 EVTGEN/latest
  ```
- Open a ticket for the alien grid
- Run the simulation using the script
  ```ruby
  ./runBcToJpsi_fwdy_pp.sh
  ```
  
 If the procedure ends properly an AO2D.root file will be produced. If there is an error try to modify the last line of the script with:
 ```ruby
 ${O2DPG_ROOT}/MC/bin/o2_dpg_workflow_runner.py -f workflow.json -tt aod
 ```
