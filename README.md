# About MVML
Megaverse Markup Language (MVML) is meant to be used as a basis for character sheets for use with the Palladium Books' line of Role-Playing Games, often marketed as the Palladium Megaverse&reg;.

## Scope
The primary goal of this project is to create a data format for self-describing, fully independent character sheets. While all data elements are within scope of the project, any code, transforms or other conversion from this data exchange format into a human-readable format are expressly outside of the scope. It is the intention of this project to allow a true, common exchange of character information between players and/or game masters, irrespective of their preferred character sheet format or storage medium.

The secondary goal is to enable sharing of specific types of user-created content, such as custom races, classes, weapons or spells while maintaining a common structure that adheres to the Palladium Books format. Most types of content will have their own schema so this data can be shared outside a specific character.

## Structure
The data exchange format will be based on the premise that published rules will be used in connection with this character data. However, because house rules are commonplace, consideration will be made to make data structure to be somewhat flexible as to how it will be used.

Character data will be generally organized as follows:
* Character
  * Player information
  * Race
    * Core Attributes
    * Hit Points, Damage Capacity
  * Class (unbounded for multi-class characters)
    * Experience, including full table
    * Class-specific attributes (e.g. ISP, PPE, etc.)
    * By-level selections, including
      * Skills & Abilities
      * Spells, Psionics, Tattoos, etc.
  * Inventory & Equipment (including weapons & ammunition)
    * Features, spells, attributes of items, such as weapon systems on a vehicle or spells castable by a rune weapon
    * Quantity

This structure is to ensure that the highest occurrence of data dependencies are kept as child objects (e.g. spell durations, skill proficiencies, etc. are based largely on level, which in turn is centered on a single character class). Multi-class characters require tracking each skill not only by level but by class. The structure reflects these important dependencies, regardless of how they are implemented.

Currently, no data will be stored at the MVML level as to which of possible conflicting items are to be shown/used. This will be a determination for the consuming system, ensuring MVML is used as a data persistence system and not a logic or rule persistence system.

## Standards & Common Tools
* [XML Schema (XSD) v1.1](https://www.w3.org/TR/2012/REC-xmlschema11-1-20120405/) - XML Schema definition/compliance
* [oXygen XML Editor v19](https://www.oxygenxml.com/xml_editor.html) - Project IDE
* [github](https://github.com) - Project Repository, Wiki, etc.

## Future Projects
It is anticipated that this project will be used as a basis for future projects in the community to display top-level character data to the end-users in a variety of formats.

### Sponsor Projects
This project is being sponsored by **[Rifters](https://rifters.org)** with the goal of bringing their own online play system to their Palladium Books-based community. They also plan on brining multiple character export options including the raw MVML and conversion to their existing [online-fillable character sheet](https://megaverseonline.com/download/rifts-fillable-character-sheet/).

### Community Content
The data contained in this format is expected to be filled with copyrighted information such as core book skills, spells, races and character classes, just like any other character sheet is today. However, once a common method for self-describing character-centric data is available, Megaverse Online will house derivative works based on the Palladium Books Megaverse&reg; including fan-created O.C.C.s&trade;, races or other non-copyrighted information for those who wish to use it.

For this reason, we ask for participation from the content creation community to ensure that we not only take material published by Palladium Books into consideration but also their own structure, possibly with modifications to the core rule system.

### Commercial Content
It is a goal to enable Palladium Books or their business partners to be able to host Palladium Books published information required to generate characters through this format for a commercial venture such as an online subscription model. As such, we likewise call upon Palladium Books and their business affiliates to participate in this community project.
