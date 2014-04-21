# SDSC "gdal" roll

### THIS ROLL HAS BEEN DEPRECATED

The functionality of the gdal-roll has been rolled into a new SDSC Rocks roll named <a href="https://github.com/sdsc/geo-roll/" target="_blank">GEO</a>.

Please use the <a href="https://github.com/sdsc/geo-roll/" target="_blank">geo-roll</a> instead of this one.

-----

## Overview

This roll bundles the GDAL geospatial data abstraction library.

For more information about GDAL please visit the official web page:

- <a href="http://www.gdal.org" target="_blank">GDAL</a> is a translator library for raster geospatial data formats.


## Requirements

To build/install this roll you must have root access to a Rocks development
machine (e.g., a frontend or development appliance).

If your Rocks development machine does *not* have Internet access you must
download the appropriate gdal source file(s) using a machine that does
have Internet access and copy them into the `src/gdal` directories on your
Rocks development machine.


## Dependencies

Unknown at this time.


## Building

To build the gdal-roll, execute these instructions on a Rocks development
machine (e.g., a frontend or development appliance):

```shell
% make default 2>&1 | tee build.log
% grep "RPM build error" build.log
```

If nothing is returned from the grep command then the roll should have been
created as... `gdal-*.iso`. If you built the roll on a Rocks frontend then
proceed to the installation step. If you built the roll on a Rocks development
appliance you need to copy the roll to your Rocks frontend before continuing
with installation.


## Installation

To install, execute these instructions on a Rocks frontend:

```shell
% rocks add roll *.iso
% rocks enable roll gdal
% cd /export/rocks/install
% rocks create distro
% rocks run roll gdal | bash
```

In addition to the software itself, the roll installs gdal environment
module files in:

```shell
/opt/modulefiles/applications/gdal
```
