## List of commands to run
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
- Run TableReader:
  ```ruby
  o2-analysis-dq-efficiency --configuration json://configAnalysisMC.json --aod-writer-json writerConfiguration_dileptons_track.json -b
  ```
