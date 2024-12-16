Usage: gam <command> [arguments]

Commands:
  init                                 Creates the credentials.json file in the config path.
  register <account>                   Register a new account with the specified ID.
                                       Prompts for name, email, username, password, and other settings.

  get <account>                        Display the details of a registered account.

  list                                 List all registered account IDs.

  set-name <account> <name>            Update the name of the specified account.

  set-email <account> <email>          Update the email address of the specified account.

  set-username <account> <username>    Update the username of the specified account.

  set-password <account> <password>    Update the password or key of the specified account.

  set-signingkey <account> <key>       Update the signing key for the specified account.

  set-gpg-format <account> <format>    Update the GPG format (e.g., 'ssh', 'gpg') for the specified account.

  set-config <account> <key> <value>   Add or update a custom configuration key-value pair for the account.
                                       Example: set-config my_account push.autoSetupRemote true

  apply <account>                      Apply the Git configuration (e.g., name, email, signingkey) of the specified account
                                       to the current Git repository.

  add-remote <account> <URL>           Add a Git remote URL with embedded credentials from the specified account.
                                       The username and password from the account are inserted into the URL.
                                       Updates the 'origin' remote of the current Git repository.

Examples:
  gam register my_account              Register a new account with the ID 'my_account'.
  gam set-name my_account 'John Doe'   Update the name for the account 'my_account'.
  gam get my_account                   Show details for the account 'my_account'.
  gam apply my_account                 Apply 'my_account' configuration to the current Git repository.
  gam add-remote my_account https://github.com/user/repo.git
                                       Add a remote URL for 'my_account' to the current Git repository.

Note: Ensure the credentials.json file exists and contains valid configurations.
