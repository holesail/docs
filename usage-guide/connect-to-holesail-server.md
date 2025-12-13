# Connect to Holesail server

Run the following command to connect to a Holesail server instance:

```
holesail <KEY>
```

Supported options:

| Option    | Purpose                                           | Required / Optional            |
| --------- | ------------------------------------------------- | ------------------------------ |
| \<key>    | Connect to a holesail server                      | Required                       |
| --connect | Similar to doing holesail KEY\_STRING             | Optional                       |
| --host    | Bind to a custom host                             | Optional. Default is 127.0.0.1 |
| --port    | Specify a custom port to use on the local machine | Optional. Default is port 8989 |
| --log     | Start debug logging                               | Optional.                      |

<mark style="color:orange;">Examples:</mark>

1. Connect to a Holesail server with default options:

```
  holesail hs://s000a19f5778ccf3b7471fd45205758ad44a572aec1e7cdf76864613db0e63b8a49c
```

2. Connect to a Holesail server with a custom key and custom port:

```
  holesail my-custom-connection --port 8080
```

3. Connect to a Holesail server and listen on a custom port and host:

```
holesail "my-connection-key" --port 8765 --host localhost
```

4. Start a holesail server with custom connection string and its smaller than 32 characters:

```
holesail --live 4545 --key "its-quite-small" --force
```

You can use multiple flags as per your need. Once you are connected, you can access the running application on the host and port you specified before.

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098730664984576/image.png?ex=686705d4&#x26;is=6865b454&#x26;hm=af79c8f01b711262703958f696247c754d5a09732909988a7cbb705cf252c64c&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>
