# Lennard Jones Molecular Dynamics in C++

![Box of Lennard-Jonesium](lj.png)

## About

Simulates Lennard Jonesium using Molecular Dynamics.

The program is written in C++ and requires [Boost](http://www.boost.org/)
libraries and development headers for reading the .ini file, and xdrfile for
writing the trajectory to .xtc. Some of the classes I use are based on my
[libgmxcpp](https://github.com/wesbarnett/libgmxcpp) library.

Current features:

* Andersen thermostat
* Velocity Verlet integrator
* Calculate RDF
* Calculate velocity distribution
* Neighbor lists
* Block error analysis

Reduced units are used. 

## Compiling

To compile simply do:

    make

You may have to modify `Makefile` if you have libraries installed in a custom
location.

## Running

To run do:

    ./md md.ini

If no file configuration file is specified, then the program attempts to open
'md.ini.' If the file you specify is not found, the defaults options are used
for the program (printed to the screen).

When running the program an initial configuration of
atoms is generated by randomly inserting them into the box according to the
specified density, ensuring that the atoms are not too close to each other. Then
then simulation begins.

## License

Copyright (C) 2015 James W. Barnett <jbarnet4@tulane.edu>

This program is free software; you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation; either version 2 of the License, or (at your option) any later
version.

This program is distributed in the hope that it will be useful, but WITHOUT ANY
WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A
PARTICULAR PURPOSE.  See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with
this program; if not, write to the Free Software Foundation, Inc., 51
Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA.

The full license is located in a text file titled "LICENSE" in the root
directory of the source.

## Resources

See Frenkel and Smit's *Understanding Molecular Simulation* as well as Allen and
Tildesley's *Computer Simulations of Liquids*.
