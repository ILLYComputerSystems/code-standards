Branching
=========

This file contains code standards relating to branching in source control.

Branch Types
--
There are several different branch types serving different purposes.
* Master branches represent the main product in its current stable state. There is always one master branch per product. It is sometimes referred to as a trunk.
* Release branches come off the master branch and represent the state of the product when it was released to market. No development is to be done on these branches, unless in the case of applying hotfixes or security patches. Usually a named tag should be created showing the position of the branch that a client is currently using.
* Development branches are where all of the main development occurs. Several development branches can exist per project and each one usually refers to a significant development task.
* A development task may be split into features. These would be represented as feature branches which would be merged back into the development branch.

Merging and Rebasing
--
Merging and rebasing are the two most commonly used ways to integrate changes made in one branch into a different branch.
* Merging is performed where the team would prefer that simultaneous development is shown in the source control history. Merging should almost always be the sole option when incorporating series of changes from one branch into another branch where many conflicts are possible.
* Rebasing is performed where the team would rather the development is shown as one continuous stream in the source control history. Rebasing should almost always be the sole option when working on the same branch.