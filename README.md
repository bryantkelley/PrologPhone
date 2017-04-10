# PrologPhone
Prolog Project for COMP 3220 Principles of Programming Languages

This is a GNU Prolog file that contains the facts and predicates for determining paths to rooms with ringing telephones and determining all paths to ringing telephones. There are also procedures for finding minimum and maximum length paths from a given room to a specific ringing telephone or all ringing telephones. There are shorter, more sensible solutions for solving this problem, but this one is how I did it.

The floorplan is determined by the `touching/2` fact which is unable to be changed during execution. To prevent looping between the same two rooms exists the `traveled/2` fact that is checked to be false before continuing down a path by the `banned(RoomA, RoomB)` rule. The last facts are `min/2` and `max/2` which are used in checking the minimum and maximum paths.

The predicates meant for user interaction are `path_to_phone(FirstRoom, LastRoom, Path)`, `min_path_to_phone(FirstRoom, LastRoom, Path, Distance)`, and `max_path_to_phone(FirstRoom, LastRoom, Path, Distance)`.
