# Python documentation 

My journey of reverse engineering of a program written in Python.

## Setup.cfg
> Providing a configuration file, setup.cfg, for users to edit is a cheap and easy way to solicit it. Configuration files also let you provide default values for any command option, which the installer can then override either on the command-line or by editing the config file.

```
[metadata]
name = PkgName
version = 1.1.1.1
author = Authors Name
author_email = authorsName@email.com
description = Pkg purpose
long_description = file: README.md
long_description_content_type = text/markdown
url = https://github.com/almenscorner/PkgName
project_urls =
    Bug Tracker = https://github.com/almenscorner/PkgName/issues
classifiers =
    Programming Language :: Python :: 3
    License :: OSI Approved :: MIT License
    Operating System :: OS Independent

[options]
package_dir =
    = src
packages = find:
python_requires = >=3.6
install_requires =
    deepdiff>=5.6.0
    pyyaml>=6.0
    adal>=1.2.7
    msrest>=0.6.21
    markdown_toclify>=0.1.7
    pytablewriter>=0.64.1

[options.packages.find]
where = src

[options.entry_points]
console_scripts =
    PkgName-functionDoSomething1 = PkgName.run_function1:start
    PkgName-functionDoSomething2 = PkgName.run_function2:start
    PkgName-functionDoSomething3 = PkgName.run_function3:start
```

> On the script file, we will just need to add at the end of the file for setup.cfg to call:
```
if __name__ == "__main__":
    start()
```

## Modules 

### argparser

The argparse module makes it easy to write user-friendly command-line interfaces. The program defines what arguments it requires, and argparse will figure out how to parse those out of sys.argv. The argparse module also automatically generates help and usage messages. The module will also issue errors when users give the program invalid arguments.

```
parser = argparse.ArgumentParser(
                    prog = 'ProgramName',
                    description = 'What the program does',
                    epilog = 'Text at the bottom of help')

parser.add_argument('filename')           # positional argument
parser.add_argument('-c', '--count')      # option that takes a value
parser.add_argument('-v', '--verbose',
                    action='store_true')  # on/off flag

args = parser.parse_args()
print(args.filename, args.count, args.verbose)
```

> It's like writing a command line function that takes args in Windows.


## Custom Modules

### makeapirequest




## 


