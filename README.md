# The SENTINEL intercomparison database
This is the model intercomparison database, maintained by the [SENTINEL collaboration](https://sentinel.energy).

It contains results from several energy systems models for scenarios of deep decarbonisation in Europe.  Specifically, the model intercomparison covers decarbonisation trajectories that meet 2030 and 2050 emission caps compatible with climate neutrality in Europe (the ‘climate neutrality’ scenario), and trajectories that assume no further policies for emissions reduction are made (the ‘current trends’ scenario). A tailored IAMC format has been developed for reporting and sharing results among partners and with external participants. 

More detail on the intercomparison design and the construction of this database can be found in the [Work Package 8 deliverables of the SENTINEL project]( https://sentinel.energy/outputs/deliverables/).

<br />


## Recommended citation of the scenario ensemble
When using this scenario database or exporting figures from any code included in this repository, please use the citation below. You should also include the version number of the database to ensure reproducibility of your work.

G. Oreggioni, M. Roelfsema, S. Mikropoulos, D. Van Vuuren and I. Staffell (2022). Model intercomparison database. Deliverable 8.2 of the SENTINEL project.

<br />


## Release notes
### Release 1.0 (25/02/2022)
Initial release to coincide with submission of Deliverable 8.2 of the SENTINEL project.

<br />


## Studies contributing to the scenario ensemble
Seven models (or combinations of models) contributed to the current release of the intercomparison database.  Further details about the models can be 


-	[Calliope][Calliope] (coupled with [DESSTINEE][DESSTINEE] and [HEB][HEB] for inputs)
-	[DESSTINEE][DESSTINEE]
-	[DESSTINEE][DESSTINEE] (coupled with [QTDIAN][QTDIAN] for inputs)
-	[EMMA][EMMA] (coupled with [Calliope][Calliope] for inputs)
-	[Energy_PLAN][Energy_PLAN] (coupled with [DESSTINEE][DESSTINEE] and [HEB][HEB] for inputs)
-	[HEB][HEB] (coupled with [QTDIAN][QTDIAN] for inputs)
-	[IMAGE][IMAGE]

[Calliope]: https://sentinel.energy/model/euro-calliope/ 
[DESSTINEE]: https://sentinel.energy/model/desstinee-demand/
[QTDIAN]: https://sentinel.energy/model/qtdian/ 
[HEB]: https://sentinel.energy/model/heb/
[EMMA]: https://sentinel.energy/model/emma/
[Energy_PLAN]: https://sentinel.energy/model/energyplan/
[IMAGE]: https://sentinel.energy/model/image/

<br />


## Format of the scenario ensemble
The scenario database is provided in a plain-text CSV file.  Each row describes a single result – the value of a specific variable over time, from one model, scenario and region.  The columns for each results are as follows:

*Model*: A string identifying which model produced the result: ``Calliope``, ``DESSTINEE``, ``EMMA``, ``Energy_PLAN``, ``HEB``, ``IMAGE``

*Scenario*: A string identifying which scenario was being modelled:
- ``Current_trends``, ``Climate_neutrality``, or ``Early_neutrality`` are the three main scenarios with increasing levels of ambition
- ``Climate_neutrality_gov``, ``Climate_neutrality_market``, ``Climate_neutrality_power`` are three variants on the 'Climate neutrality' scenario

*Region*: 
- ``EU27+UK`` for the former EU28 (all EU Member States and the United Kingdom)
- ``EU27`` for mainland Europe (all EU Member States) excluding the United Kingdom
- ``CEU&WEU`` for the combination of Western and Central Europe regions (covering 43 countries in total) as defined [here](https://models.pbl.nl/image/index.php/Region_classification_map).
- Individual countries are identified by their ISO3 code 

*Code*: The IAMC code to describe the variable.  1429 unique codes are included in this dataset, which are described further in the [Deliverable 8.2 report](URL).

*Unit*: The unit in which the results are reported
- Monetary values are measured in 2015 Euros
- Travel demand is measured in ``billion_km`` (billions of kilometres) ``billion_pkm`` (billions of passenger-kilometres) and ``billion_vkm`` (billions of tonne-kilometres)
- Options are ``billion_EUR_2015``, ``billion_EUR_2015/yr``, ``billion_pkm/yr``, ``billion_tkm/yr``, ``EJ/yr``, ``EUR_2015/GJ``, ``EUR_2015/MJ``, ``EUR_2015/ton_CO2``, ``GW``, ``GWh``, ``kt N2O/yr``, ``million``, ``million_km``, ``Mt CH4/yr``, ``Mt CO2/yr``, ``Mt CO2e/yr``, ``Mt CO2eq/yr``, ``TJ/yr``

Data values are then given for the years included by each model: 
- 1990, 1995, 2000, 2005, 2010, 2015, 2016, 2018, 2019, 2020, 2021, 2022, 2025, 2030, 2035, 2040, 2045, 2050, 2100

<br />


## Acknowledgements
This work was supported by the European Union's Horizon 2020 research and innovation programme under grant agreement No 837089 (SENTINEL).
