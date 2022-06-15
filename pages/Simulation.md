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
 
# Run simulation on LXPLUS
In afs configure the environment to run the Bc script:
  ```ruby
  /cvmfs/alice.cern.ch/bin/alienv enter VO_ALICE@O2Physics::nightly-20220615-1
  ```
  ```ruby
  module load EVTGEN
  ```
  ```ruby
  export O2DPG_ROOT=/afs/cern.ch/work/l/lmichele/alice/O2DPG
  ```
  create a ticket for the grid
 
## Fast simulation with RapidSim and BDT

- Fast simulation tool (modified particle-gun generato for LHCb, adapted to ALICE run3) : https://github.com/mcoquet642/RapidSim/tree/clean_aliceRun3
- XGboost, Boosted Decision tree : https://github.com/mcoquet642/bdt-tutorial/tree/b_c
- Some simple macros to reproduce a background mix : https://github.com/mcoquet642/Bc_Bkg_mix.git
