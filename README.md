# nexus-calculators

This repository is intended to house a number of html-based calculators that nexians may find useful in their TEKs

## Using the calculators

After reviewing the code, if you're inclined, download it [here](https://github.com/orchidist/nexus-calculators/archive/refs/heads/main.zip). Once unzipped, you can open any calculator you like, and the browser takes care of the rest. Have fun! 

## Calculators in this repo

### salt-converter.html

This calculator converts salts of various molecules into equivalent masses of other forms.

It also allows for easy calculation of % yield for use during extraction.

#### Converting between different salts

Choose the form of the alkaloid you have, then input the mass you have. The calculator will automatically convert it into equivalent quantities of freebase and salts

#### Working with varying stoichiometric ratios

Some acids have the potential to bond with more than one alkaloid molecule. In many cases we are not certain which ratio we have. This calculator produces conversions between the different possible ratios to help deduce which ones actually exist.

#### Water of crystallization

Some salts incorporate water molecules in their crystal lattice, use the hydration fields to adjust for this variable.

#### Calculating yield
Choose the form of the alkaloid you're collecting using the drop downs, then insert the amount of raw material in grams, and the amount of final product in grams. The calculator will automatically account for the molecular weight of the acid used and return the yield in terms of the freebase alkaloid. 

#### Adding new alkaloids

Simply add a new one to the `alkaloids` data structure in the code in the following format:

```json
"<YOUR ALKALOID HERE>": {"molarMass": <MOLAR MASS HERE>}
```

Don't forget to add a comma between entries!

#### Adding new anions

This is very similar to adding to `alkaloids`, except you'll indicate the number of acidic protons in the `protons` value.

```json
"<YOUR ALKALOID HERE>": {"molarMass": <MOLAR MASS HERE>, "protons": <PROTON NUMBER HERE>}
```