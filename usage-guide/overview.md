# 😙 Overview

Holesail can be segregated into mainly two parts, one is the **serve**r and other the **client**. When you set a port live (expose a port), we call it a holesail server, and when you connect to a holesail server, we call it a holesail client.

Holesail npm version and the Holesail executable for terminal supports both holesail client and server. That means you can use the terminal version to set ports live and connect to other people.

We also have Holesail Go apps for Mac, iOS and Windows which support only connecting and you can not set a port live using them.

## Step 1 : Expose a port

Let's assume we have a react website running on localhost:80, then to expose this port we will do:

```
holesail --live 80
```

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098304104140943/image.png?ex=6867056e&#x26;is=6865b3ee&#x26;hm=c0f8c70030796bf6ed70422f0237a448bf6a19b54b44147032b6a47bc0517b33&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=759&#x26;height=370" alt=""><figcaption></figcaption></figure>

## Step 2: Connect to the server

Now, on a different computer (or even same) copy the connection string you got from the previous step  and run:

```
holesail hs://s000a19f5778ccf3b7471fd45205758ad44a572aec1e7cdf76864613db0e63b8a49c
```

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098730664984576/image.png?ex=686705d4&#x26;is=6865b454&#x26;hm=af79c8f01b711262703958f696247c754d5a09732909988a7cbb705cf252c64c&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>

You can also scan the QR code using Holesail Go app on your phone and Mac to connect.

## Step 3: Access the application

**You are now connected, and the port from device 1 is available on device 2.** You can now access the running application on the provided URL after "Access application on". Which is 127.0.0.1:80 in this case.

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390099849369751552/image.png?ex=686706de&#x26;is=6865b55e&#x26;hm=ccfa5c1cf0c866b77e4075fd686643ace15a4538f632a04874879d61588cc485&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>

The port details used when the host started the connection will automatically transfer along with the connection, however, if the user on device 2 wants to utilize a different port they may specify a custom port using the --port flag.
