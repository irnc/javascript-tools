# How to configure WebStorm to use JSCS

Starting from menu, go to _File > Settings... > Languages & Frameworks > JavaScript > Code Quality Tools > JSCS_.

1. _Enable_
1. Set _Node interpreter_ to the one used to run project, e.g. `C:\Program Files\nodejs\node.exe`
1. Set _JSCS package_ to `jscs` package directory under your project, e.g. `C:\Users\_user_\_project_\node_modules\jscs`
1. Select _Search for config(s)_
1. Click _OK_, from now on WebStorm will check your code style based on project configuration (as defined in `.jscsrc`) in real time as you type.

## My project does not depend on `jscs`

It is a bad practice to not enforce code style. You project should start depend on `jscs`.

In case you depend on `grunt-jscs`, point _JSCS package_ to `jscs` directory inside it.

## Should I use global `jscs` instead of local one?

It is prefferable to use local `jscs` version, as it is used for checks in CI builds.
