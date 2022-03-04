## To do list

ToDo: share code of Maurice for fast simulation studies
-> share code during next week  (Maurice)
 --- on github
-> Luca: understanding how information is stored to adapt for 3 prong
--> Luca/Maurice: merging (complete information from different tables (BDT)) output 
-> proposal for DQ/O2 (Maurice with help of Batoul and Luca)

-> Michael: follow up on external account and  test cvfms O2 on cluster.
--> investigate: EOS disc space for analysis


-> Batoul: start with digging in code when arriving and discussion on T&P etc. ...
-> Michael/Maurice: trigger simulation production after discussion with Roberto and Sandro. (Michael for generator inclusion) 
	Could do local pp production on cluster for testing (depending on time)?
	
-> Create github for documentation (Luca Micheletti with documentation)


---> pp luminosity: 30 /pb. (next week)

-> next meeting: 4th of March



Prequisites:

1) Adapt table-tree-maker in O2 for Trimuon

(should be adapatable from Jpsi+track part for B+->jpsi K^+ analysis model)

-> Batoul (priority),
Maurice, Luca

2) introduce all required variables in Varmanager in O2 (pending since tracking implementation not yet finished)

- first steps done by Maurice
- start with 2-track variables (anyhow needed for all kind of analyses)

3) implement B_c Veg generator into O2

- first steps done by Maurice

4) put in place interface for root trees/arrow tables as analysis 
- rudimentary thing avaialble in table-reader, to be adapted

- check if possible to take same interface as heavy-flavour working group
--> Luca with contact to Fabrizio


----> can be already done once we have reasonable simulation and tracking in O2


5) take care of local cluster adaptation for O2 analysis at IRFU
-> cvfms for O2 (or local installation if needed)
-> acces for Luca


Actual analysis preparation (requires largely first 3 steps in place):

0) acess feasibility in pp and PbPb with a given luminosity more precisely than previously to define priorities, in any case, at some point should be feasible. Since predictions are quite astronomic, already limit setting could be interesting (although requiring additional work)

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
