# 🤝 Connect to someone

It is quite easy to connect to someone running holesail:

```
holesail <KEY>
```

Supported options:

| Option    | Purpose                                           | Required / Optional            |
| --------- | ------------------------------------------------- | ------------------------------ |
| \<key>    | Connect to a holesail server                      | Required                       |
| --connect | Similar to doing holesail KEY\_STRING             | Optional                       |
| --host    | Listen on a custom host                           | Optional. Default is 127.0.0.1 |
| --port    | Specify a custom port to use on the local machine | Optional. Default is port 8989 |

<mark style="color:orange;">Examples:</mark>

1. Connect to a Holesail server with default options:

```
  holesail hs://s000a19f5778ccf3b7471fd45205758ad44a572aec1e7cdf76864613db0e63b8a49c
```

2. Connect to a Holesail server with a custom key and custom port:

```
  holesail my-custom-connection-key-that-I-will-not-share --port 8080
```

3. Connect to a Holesail server and listen on a custom port and host:

```
holesail "my-connection-key" --port 8765 --host localhost
```

4. Start a holesail server with custom connection string and its smaller than 32 characters:

```
holesail --live 4545 --key "its-quite-small" --force
```

You can combine multiple options according to your needs. After executing any of the command above, you will be connected. To see the content visit the  url that terminal shows you after "Access application on"

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098730664984576/image.png?ex=686705d4&#x26;is=6865b454&#x26;hm=af79c8f01b711262703958f696247c754d5a09732909988a7cbb705cf252c64c&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>
