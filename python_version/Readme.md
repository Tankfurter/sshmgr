# SSH Manager (`sshmgr`)

`sshmgr` is a Python-based command-line tool designed to manage SSH server configurations effectively. It enables users to store, retrieve, and manage SSH connection details using an SQLite database. The tool also supports importing SSH configurations from the standard `~/.ssh/config` file and allows for easy searching of servers based on various attributes.

## Features

- **List Servers**: Display a list of all stored SSH server configurations.
- **Add Server**: Interactively add a new server entry to the database.
- **Delete Server**: Remove a server entry from the database using its alias.
- **Connect to Server**: SSH into a server using stored connection details.
- **Import from SSH Config**: Import server configurations from the `~/.ssh/config` file, avoiding duplicates.
- **Search Servers**: Search for servers by alias, hostname, environment, or description.
- **Help Menu**: Display usage information and examples for easy reference.

## Requirements

- Python 3.x
- `tabulate` library for formatted table output

### Install `tabulate`:

```bash
pip install tabulate
```

## Installation

1. **Clone the Repository**:

```bash
git clone https://github.com/yourusername/sshmgr.git
cd sshmgr
```

2. **Make the Script Executable**:

```bash
chmod +x sshmgr
```

1. **Add to PATH (Optional)**:

   For easier access, add the directory containing `sshmgr` to your system's `PATH`, or move the script to a directory already in your `PATH`.

## Usage

Run the script with the appropriate command-line flags:

### List Servers

```bash
./sshmgr --list
```

### Add a New Server

```bash
./sshmgr --add
```

### Delete a Server

```bash
./sshmgr --delete
```

### Connect to a Server by Alias

```bash
./sshmgr --connect <alias>
```

### Import Servers from SSH Config

```bash
./sshmgr --import-config
```

### Search for Servers

```bash
./sshmgr --search <query>
```

### Display Help Menu

```bash
./sshmgr --help
```

## Examples

- **Add a New Server**:
```bash
./sshmgr --add
```
  Follow the interactive prompts to input server details.

- **Connect to a Server**:
```bash
./sshmgr --connect myserver
```
  Connects to the server with alias `myserver`.

- **Import SSH Configurations**:
```bash
./sshmgr --import-config
```
  Imports SSH hosts from the user's SSH config file (`~/.ssh/config`).

- **Search for Servers**:
```bash
./sshmgr --search production
```
  Searches for servers containing the term "production" in their details.

## Contributing

Contributions are welcome! Feel free to fork the repository and submit a pull request with your improvements or new features.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Python](https://wwwthon.org/)
- [SQLite](https://www.sqlite.org/)
- [tabulate](https://pypi.org/project/tabulate/)

---

Enjoy managing your SSH connections with `sshmgr`!
