## kcdecrypt
OSX Keychain Decrypt Utility - Written in pure C

Currently supported Keychain-DataTypes:
`GENERIC_PASSWORD`
`INTERNET_PASSWORD`

### Usage:
```
User Keychain
	./kcdecrypt -u [options]

	Options: -P <path_to_userkc> [-e] [-t <token_dir>] -p <user_password> [-o <out_dir>] [-v[v]]

	-P: Likely in '{User}/Library/Keychains/login.keychain-db'
	-e: If the decrypted Sqlite3 DB should be saved in <out_dir>
	-t: Likely '{User}/Library/Application\ Support/iCloud/Accounts'
	-p: User Login-Password or custom keychain if changed
	-e: Directory, where the data should be saved. Required if '-e' or '-t' used.
	-v: Get Verbose log. Use '-vv' for even more verbose log.

System Keychain (not implemented yet)
	./kcdecrypt -s [options]

iCloud Keychain (not implemented yet)
	./kcdecrypt -c [options]
```

Binary is compiled for `Mach-O X86_64`(MacOS)

### Changelog:
1.1: Added option to create iCloud MME-Tokens
1.0: Initial Release
