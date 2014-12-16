# Comfortable C

The C language has been getting on a bit. And although I still like it, for it's
bare metal simplicity and no-nonsence attitute, it is time to admit: It has been
getting a bit rusty lately.

This engine will in most of it's parts be written mainly in c. To spare a bit of
headache, I attempt to run all the code through a prepocessor that will
(hopefully) manage some of the ugly stuff for me.

This also means, that I won't be stricktly writing ```c```, but a slight
deriverat. **Comfy** if you will.

I don't know, if I really need to, but it seems fun enough.

To not get lost, and also find out later, whether anything worthwhile could be
gained from it, I will be documenting all the languagege tweaks I made here.

## Automatic include guard

    @version: FUTURE

I never met anybody, who used includes in a way, that they didn't profit from
include guards. Thus (except for lazyness) I have never seen C (or C++) code
that didn't include-guard its headers.

The **Comfy** preprocessor will therefore prepend any header it is given with
an include guard automatically.

The following is therefore not neccessary anymore:

    #ifndef __headername__
    #define __headername__

    //Your code goes here...

    #endif
