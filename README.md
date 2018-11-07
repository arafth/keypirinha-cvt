Keypirinha Plugin: Cvt
=========
# A universal unit converter for the Keypirinha launcher

This plugin for Keypirinha provides unit conversions for the following measures:

* Distance
* Area
* Volume
* Mass
* Speed
* Time
* Force
* Pressure
* Energy
* Power
* Fuel Consumption
* Temperature
* Data Size

## Usage ##

To convert a number of certain unit type:
```
<number> <from-unit-name>
```

Once the `from-unit-name` is typed, a list of units to convert to along with converted values is shown. At this point you can type a space (or any other non-alphanumeric character except /) and the target unit or select it from the list. Hit Enter to copy the converted value to the clipboard

![Example: convert 12 kg to other units](images/example-weight-conversion.png?raw=true)


To see a list of valid unit names for a given measure, type:
```
Cvt: <measure-name>
```
You don't need to remember the measure names - a list of measure names will be offered to select from. The list of units will include the full unit name as well as the conversion factor and offset (if applicable).

## Customizing Conversions ##

Cvt lets you customize the list of measures and units it supports. To customize the list, place a copy of the cvtdefs.json file (from this repository or from the plugin file) in the user configuration directory (`Keypirinha\portable\Profile\User`) and add there your measures or units. 

When a custom conversion file is used, the built-in conversion file is ignored so you won't see new measures and units that come with Cvt. When using a custom conversion file, typing Cvt: will show an option to reload the custom conversion file.

## Installation ##

The easiest way to install Cvt is to use the [PackageControl](https://github.com/ueffel/Keypirinha-PackageControl) plugin's InstallPackage command. 

For manual installation simply download the cvt.keypirinha-package file from the Releases page of this repository to:

* `Keypirinha\portable\Profile\InstalledPackages` in **Portable mode**

**Or** 

* `%APPDATA%\Keypirinha\InstalledPackages` in **Installed mode** 

## Credits ##

* Thanks the folks at [Quartic Software](http://www.quartic-software.co.uk/) for their awesome Android calculator app [RealCalc Plus](https://play.google.com/store/apps/details?id=uk.co.nickfines.RealCalcPlus) from which I took the list of measures, units and their conversion rules. If you like an HP-style RPN calculator in your phone, that's the one to use!
* Thanks [ArmaniKorsich](https://gitter.im/ArmaniKorsich) for the inspiration to write this plugin.

## Release Notes ##

**V1.0.1**
- Support Keypirinha's space_as_tab=yes setting. No need for space after number so now 12kg is fine. To enter the target unit any non-alphanumeric character (other than /) can be used as separator. 

**V1.0**
- First formal release
- Made major change (simplification) to the usage 
- Add way to see available units as well as conversion factors and offsets (when applicable)
- Fixed errors in pressure and other conversions

**V0.2**
- Fix temperatue and fuel consumption conversions
- Aliases are no longer case sensitive
- A copy of cvtdef.json can be placed in the User folder for customization
- Known issue: Keypirinha shows just 8 suggestions, when more than 8 units, some are not visible but still available if you type the unit code

**V0.1.1**
- Fixed aliases to make them enter-able.
- Aliases selection is case sensitive - it should not be.

**V0.1**
- Initial release, rough around the edges.
- Known issues: temperatue and fuel consumption conversions are broken, some aliases are not enter-able.

