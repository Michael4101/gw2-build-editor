# Guild Wars 2 Build Editor 

This document uses some language in a context unique to Guild Wars 2 and video games more broadly. To aid in reader comprehension, terms used in this way are explained under [Definitions](#definitions) and can quickly be found by clicking these words the first time they appear in the text.

## Introduction 

This ongoing project is a character [Build](#build-definition) editor for Guild Wars 2, a popular Fantasy MMO (Massively-Multiplayer Online game) where a player's experience is largely guided by the [Profession](#profession-definition) they start with and the Build they play it with. 

Most committed players will orient their Build towards a preferred [playstyle](#playstyle-definition), and will attempt to increase the relevant [Attributes](#attribute-definition) and create a suitable combat profile. For example, Builds with an affinity for sustained face-to-face melee combat are frequently characterised by heavy investments in the Might and Toughness Attributes, as these will increase the damage dealt and reduce the damage taken by the character respectively. 

This Build Editor functions as an advanced calculator which allows users to conveniently arrange and simulate a character Build with the desired Attribute distribution without committing the time and resources that might otherwise be wasted in-game on trial-and-error Build crafting. 

## Instructions 

The main Editor is split into two sheets, "Build & Totals" and "Trait Configuration." The latter becomes relevant only when [Specialisations](#specialisation-definition) and [Traits](#trait-definition) have been selected in the former and can significantly change how these selections affect final Attribute totals. 

### Selecting Profession and Attribute Filter 

First, choose the Profession this build is for in the top-left corner. This is important, as a character's Profession determines what they have access to across several core Build components, including Specialisations and Traits. Selecting a Profession will limit options based on what that Profession has access to. 

 

Next to the Profession selection field, selecting an Attribute in the Attribute filter box to further constrain available options is recommended to guide and develop a coherent Build identity. For example, filtering for Build components that provide Healing Power is a good choice when creating a group support-oriented Build.

### Creating a Build 

To make a selection, click on any field containing italic text and choose an item from the drop-down list that appears. If the text is missing, these fields can also be identified by their background colour - see the legend on the right side of the Build & Totals sheet. If the selected item is a Build component, its Attribute bonus (if any) will appear beside it in the appropriate column of the adjoining table.  

### Tuning and Final Results

In the Trait Configuration sheet, users can toggle the active states of selected Traits, altering or disabling their accompanying bonuses. Multipliers on Traits with [stacking](#stacking-definition) can also be selected up to a per-Trait maximum. If a condition or stack multiplier is changed in the Trait Configuration sheet, the bonus value for that Trait in the Build & Totals sheet will be altered. 

## Features 

- Straightforward UI - Main build component selections, corresponding attribute bonus values and final attribute totals are consolidated in one sheet.
- Additional trait tuning - Toggle active states and configure stacking bonuses.
- Contextual UI filtering - Available options are filtered to be compatible with parent field selections, including character profession bonus attribute filtering.
- Traceability - Selected components are highlighted in their source tables.
- Complex bonus resolution - Component bonus values are solved in resolution modules according to their bonus type(s) and aggregated in the main interface.

## Tools used
Python
Excel

## Definitions
<a name="build-definition"></a>
Build<br>
</br><a name="attribute-definition"></a>
Attribute<br>
</br><a name="profession-definition"></a>
Profession<br>
</br><a name="trait-definition"></a>
Trait<br>
</br><a name="specialisation-definition"></a>
Specialisation
