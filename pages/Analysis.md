## List of commands to run (outdated)
- Load the environment on LXPLUS:
  ```ruby
  /cvmfs/alice.cern.ch/bin/alienv enter VO_ALICE@O2Physics::nightly-20220422-1
  ```
- Run TableMaker:
  ```ruby
  python runTableMaker.py configTableMakerMCRun3.json runMC table-maker-m-c:processMuonOnlyWithCov:true
  ```
- Run TableMaker with mcParticle converter (if the first command does not work):
  ```ruby
  python runTableMaker2.py configTableMakerMCRun3.json runMCwithConverter table-maker-m-c:processMuonOnlyWithCov:true
  ```
- Run TableMaker with fdd converter:
  ```ruby
  python runTableMaker_fddconverter.py configTableMakerMCRun3.json runMC table-maker-m-c:processMuonOnlyWithCov:true
  ```

## List of commands to run (updated)
In case of missing tables add the following arguments
1. --add_mc_conv: o2mcparticle -> o2mcparticle_001
2. --add_fdd_conv: o2fdd -> o2fdd_001
3. --add_track_prop: o2track -> o2track_iu ([link](https://aliceo2group.github.io/analysis-framework/docs/helperTasks/trackPropagation.html))

### TableMaker
- Run TableMaker on data/AO2D_Bc100.root
  ```ruby
  python runTableMaker.py config/configTableMakerMCRun3.json -runMC table-maker-m-c:processMuonOnlyWithCov:true
  ```
- Run TableMaker on data/AO2D_NonPromptJpsi.root
  ```ruby
  python runTableMaker.py config/configTableMakerMCRun3_NonPromptJpsi.json -runMC table-maker-m-c:processMuonOnlyWithCov:true --add_track_prop
  ```

### TableReader
- Run TableReader with dilepton-track tables saved:
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json --aod-writer-json writerConfiguration_dileptons_track.json -b
  ```
- Run TableReader without dilepton-track tables saved:
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json -b
  ```
