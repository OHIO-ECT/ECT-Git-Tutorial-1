# ECT Git Guide

## Goals 

- Authenticate command line git to GitHub.

## Toolkit 

- Any Linux based computer with command line git.

## Process

1. Deploy the GitHub command line application and authenticate the local unix account to the GitHub account.

```sudo apt install gh```

2. Setup authentication with the command line tool.

```gh auth login```

3. Follow the following prompts

4. Select GitHub.com

```? What account do you want to log into?  [Use arrows to move, type to filter]
> GitHub.com
  GitHub Enterprise Server
```

5. Select SSH

```
? What is your preferred protocol for Git operations?  [Use arrows to move, type to filter]
  HTTPS
> SSH
```

6. Enter Y to enter a new key.  n to not generate a key or selecting a key if one is presented are also options, but requires the user to understand the consequences of advanced key management.

```
? Generate a new SSH key to add to your GitHub account? (Y/n) Y
```

7. It is suggested to use a proper passphrase here.

```
? Enter a passphrase for your new SSH key (Optional)
```

8. Select the Login with a web browser regardless of the type of terminal these commands are being entered in.

```
? How would you like to authenticate GitHub CLI?  [Use arrows to move, type to filter]
>  Login with a web browser
   Paste an authentication token
```

9. The open browser prompt will only work in certain contexts.  If it doesn't present a web browser to login to github at browse to the following URL on any computer that is already logged into on GitHub: https://github.com/login/device  Enter the one-time code and select "Authorize github"

```
The Enter to open github.com in your browser...  
```

10. Return to GitHub SSH keys page at https://github.com/settings/keys.  Find the key titled "GitHub CLI" with a recent added date.  Select the "Configure SSO" dropdown and then select "Authorize" for OHIO-ECT.

11. Follow the Ohio University Single sign on process

12. Configure Git user info with the following commands
```
git config --global user.email "<OHIO_EMAIL>"
git config --global user.name "<FIRSTNAME> <LASTNAME>"
```

13. Initial Repo clones are done with gh.  For example:
```
gh repo clone OHIO-ECT/ITS-4900-SDx-HW-02
```

14. The resulting Git repo can be manipulated with standard git commands and workflows.
