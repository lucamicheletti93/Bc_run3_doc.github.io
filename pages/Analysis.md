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
### TableMaker
- Run TableMaker on data/AO2D_Bc100.root
  ```ruby
  python runTableMaker.py config/configTableMakerMCRun3.json -runMC table-maker-m-c:processMuonOnlyWithCov:true
  ```
- Run TableMaker on data/AO2D_NonPromptJpsi.root
  ```ruby
  python runTableMaker.py config/configTableMakerMCRun3_NonPromptJpsi.json -runMC table-maker-m-c:processMuonOnlyWithCov:true --add_track_prop
  ```
  
- Run TableReader with dilepton-track tables saved:
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json --aod-writer-json writerConfiguration_dileptons_track.json -b
  ```
### TableReader
- Run TableReader without dilepton-track tables saved:
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json -b
  ```
