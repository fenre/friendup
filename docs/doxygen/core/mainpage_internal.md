# For internal use only

This documentation is the internal version of the documentation generated by Doxygen.

It contains the list of TODOs generated by Doxygen, and should likst the things reported as 
bugs (as soon as I have found the command to do it).

This is not to be distributed.

A macro 'INTERNAL' is defined when the doc is generated, you can have sections of your
code be only present in the internal docs by documenting the functions and structures within
exclusion macros (note, I have to put a dot infront of the hash, as the .md format of this file
would make them affect the display you are reading right now).

.#ifdef INTERNAL

/**
 * My internal function for Friend only
 *
 * @params
 * @return
 */

.#endif

You can have different definitions for both internal and open-source...

.#ifndef INTERNAL

/**
 * An incredible function that does everything all the time!
 *
 * It really works!
 *
 * @params
 * @return
 */

.#elseif

/**
 * A crappy function that Hogne made me do.
 * 
 * I was against, it is crap sorry.
 *
 * @params
 * @return
 */

.#endif

... but warning, those comments will be in the code of the open-source version, if I do not 
remove them with Friend Parser... (we should do it, we would be a little more free and secure 
in our Doxygen comments)...
