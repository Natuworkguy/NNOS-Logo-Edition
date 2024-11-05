# NNOS Logo Edition

**NNOS Logo Edition** is a lightweight program written in the **Logo programming language**, designed to make Logo easier and more accessible for users of all skill levels. The current codebase, while small, is structured for future expansion, offering enhanced usability and interactive features that will grow with time.

This edition introduces an animated startup and an intuitive interface, built to help users experience the versatility of Logo. Whether you're a beginner or an experienced Logo programmer, NNOS Logo Edition provides tools that make coding in Logo simpler and more fun.

## Features

- **Animated Startup**: A smooth, animated splash screen that displays "NNOS" based on your selected screen size.
- **Simplified Logo Procedures**: Easy-to-understand commands for beginners, with flexibility for future enhancements.
- **Future-Proof Design**: The codebase is modular and ready to expand with additional features and improved performance.

## Future Plans

NNOS Logo Edition will continue to grow in future updates. Planned features include:

- **More Drawing Utilities**: Advanced shapes and functions for complex drawings.
- **Interactive Features**: GUI enhancements that allow users to interact with Logo visually.
- **Learning Modules**: Built-in tutorials to help new users learn Logo while using NNOS.
- **Optimized Performance**: Speed improvements and reduced memory usage to enhance user experience.

## Installation & Setup

To run NNOS Logo Edition, follow these steps:

1. **Install a Logo Interpreter**: 
   - Ensure you have a compatible Logo interpreter such as [UCBLogo](https://people.eecs.berkeley.edu/~bh/logo.html) or [FMSLogo](https://fmslogo.sourceforge.io/).
   
2. **Download the Code**:
   - Clone this repository to your local machine:
     ```bash
     git clone https://github.com/YourUsername/NNOS-Logo-Edition.git
     ```

3. **Run the Program**:
   - Open your Logo interpreter and load the `NNOS.lgo` file.
   - Start the NNOS procedure by typing the following command:
     ```logo
     NNOS
     ```
   This will trigger the starting animation for medium-sized screens.

## Code Example

Here is the main Logo code used in NNOS Logo Edition:

```logo
TO STARTINGANIMATION :SCREENSIZE
  MAKE "DOANIMATION "TRUE
  IFELSE (:SCREENSIZE = "S) [
    MAKE "LSP 46
  ][
    IFELSE (:SCREENSIZE = "M) [
      MAKE "LSP 82
    ][
      IFELSE (:SCREENSIZE = "L) [
        MAKE "LSP 118
      ][
        MAKE "DOANIMATION "FALSE
        PRINT [INVALID VALUE FOR SCREENSIZE]
      ]
    ]
  ]
  IF (:DOANIMATION = "TRUE) [ 
    CS WINDOW HIDETURTLE
    REPEAT :LSP [
      SETLABELHEIGHT REPCOUNT
      PU
      FD REPCOUNT * REPCOUNT / 30
      LABEL "NNOS
      BK REPCOUNT * REPCOUNT / 30
      PD
      RT 10
      WAIT 5
    ]
    ST
    WAIT 30
    CS
  ]
END

TO NNOS
  STARTINGANIMATION "M
END
```

This code defines a `STARTINGANIMATION` procedure that displays an animated "NNOS" logo on the screen based on the screen size. Users can adjust the screen size by providing the `"S"`, `"M"`, or `"L"` argument for small, medium, or large screen sizes respectively.

## Usage

Once you've executed the `NNOS` procedure, the startup animation will play for a medium-sized screen (`"M"`). You can customize the experience by modifying the input to the `STARTINGANIMATION` procedure to fit different screen sizes.

- Small: 
  ```logo
  STARTINGANIMATION "S
  ```
- Large: 
  ```logo
  STARTINGANIMATION "L
  ```

## System Requirements

- **Operating System**: Any operating system that supports Logo interpreters (e.g., Windows, macOS, Linux).
- **Logo Interpreter**: Compatible with popular Logo interpreters like UCBLogo or FMSLogo.
- **Memory**: NNOS Logo Edition requires minimal memory to run, suitable for any modern system.

## Contributing

Contributions are welcome! If you'd like to contribute to the development of NNOS Logo Edition, here’s how you can help:

1. **Fork the Repository**: Create your own copy of the project by clicking "Fork" in the top right.
2. **Create a New Branch**: Make changes in a feature branch.
   ```bash
   git checkout -b feature-branch-name
   ```
3. **Submit a Pull Request**: Once you've tested your changes, submit a pull request to the main repository.

We welcome improvements, bug fixes, and new feature ideas! Be sure to document your changes clearly and keep the code modular.

## License

NNOS Logo Edition is licensed under the **Apache License 2.0**. You are free to use, modify, and distribute this software under the conditions of the license. See the full license text below.
