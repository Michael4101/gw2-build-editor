
# Guild Wars 2 Build Editor 

This document uses some language in a context unique to Guild Wars 2 and video games more broadly. To aid in reader comprehension, terms used in this way are explained under [Definitions](#definitions) and can quickly be found by clicking these words the first time they appear in the text.

For more information about this project's architecture and features, see the technical document PDF in this repository.

<table border="0">
  <tr>
    <td align="center" valign="middle" width="50%">
      <p align="center">
        <img src="/images/editor-main-overview.png" alt="Main Build Editor Interface" width="60%">
      </p>
    </td>
    <td align="center" valign="middle" width="100%">
        <img src="/images/editor-traits-overview.png" alt="Traits Configuration Interface" width="100%">
    </td>
  </tr>
</table>
    
## Introduction 

This ongoing project is a character [Build](#build-definition) editor for Guild Wars 2, a popular Fantasy MMO (Massively-Multiplayer Online game) where a player's experience is largely guided by the [Profession](#profession-definition) they start with and the Build they create for it.

Most committed players will orient their Build towards a certain [playstyle](#playstyle-definition), and will attempt to increase the relevant [Attribute](#attribute-definition) values and create a suitable combat profile. For example, Builds with an affinity for sustained face-to-face melee combat are frequently characterised by heavy investments in the _Power_ and _Toughness_ Attributes, as these will increase the damage dealt and reduce the damage taken by the character respectively. 

This Build Editor functions as an advanced calculator which allows users to conveniently arrange and simulate a character Build with the desired Attribute distribution without committing the time and resources that might otherwise be wasted in-game on trial-and-error Build crafting. 

## Quick Instructions

### 1. Select a Profession
This determines which Build components are available.
### 2. Select an Attribute filter (optional)
This narrows available choices towards a particular Build focus.
### 3. Create a Build
Select equipment, [Traits](#trait-definition) and other components from the available drop-down menus.
### 4. Configure Traits
Use the _Trait Configuration_ sheet to toggle active states and adjust stack counts where applicable.
### 5. Review the Results
Final Attribute totals and derived Attributes. 



## Detailed Instructions 

The main Editor is split into two sheets, _Build Configuration_ and _Trait Configuration._ The latter becomes relevant only when [Specialisations](#specialisation-definition) and [Traits](#trait-definition) have been selected in the former and can significantly change how these selections affect final Attribute totals. 

To make a selection, click on any field containing italic text and choose an item from the drop-down list that appears. If the text is missing, these fields can also be identified by their background colour - see the legend on the right-side of the Build Configuration sheet. If the selected item is a Build component, its Attribute bonus (if any) will appear beside it in the appropriate column of the adjoining table.  


### Selecting Profession and Attribute Filter 

First, choose the Profession in the top-left corner. This is important, as a character's Profession determines what they have access to across several core Build components, including Specialisations and Traits. Selecting a Profession will limit options based on what that Profession has access to.

Next to the Profession selection field, selecting an Attribute in the Attribute filter box to further constrain available options is recommended to guide and develop a coherent Build identity. For example, filtering for Build components that provide Healing Power is a good choice when creating a group support-oriented Build.


### Creating a Build

Select Build components on the left-side of the screen using the previously described selection fields. If a particular distribution of Attribute bonuses on a component is required, refer to its category's _Source_ sheet after filtering for one of the desired Attributes - all results that match the criteria will be named in the _Filter_ column on the right-side of the table.

Component sections are clearly categorised for ease of use and components not yet selected are recognised by the phrase "(Select)" or a blank field.

A red selection field indicates its contents is in conflict with another selection, for example an incompatible Specialisation-Profession matchup. Clear or replace these selections to ensure final Attribute totals are valid.


### Tuning and Final Results

In the Trait Configuration sheet, users can toggle the active states of selected Traits, altering or disabling their accompanying bonuses. Multipliers on Traits with [stacking](#stacking-definition) can also be selected up to a per-Trait maximum. If a condition or stack multiplier is changed in the Trait Configuration sheet, the bonus value for that Trait in the Build Configuration sheet will be altered. 

Users can also enable various [Boons](#boon-definition) in a box next to final results. Some of these provide additional bonuses inherently, such as Might increasing Power and Condition Damage, while others require certain active Traits to have an effect on Attributes. For example, the Quickness Boon reduces a character's ability cooldown and does not influence Attributes under normal circumstances, but with the "Imbued Haste" Trait active it also increase the Condition Damage, Healing Power and Vitality Attributes.

Final Attribute results are displayed at the bottom of both sheets. The values of base Attributes are translated into practical values, known as _derived Attributes,_ where the relationship can be solved directly. For example, the base Attribute _Vitality_ contributes to the derived Attribute _Health,_ the exact amount of damage a character can sustain before being defeated. Some attribute totals are joined by additional values inside parentheses - this represents the remaining amount required in that base Attribute to achieve its associated derived Attribute's [hard cap](#hardcap-definition).

Calculations that depend on additional combat variables, such as weapon damage, skill coefficients or target defences are currently excluded. This is a limitation that will be addressed in future iterations.

## Features 

### Straightforward UI
Main build component selections, corresponding attribute bonus values and final attribute totals are consolidated in one sheet.
### Additional Trait Tuning
Toggle active states and configure stacking bonuses.
### Contextual UI Filtering
Available options are filtered to be compatible with parent field selections, including character profession bonus attribute filtering.
### Traceability
Selected components are highlighted in their source tables.
### Complex Bonus Resolution
Component bonus values are solved in resolution modules according to their bonus type(s) and aggregated in the main interface.

## Tools used
### Python
Data extraction and processing.
### Excel
Build editor, attribute calculations and user interface.
### [Thonny](https://thonny.org/)
Python IDE.


## Definitions
<a name="build-definition"></a>
### Build
The collective term for the Specialisations, Traits, items and upgrades a player chooses for their character.
<a name="attribute-definition"></a>
### Attribute
The measure of a player character's ability in one facet of combat, such as dealing damage or healing.
<a name="profession-definition"></a>
### Profession
The core of a character's identity which determines their available Specialisations and Traits.
<a name="trait-definition"></a>
### Trait
A character enhancement that may be selected by the player or applied automatically.
<a name="specialisation-definition"></a>
### Specialisation
A Trait line oriented towards a certain playstyle.
<a name="hardcap-definition"></a>
### Hard Cap
The effective limit of a base Attribute, at which point its derived Attribute is maximised and all further investment is wasted. For example, _Precision_ cannot increase _Critical Chance_ past 100%, so that is point at which Precision's hard cap has been achieved. 
<a name="playstyle-definition"></a>
### Playstyle
A player's preferred approach to a game.
<a name="boon-definition"></a>
### Boon
Beneficial status effects.
<a name="stacking-definition"></a>
</table>
### Stacking
An effect that multiplies based on its number of "stacks."


