# Password Strength Analyzer

A simple yet effective Python command-line tool that evaluates the strength of a password based on common security best practices. It checks for length, character diversity, and the presence of special characters, then provides instant feedback to help users create stronger, more secure passwords.

## Overview

Weak passwords are one of the leading causes of account compromise. This project was built to help users understand what makes a password strong by analyzing it against a set of well-established security criteria and returning clear, actionable feedback in real time.

The tool runs directly in the terminal, prompting the user to enter a password and immediately displaying whether it is Weak, Medium, or Strong, along with a specific reason if it falls short.

## Features

- Checks minimum password length (at least 8 characters)
- Verifies the presence of at least one digit
- Verifies the presence of at least one uppercase letter
- Verifies the presence of at least one lowercase letter
- Checks for special characters (e.g. !, @, #, $, %, etc.)
- Returns a clear strength rating: Weak, Medium, or Strong
- Provides specific, actionable feedback on what is missing
- Interactive loop that allows continuous password checks until the user chooses to exit

## How It Works

The core logic lives in the `check_password_strength()` function, which validates a password against a series of conditions in order:

1. Length check – rejects passwords under 8 characters
2. Digit check – ensures at least one numeric character is present
3. Uppercase check – ensures at least one capital letter is present
4. Lowercase check – ensures at least one lowercase letter is present
5. Special character check – uses a regular expression to detect symbols

If a password passes all the above checks, it is classified as Strong. If it passes the basic checks but lacks special characters, it is classified as Medium. If it fails any of the fundamental checks, it is classified as Weak, along with the specific reason.

The `password_checker()` function handles user interaction, running a loop that repeatedly prompts for password input and displays the result, until the user types "exit" to quit.

## Requirements

- Python 3.x
- No external libraries required (uses only the built-in `re` module)

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/lalabha96/password-strength-analyzer.git
   ```
2. Navigate into the project directory:
   ```
   cd password-strength-analyzer
   ```
3. Run the script:
   ```
   python Password_Strength_Analyzer.py
   ```

## Usage

Run the script from your terminal, then enter any password when prompted. The tool will analyze it and print the strength rating along with feedback.

Example session:

```
Welcome to the Password Strength Checker!

Enter your password (or type 'exit' to quit): abc123
Weak: Password must include at least one uppercase letter.

Enter your password (or type 'exit' to quit): Abcdef1
Medium: Add special characters to make your password stronger.

Enter your password (or type 'exit' to quit): Abcdef1!
Strong: Your password is secure!

Enter your password (or type 'exit' to quit): exit
Thank you for using the Password Strength Checker! Goodbye!
```

## Project Structure

```
password-strength-analyzer/
│
├── Password_Strength_Analyzer.py   # Main script containing the password checking logic
└── README.md                        # Project documentation
```

## Future Improvements

- Add a graphical user interface (GUI) using Tkinter
- Add a password strength meter/score (e.g. 1 to 5) instead of just three categories
- Check passwords against a list of commonly used or breached passwords
- Add support for checking password strength without displaying the input on screen (masked input)
- Allow customizable strength criteria (e.g. minimum length, required character types)

## Contributing

Contributions are welcome. If you would like to improve this project, feel free to fork the repository, make your changes, and submit a pull request.

## License

This project is open source and available for anyone to use, modify, and distribute.

## Author

Created as a personal Python project to practice string manipulation, regular expressions, and building simple interactive command-line tools.
