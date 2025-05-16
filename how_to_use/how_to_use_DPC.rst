How to use?
+++++++++++


Config (yaml file)
===================

  1. Define a disease
  2. Define disease cases
    - cases can be subdivided by severity, age, and gender (sex)
    - or single cases
  3. For each case one must have the LFC table
  4. Configure the all params using mtp_MB_01_config.ipynb
  5. Chenk if the basic configuration works
  6. Define the new LFC and FDR cutoffs manually or run BCA (if available)



Examples
===========

DPC and BCA must be able to split each case and define the disease, severity, age, and gender.

.. Disease:: 
**COVID-19**: 
  - **g1**: assymptomatic
  - **g2a**: mild
  - **g2b**: moderate
  - **g3**: severe

Cases:
  case_list = ['g1_male', 'g1_female', 'g2a_male', 'g2a_female', 'g2b_male', 'g2b_female, 'g3_male_adult', 'g3_female_adult', 'g3_male_elder', 'g3_female_elder']


.. Disease:: 
**MB**: 
  - **WNT**
  - **SHH** ~ Sonic hedgehog
  - **G3**
  - **G4**

Cases:
  case_list = ['WNT', 'G4']   # our study has only WNT and G4.

