# Overview

Holesail can be segregated into mainly two parts, one is the **serve**r and other the **client**. When you set a port live (expose a port), you use the Holesail server, and when you connect to a Holesail server, you use a Holesail client.

## Step 1 : Share a port

Let's assume we have a react website running on localhost:8080, to share this service we need to run the following in terminal:

```
holesail --live 8080 --host localhost
```

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098304104140943/image.png?ex=6867056e&#x26;is=6865b3ee&#x26;hm=c0f8c70030796bf6ed70422f0237a448bf6a19b54b44147032b6a47bc0517b33&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=759&#x26;height=370" alt=""><figcaption></figcaption></figure>

## Step 2: Connect to the server

Now, on a different computer (or even same) copy the connection key you got from the previous step  and run:

```
holesail <key>
```

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390098730664984576/image.png?ex=686705d4&#x26;is=6865b454&#x26;hm=af79c8f01b711262703958f696247c754d5a09732909988a7cbb705cf252c64c&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>

Replacing \<key> with the key your received from Step 1.

You can also scan the QR code using Holesail Go app on your phone to connect.

## Step 3: Access the application

**You are now connected, and the port from device 1 is available on device 2.** You can now access the running application on the provided URL after "Access application on". Which is localhost:8080 in this case.

<figure><img src="https://media.discordapp.net/attachments/1232882914635681823/1390099849369751552/image.png?ex=686706de&#x26;is=6865b55e&#x26;hm=ccfa5c1cf0c866b77e4075fd686643ace15a4538f632a04874879d61588cc485&#x26;=&#x26;format=webp&#x26;quality=lossless&#x26;width=822&#x26;height=370" alt=""><figcaption></figcaption></figure>

The port details used when the host started the connection will automatically transfer along with the connection, however, if the user on device 2 wants to utilize a different port and host, they may specify a custom port using the --port and --host flag.
