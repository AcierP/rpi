# `rpi` - rolimon's python interaction

`rpi` is an **open source** python-based **rolimon's api wrapper**. It
provides an end-to-end pipeline in which each component can
be easily modified to get item, user, and game statistics. `rpi` also allows rolimon's api 
to be parsed with ease and includes data extraction and interpretation models, provided by 
[rolimon's private api](http://rolimons.com).

## Table of Contents

* [Installation](#installation)
* [Examples](#Examples)
* [Getting started](#getting-started)
* [Documentation](#documentation)

## Installation

To pip install `rpi` from github:

```bash
pip install git+https://github.com/AcierP/rpi.git
```

## Examples

### Getting an item's value
```python
import rpi
value = rpi.getValue(21070012)
```
### Getting the item attributes to every item on the catalog
```python
import rpi
itemdata = []

catalog = rpi.getlimitedsCatalog(format='id')

catalogatrributes = rpi.getitemAttributes(catalog))
```
### Getting the value, demand, acronym, trend, projected status, and hyped status of an item
```python
import rpi
details = rpi.getitemAttributes(21070012)

itemattributes = details['name'], details['acronym'], details['value'], details['demand'], details['trend'], details['projected'], details['hyped'])
```
