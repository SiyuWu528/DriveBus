# EyesNhand: A module to simulate the movement of eyes and hands

## Requirement:

You first are going to need to install the requirements. Installation of the requirements require the following code on the command prompt:

```
pip install -r requirements.txt
```

## Getting Started

You may first open the file "GettingStarted.py". First, you will be asked to identify the environment you are going to use for your problem. You are required to click twice, as you click once, there will be a black box originating from that point to where you mouse is. You will need to make sure that the black box includes the whole environment. After that you are asked to identify you visual modules within the environment. The process in the same as defining the environment the only difference is that instead of being able to chose any part of the screen, you are limited to the environment you defined in earlier. You will need to name these items in a way that you'd be able to recall them later to use them. After that, you will need to define feedback modules but for this one, since sometimes, the environment changes based on the goal, you will be offered to use the whole screen again to identify your feedback moduels. And then you can save the files or just close and start again.



The main file is "EyesNhand.py". In order to run the file on command prompt, you will need three argument which two of which are optional. The first argument is the function which you want to use. The options for this argument are one of the following:

- "**click**": Will simulate the action of right clicking. It gets no argument.
- "**Keypress**": Will simulate the action of a Keypress. It will get a argument: 
  - --arg2 which is going to be the key you want the computer to press.
- "**movecursorto**": Will simulate the movement of the mouse to a specific part of the screen. It will get an argument :
  -  --arg2 which is going to be the "x" and "y" values separated by a space
- "**whatisonscreen**": Will check if any of the modules given can be found in that moment. It will get two argument: 
  - --Dir: Directory of where the visual modules are defined.
  - --arg2: The visual modules that you want to look for. Each separated by a space
- "**getMouseLocation**": Gets the location of the mouse. It gets no argument.
- "**whereis**": Will find where a module is located. It will get two argument: 
  - --Dir: Directory of where the visual modules are defined.
  - --arg2: The visual modules that you want to look for.
- "**movecursortopattern**": Will simulate the movement of the mouse to a specific pattern on the screen. It will get two argument: 
  - --Dir: Directory of where the visual modules are defined.
  - --arg2: The visual modules that you want to look for.

To run the program, your request has to have the following format:

```
python Visitor (The function you want to use) --Dir (Directory) --arg2 (the second argument)
```

For example, for running "*movecursortopattern*" with all the arguments, we have a code similar bellow

```
python Visitor movecursortopattern --Dir Directory/to/where/you/want --arg2 SignInBotton
```

## Calling from Common lisp

Even though the code is written in python, it is accessible from any programming language by accessing the command prompt and writing the correct code. In this part, we are going to talk about how to run this code on Common lisp (CLISP):

### Loading inferior-shell

You can load the inferior-shell in the slime by the following code 

```commonlisp
(ql:quickload 'inferior-shell)
```

Then with the inferior-shell loaded, we can write the following code:

```commonlisp
(inferior-shell:run/ss '("python" "C:/Route/To/The/Directory/Visitor.py" "Function" "--Dir" "Directory" "--arg2" "arg2 values each inside a quotation" ))
```

