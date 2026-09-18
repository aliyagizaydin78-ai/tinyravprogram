TinyRavProgram / AUTH
README
==============================

1. WHAT IS TINYRAVPROGRAM?
------------------------------
TinyRavProgram is a small Windows program designed to run files written
in the custom AUTH scripting language.

AUTH is intentionally simple and lightweight. It is designed so that
programs can be written directly in Notepad without needing HTML, CSS,
JavaScript, Python, or another large language.

AUTH files use the extension:

    .auth


2. WHAT IS AUTH?
------------------------------
AUTH is the scripting language used by TinyRavProgram.

A basic AUTH program can look like this:

    var x = 10 ;
    var y = 5 ;

    say var-x + var-y ;

The semicolon (;) ends a command.

Variables are created with "var".

The "var-" prefix is used when referring to a variable.

The "say" command displays a result.


3. BASIC SYNTAX
------------------------------
Create a variable:

    var x = 10 ;

Create another variable:

    var y = 5 ;

Use variables:

    say var-x + var-y ;

Text can also be displayed:

    say "Hello from AUTH!" ;


4. TEXT AND VALUES
------------------------------
AUTH supports simple numeric values and text values.

Number:

    var number = 25 ;

Text:

    var name = "RavKo" ;

Display a variable:

    say var-name ;

Combine text:

    say "Hello " + var-name ;


5. WINDOWS
------------------------------
AUTH can create a simple program window.

Example:

    CreateWindow {
        W="300"
        H="300"
        TITLE="My AUTH Program"
        RESIZABLE="false"
        TRAYICON="false"
        EXTENSIONS="false"
    }

W = window width.
H = window height.
TITLE = window title.
RESIZABLE = whether the window can be resized.
TRAYICON = whether a tray icon is requested.
EXTENSIONS = enables additional AUTH interface features.


6. EXTENSIONS
------------------------------
When EXTENSIONS is enabled, interface elements such as Text and Button
can be used.

Example:

    CreateWindow {
        W="400"
        H="250"
        TITLE="AUTH Test"
        RESIZABLE="true"
        TRAYICON="false"
        EXTENSIONS="true"
    }

    Text {
        X="20"
        Y="20"
        W="350"
        H="30"
        TEXT="Hello from AUTH!"
    }

    Button {
        X="20"
        Y="70"
        W="120"
        H="30"
        TEXT="Click me"
    }


7. HOW TO USE AUTH
------------------------------
1. Open Notepad.
2. Write an AUTH program.
3. Save the file with the .auth extension.
4. Open TinyRavProgram.
5. Press "Run .auth".
6. Select the .auth file.
7. TinyRavProgram reads and interprets the AUTH commands.

The first time "Create .auth" is used, TinyRavProgram can register the
.auth file type with Windows and associate it with Notepad.

AUTH files are intended to remain editable text files.


8. TINYRAVPROGRAM SOURCE FOLDER
------------------------------
On startup, TinyRavProgram creates a folder in Documents:

    Documents\
    └── TinyRavProgram_src\
        ├── TinyRavProgram.db
        ├── README.bat
        ├── TinyRavProgram.ahk
        └── example.auth

TinyRavProgram.db contains basic program information.

README.bat is a small information batch file.

TinyRavProgram.ahk is the source code used to build the program.

example.auth is an example AUTH program.


9. EXAMPLE PROGRAM
------------------------------
The following is a complete small AUTH example:

    var name = "RavKo" ;
    var x = 10 ;
    var y = 5 ;

    say "Hello " + var-name ;
    say var-x + var-y ;

It demonstrates variables, text, numbers, and the say command.


10. HOW AUTH WAS DISCOVERED / CREATED
------------------------------
AUTH was not discovered as an existing mainstream programming language.

It was created as a custom scripting-language idea for TinyRavProgram.

The goal was to make a language that feels like a real programming
language while staying small enough to understand and write manually.

The original idea started with very simple commands such as:

    var x = 10 ;
    var y = 5 ;
    say var-x + var-y ;

From there, the language was expanded with CreateWindow and optional
interface extensions.

The name AUTH refers to the custom file and language format used by
TinyRavProgram. It is not intended to claim compatibility with another
existing AUTH language.


11. DESIGN GOALS
------------------------------
AUTH is designed around these ideas:

- Simple syntax
- Lightweight interpreter
- Easy editing in Notepad
- Small programs
- No HTML
- No CSS
- No JavaScript requirement
- No Python requirement
- Easy-to-read commands
- Custom Windows program integration


12. CURRENT LIMITATIONS
------------------------------
AUTH is currently a small interpreter rather than a full programming
language.

Only the commands implemented by the current TinyRavProgram interpreter
are supported.

Some planned language features may not work yet.

If an unsupported command is used, TinyRavProgram can show an AUTH error.

The Button extension currently uses the built-in TinyRavProgram button
handler.


13. FILE EXTENSION
------------------------------
AUTH programs use:

    .auth

Example:

    hello.auth

Windows can be configured so that .auth files open in Notepad.

TinyRavProgram can separately read and execute the AUTH code when the
"Run .auth" option is used.


14. PROJECT STATUS
------------------------------
Project: TinyRavProgram
Language: AUTH
Platform: Windows
Main source language: AutoHotkey v1
AUTH interpreter: TinyRavProgram

This project is experimental and is being developed as a lightweight
custom scripting environment.


15. QUICK START
------------------------------
Create a file named:

    hello.auth

Put this inside:

    say "Hello from AUTH!" ;

Save it.

Open TinyRavProgram.

Press:

    Run .auth

Select hello.auth.

The program should interpret the command and display the message.


==============================
End of README
TinyRavProgram / AUTH
==============================
