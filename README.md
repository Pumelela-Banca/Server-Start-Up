# Server-Start-Up
# User Creation Script

## Description

This Bash script automates the process of creating a new user on a Linux system. It allows you to specify a username and optionally a password. If no password is provided, it sets a default password and forces the user to change it on first login.

## Features

- Creates a new user with a home directory
- Sets a password for the new user
- Uses a default password if none is provided
- Forces password change on first login when using the default password
- Checks if the user already exists before attempting to create

## Requirements

- Linux operating system
- Root privileges (script must be run with sudo)

## Usage

1. Make the script executable:
   ```
   chmod +x create_user
   ```

2. Run the script with sudo:
   - To create a user with a specified password:
     ```
     sudo ./create_user.sh <username> <password>
     ```
   - To create a user with the default password:
     ```
     sudo ./create_user.sh <username>
     ```

   Example:
   ```
   sudo ./create_user.sh john password123
   ```

## Arguments

1. `<username>` (required): The name of the user to create
2. `<password>` (optional): The password for the new user
   - If not provided, the default password "changeme" will be used

## Behavior

- If the specified user already exists, the script will notify you and take no action.
- If no password is provided, the script will:
  1. Set the default password "changeme"
  2. Force the user to change the password on first login

## Security Notes

- Passing passwords as command-line arguments can be a security risk. In a production environment, consider more secure methods of setting passwords.
- Always use strong, unique passwords.
- Be cautious when creating users, especially on production systems.
- This script is for demonstration purposes and may need additional security measures for use in a production environment.

## Customization

You can modify the script to add additional features or change its behavior:
- Add password strength validation
- Specify additional user properties (e.g., groups, shell)
- Implement logging for auditing purposes

## Troubleshooting

If you encounter issues:
1. Ensure you're running the script with root privileges (sudo)
2. Check that the username doesn't already exist on the system
3. Verify that you have permission to create new users

## Contributing

Feel free to fork this script and submit pull requests for any improvements or additional features you develop.

## License

This script is provided "as is", without warranty of any kind. Use at your own risk.
