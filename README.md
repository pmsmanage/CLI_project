# pms

password management system (pms) is a cli app to store and manage your passwords

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install pms.

```bash
pip install password-management-system
```

## User
Signup and login user to add passwords for them:
```bash
pms signup ahmad 123
pms login ahmad 123
```

don't forget to logout user after you finish so your passwords stay secure:
```bash
pms logout
```
use "pms -h" for the rest of the commands

## Password
After login you can manage your passwords:

add new password:
```bash
pms add <password> <password_name>
```
you can also use -w or --website to add a website to that password -d or --description to add description
```bash
pms add 1234 g_password -w google.com -d "gmail password"
```

you can see your all passwords by:
```bash
pms show
```
use "pms -h" for the rest of the commands

## Security
The app doesn't store user password but use a hashed version to login the user, a random secret key get generated when a user signup and it's encrypted using user password, all passwords belong to that user will get encrypted by this key.

as long as user is logged out nothing can get his passwords without the user password.

python [cryptography](https://pypi.org/project/cryptography/) package is used for encryption.


## License

[MIT](https://choosealicense.com/licenses/mit/)