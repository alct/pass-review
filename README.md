# Password Store Review

Password Store Review is a [pass](https://www.passwordstore.org/) utility for manually inspecting password stores. It provides a table consisting of logins and cleartext passwords (only the first line is retrieved).

## Installation

```bash
wget -O ~/pass-review https://raw.githubusercontent.com/alct/pass-review/master/pass-review
chmod +x ~/pass-review
sudo ln -s ~/pass-review /usr/local/bin/pass-review
export PATH=$PATH
```

## Usage

```
Usage:
  pass-review [<path/to/.password-store>]
  pass-review [-h | --help]
  pass-review [-V | --version]

Options:
  -h, --help    Print this help message and exit
  -V, --version Print version and copyright information and exit

Description:
  Used without option or argument, pass-review tries to open the store located at /home/$USER/.password-store
```

## Example

Given the following password store located at `/home/user/.password-store`:

```
Password Store
├── bar
│   └── jane@example.com
├── baz
├── foo
│   └── john
└── qux
    └── example
```

```
user@computer: pass-review
Review Password Store located at /home/user/.password-store
bar/jane@example.com    super password
baz                     another super password
foo/john                1234
qux/example             yet another password
```

## License

[GPLv3](LICENSE)
