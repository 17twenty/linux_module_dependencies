linux_module_dependencies
=========================

Two simple drivers that provide and consume an exported symbol.

Export your symbols using EXPORT_GPL_SYMBOL or EXPORT_SYMBOL as normal.

Build your provider module as normal - and take a look at the Module.symvers 
file as we're going to depend on what it exports - the Makefile contains the 
magic part.

Your dependent module will now need a makefile that uses KBUILD_EXTRA_SYMBOLS 
in order to reference these additional symbols

