## To do list

ToDo: share code of Maurice for fast simulation studies
-> share code during next week  (Maurice)
 --- on github

-> Michael: follow up on external account and  test cvfms O2 on cluster. not yet solved, going for CERN ressources for the moment
--> investigate: EOS disc space for analysis


-> Batoul: startrd T&P, and working on merging debugging
-> simulation signal: bricolage solution working  (non-dev branch of DPGO2) 
------> Bother again simulation people (Sandro/Gustavo)
	
-> Create github for documentation (Luca Micheletti with documentation)


---> pp luminosity: 15 /pb. 

-> next meeting: 15th of July, 11 AM



Prequisites:

1) Adapt table-tree-maker in O2 for Trimuon

(should be adapatable from Jpsi+track part for B+->jpsi K^+ analysis model)

-> Done, at least functional, may require adaptation once analysis starts

2) introduce all required variables in Varmanager in O2 (pending since tracking implementation not yet finished)

- start with 2-track variables (anyhow needed for all kind of analyses)
->  to be verified soon, at least single-track dca missing, cos(thetastar_jpsi_mu) missing
--> trigger Shreyasi again for single-track dca

3) implement B_c Veg generator into O2

- first steps done by Maurice
-- waiting

4) put in place interface for root trees/arrow tables as analysis 
- available

- check if possible to take same interface as heavy-flavour working group
--> possible with current signal simulation and data structure
--> HF has 2 signal categories


5) take care of local cluster adaptation for O2 analysis at IRFU
-> cvfms for O2 (or local installation if needed)
-> acces for Luca
--> pending since O2 not yet running, under discussion

Actual analysis preparation (requires largely first 3 steps in place):

0) acess feasibility in pp and PbPb with a given luminosity more precisely than previously to define priorities, in any case, at some point should be feasible. Since predictions are quite astronomic, already limit setting could be interesting (although requiring additional work)
-> pp 13 TeV should be feasible
-> PbPb depending on background rejection/detector calibration etc. (should be feasible as well if everything up to specifications)


I) Studies (CMS, fast simulation, simple considerations) to identify correlated background that needs to be simulated
-- anticipate full simulations that we can have easily and that we should ask for
-- might be useful to have some fast simulation analogue from Maurice studies to make some simple studies with large statistics, limitations to be discussed.
--- for instance, need to study correlated backgrounds with a decay in flight of a hadron producing a valid muon candidate  whether we can afford to simulate this
-----> useful to check what is available as recipe from Light flavour group for nuclear production (they trigger also on particles in the simulation produced in the GEANT transport)


II) general to muon analysis in MFT (also non-prompt jpsi), but most crucial for B_c since probably most cutting into resolutions and requiring good understanding of matching

- identification of data driven control of matching efficiency (in pp, hopefully tag-and-probe if fake match background in data still okish, in PbPb to be identified)
- identification of data driven control of DCA resolution for matched muons

III) identification of analysis pipeline:

- sensitivity study for input features for BDT or similar
--- can be probably already defined prior to data with full simulation
- which dimensions used for final signal extraction (e.g. mass of trimuon system or something else)

-- studies for definition of background training samples, templates for background templates

IV) decide whether with blinding or not.

Analysis

A) selection optimization: BDT/etc 

B) control sample definitions

B) signal extraction: template definition, fitting procedure

D) Accxeff correction (apart from selection efficiency common with non-prompt/prompt jpsi) and its uncertainty

E) Systematic uncertainties related to selection (resolution, unknown kinematics, unknown backround composition etc.) and control samples

google-doc: link:


https://docs.google.com/document/d/1idP7ueNuwJ16qJQxDja_9YV9GinSnn0_ZJ8cRxYGg84/edit
