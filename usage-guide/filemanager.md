# Filemanager

Holesail file manager let's you share files and folders with anyone and across devices with a single command.

There are no restrictions on the number of files that can be shared, the bandwidth or the size of the file.

**Command:**

```
holesail --filemanager
```

Supported options:

| Option             | Purpose                                                                            | Required / Optional                      |
| ------------------ | ---------------------------------------------------------------------------------- | ---------------------------------------- |
| --filemanager      | Start file manager in current directory                                            | Required                                 |
| --filemanager PATH | Start file manager in the given directory                                          | Optional                                 |
| --username         | Set a custom username for authentication                                           | Optional. Default is admin               |
| --password         | Set a custom password                                                              | Optional. Default is admin               |
| --role             | Allow a user to create folder and files by setting role to **admin**               | Optional. Default is "user".             |
| --connector        | Set a custom connection string. Can not be less than 32 chars or equal to 64 chars | Optional. The default is auto-generated. |
| --force            | Bypass custom connection string length limit                                       | Optional. Default is false               |

<mark style="color:orange;">Examples:</mark>

1. Start a filemanager session in the current directory with default username and password:

```
holesail --filemanager
```

2. Start a filemanager session in a custom directory with custom username:

```
holesail --filemanager "/Users/supersu" --username "holesail"
```

3. Start a filemanager session in a custom directory with custom username and password and admin role:

```
holesail --filemanager "/Users/supersu" --username "holesail" --password "securepass@99#123" --role admin
```

You can combine multiple options according to your needs. You will get a connection string and QR code that you can use to connect with Holesail filemanager and access in the browser.
