Spyder - Scientific PYthon Development EnviRonment
==================================================

Copyright © 2009-2013 Pierre Raybaut
Licensed under the terms of the MIT License
(see spyderlib/__init__.py for details)


    Overview

        Spyder is a Python development environment with tons of features:
            Editor
                Multi-language editor with function/class browser, code analysis
                (pyflakes and pylint are currently supported), horizontal/verti-
                cal splitting, etc.
            Documentation viewer
                Automatically show documentation (if available, or source code
                otherwise) for any class instantiation or function call made
                in a Python shell (interactive/external console, see below)
            Interactive console
                Python shell with workspace support (variable explorer with GUI
                based editors: dictionary editor, array editor, ...) and
                matplotlib figures integration
            External console (separate process)
                Run Python scripts (interactive, debugging or normal mode) or
                open a Python interpreter with variable explorer and documenta-
                tion viewer support (a basic terminal window may also be opened
                with the external console)
            File/directories explorer
            Find in files feature
                Supporting regular expressions and mercurial repositories
            History log

        Spyder may also be used as a PyQt4 extension library (module 'spyderlib').
        For example, the Python interactive shell widget used in Spyder may be
        embedded in your own PyQt4 application.

    Build dependencies

        When installing Spyder from the .zip source package (using the 
        command `python setup.py install`), the only requirements is:
            Python 2.5+

    Runtime dependencies
    
        Python 2.5+
        PyQt4 4.4+ or PySide 1.1.1+ (PyQt4 is recommended)
            
        Recommended modules
            rope v0.9.2+ (editor code completion, calltips and go-to-definition)
            pyflakes v0.5.0+ (real-time code analysis)
            sphinx v0.6+ (object inspector's rich text mode)
            numpy (N-dimensional arrays)
            scipy (signal/image processing)
            matplotlib (2D/3D plotting)
	    
        Optional modules
            IPython 0.13 (enhanced Python interpreter)
                On Ubuntu you need to install ipython-qtconsole, on Fedora
                ipython-gui and on Gentoo ipython with the qt4 USE flag.
            pygments (syntax highlighting for MATLAB, batch and ini files)
            pylint (powerful code analysis)
            pep8 (style analysis)

    Running from source
      
        It is possible to run Spyder directly from unpacked source folder 
        using Spyder's bootstrap script:

            `python bootstrap.py`

        This is especially useful for beta-testing, troubleshooting 
        and development of Spyder itself.

    Installation
    
        This section explains how to install the latest *stable* release of 
        Spyder. If you prefer testing the development version, please use 
        the bootstrap script (see previous section).
        
        From the source package (see section 'Building dependencies'), you may 
        install Spyder using the integrated setup.py script based on Python 
        standard library `distutils` with the following command:

            `python setup.py install`

        Note that `distutils` does *not* uninstall previous versions of Python 
        packages: it simply copies files on top of an existing installation. 
        When using this command, it is thus highly recommended to uninstall 
        manually any previous version of Spyder by removing the associated 
        directories ('spyderlib' and 'spyderplugins' in your site-packages 
        directory).

        From the Python package index, you may simply install Spyder *and* 
        upgrade an existing installation using `pip`:
        http://pypi.python.org/pypi

        But the easiest way to install the last stable release of Spyder is:
            * on Windows:
                * using an executable installer: http://spyderlib.googlecode.com
                * or through Python(x,y): http://pythonxy.googlecode.com
            * on Mac OSX:
                * using our DMG installer: http://spyderlib.googlecode.com
                * Using the Anaconda Python Distribution: https://store.continuum.io/cshop/anaconda/
                * through MacPorts 
            * on GNU/Linux, through your package manager
        For more details on supported platforms, please go to http://spyderlib.googlecode.com.

    Build Windows installers

        From the source package, you may build Windows installers to distribute
        Spyder on all supported platforms and versions of Python.
        Spyder has a single code base supporting both Python 2 and Python 3 but
        the Windows installer will target a specific version of Python because 
        of the two external libraries included in the Windows installers 
        ('pyflakes' and 'rope') which have specific versions for Python 3. 
        Moreover, despite the fact that Spyder code base supports all Python 
        architectures (32 and 64bit), the Windows installers will also target 
        specific architectures because of a limitation of the way distutils 
        works (see http://bugs.python.org/issue6792).

        Example of Spyder binary installers for Windows:
            * Python 2.7 and 32bit: spyder-2.3.0-win32-py2.7.exe
            * Python 2.7 and 64bit: spyder-2.3.0-win-amd64-py2.7.exe
            * Python 3.3 and 32bit: spyder-2.3.0-win32-py3.3.exe
            * Python 3.3 and 64bit: spyder-2.3.0-win-amd64-py3.3.exe

    More informations
    
        Downloads, bug reports and feature requests:
            http://code.google.com/p/spyderlib/
        Discussions:
            http://groups.google.com/group/spyderlib