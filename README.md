# Aurora Altium Library

An exceptional, open source database library for Altium.

Current part count: 29,765 in over 600 packages.

This library has been built for high quality data, with high quality footprints and high quality 3D models.

# The Library
### Why use this library over something like Ultra Librarian?
Ultra librarian doesn't have high quality 3d models or parametrics. If all you need is basic footprint, Ultra librarian is what you want. If you want something open source, ultra high quality parts and with all the data fields you desire.. then you'll probably really like this library.

If you're integrating your electronic design into a housing or designing injection moulded cases for it - you need accurate 3d models or your mechanical engineers will spend a lot of time making sure the case fits your design files.

### Data
All parts are matched with every relevant parameter that Digi-Key has for the part, so you can search/filter within Altium for the part you require. If you are looking for low Rds(on) N-Ch fets, just add the Rds(on) column to the Altium library window and sort by it.

Every part has a link to the part on Digi-key, and has a link to the datasheet for the part for ease of design. Both the Digi-Key part number, price, and manufacturer name/part number are stored, now your BOM will be completely filled out automatically.

### Footprints
Every part has a footprint created to match it's manufacturers recommended footprint by the manufacturer, or lacking that, an IPC Compliant footprint for the manufacturers specific package sizing. There are no generic footprints within this library, everything is manufacturer specific.

Every footprint has a high quality, dimensionally accurate, accurately coloured 3d model. For complex parts (connectors like modular jacks), the manufacturers model is preferred however is always fully coloured and checked for accuracy against their drawings and modified as required.  I've found issues with the accuracy of the manufacturer issued model from most models, where they do not match the datasheet - every instance has been checked with the manufacturer and many have re-issued their 3d models because of these checks.

Basic parts (TSSOP/SOP/Resistors etc) I have created every model from scratch in SolidWorks, if the manufacturers dimensions vary from the JEDEC standard, they receive their own version of the 3d model (see SOT-23-3..) For ultra basic parts with no features (QFN/DFN), a black basic Altium 3D extrusion is used of the correct size.

Every part's centre position is where the Pick and place head should grab the part. For companies running their own Pick and Place machine, this is very convenient compared to centres at pin 1/centre of pads - your pick and place export list now has centres in the correct location.

### Symbols

Every symbol in the library is somewhat standardised as to where pins are located, such as VCC in the top left, GND in the bottom left, user function pins on the right (controllable inputs/outputs). Standard protocols like SPI have the pins in the same order in every part - however manufacturer datasheet labeling is kept (DOUT rather than MISO for example) to make it easier to reference the datasheet. All components within a database category should have similar if not identical layouts/pin groupings where possible. This makes it much easier to switch out components.

All passive components, such as resistors and capacitors all have the same size symbol lead span, keeping your schematics tidy.

# What components are contained in the library?
There are currently over 27000 parts in the library, this number sounds quite large but when you consider you need every value of resistor in 1%, 0.5%, 0.25%, 0.1% and 0.05%, in 0201, 0402, 0603, 0805 and 1206... you're now looking at over 5000 resistors.

Generally only SMT parts are in the library, except connectors, buttons and displays which have a mixture.

There are currently parts from over 120 manufacturers in the database.

# Contributing

Want to contribute? Great!

To contribute parts:
Please ensure your 3d models are completely accurate to the manufacturer's specifications. Do not submit parts with 3d models that are not sourced from the manufacturer, or that you have not created yourself from the manufacturers drawing. Parts sourced from the manufacturer should be correctly coloured in, most manufacturers give you colourless or very oddly coloured models (Hirose and JST especially.)

Standard colours:
- Black: SolidWorks [Plastics -> Medium Gloss -> Black Medium Gloss Plastic] R:26 G:26 B:26
- Tin/Lead/other "silver" plating: SolidWorks [Metal -> Zinc -> Polished Zinc] R:204 G:206 B:204
- Gold: SolidWorks [Metal -> Gold -> Polished Gold] R:255 G:206 B:127
- White: SolidWorks [Plastics -> Medium Gloss -> White Medium Gloss Plastic] R:255 G:255 B:255

The only time you should need to stray from these colours is for LEDS. Use SolidWorks Medium Gloss plastics for these colours.
- Red: R177 B25 G25
- Green: R73 G169 B84
- Blue: R2 G61 B210
- Yellow: R255 G239 B35

If you cannot colour your 3D model, do not submit it, ask someone (me?) to colour it for you.

All models should have fillets, drafts and features as the real device would. If you can see it in the manufacturers drawing, it should be in the model. If you can see it in a photo or render on Digi-Keys site, it should be in the model. This library should only contain high quality parts.

All footprints should match the specific parts manufacturer drawing, either as their recommended land pattern, or if that does not exist, then the generated IPC Compliant footprint that Altium made. Please ensure pin 1 is clear marked - a single dot to mark pin 1 is not clear enough, it can be easily lost on high density boards. Check what other similar parts have.

Symbols should be laid out with pins in logical groups, not as they appear on the package or in their pin order. Do not use generic symbols for specialised parts. If an ISO/ANSI standard symbol exists for a type of component (transistor for example), use it.


License
----

This project is forked from: https://github.com/issus/altium-library

You may use this library commercially in commercial designs, however you may not charge your clients for component design time if you are just going to use a part from this library. You may not charge anyone for the footprints, 3d models or schematic symbols contained in this library. You may give you clients a copy of this library, as long as you attribute the source back to this GitHub Repository. You may not claim credit for the work in this library unless you have contributed it yourself, you must give attribution where it is due.


[//]: # (These are reference links)
