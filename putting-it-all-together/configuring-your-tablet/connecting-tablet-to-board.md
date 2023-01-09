# Connecting tablet to board

Ah networks... the devil's spaghetti. Don't worry - this will be a LOT easier than you think.

### Overview

Usually, you'll be in the following configuration:

Internet-based RTK provider -> mobile phone hotspot -> tablet -> AOG board

Hopefully, you can connect your phone to your tablet over a wifi hotspot, so no cables needed. You might need to USB tether it to the phone, but maybe not.

The only physical network connection that you need is via an ethernet cable from the tablet to the AOG board. Now - this is important; usually, you have to have a device known as a network switch in between them, so they both plug into the switch. If you have a machine/implement board, it would also plug into the switch, so you'd have 3 ethernet cables going to the switch.

Tablet <-> switch <-> AOG board

If you ONLY have two devices - the Tablet and the AOG board, you can do away with the switch and save some complexity by buying what's known as a "crossover ethernet cable". Crossover being the important word there - some network cards will spot when they should act accordingly in a crossover situation, but some won't, so save yourself the trouble and buy the right kind.

### Your phone/hotspot and your tablet

Your phone, when you enable the mobile hotspot feature, establishes a point of presence on the internet and creates a local network that devices can connect to, so they can use the phone as a gateway to the internet. This is how your tablet or laptop can get on the internet via your phone - your computer temporarily joins the local/private network that the phone creates and says "all chat, onto the internet please!".

To do that, your phone creates what's known as a subnet range, and allocates device that connects to it a unique address in that range. It'll be in the settings to tell you what that subnet range.

(TODO: image of phone's view of connected device)

Your phone will likely tell you what IP address it gave your tablet - and this is where the fun starts.

### Subnets and networks

Usually, a mobile hotspot will assign your device an IP similar to 192.168.X.Y, and while the first two numbers are almost certainly going to be 192.168, the last two will vary. The first three parts of the address - known as octets - form what's known as the subnet so in the example, the subnet would be 192.168.x and your tablet's unique private IP address as 192.168.X.Y.

X marks the subnet/network, Y marks the device. You with me?

So your computer is now passing traffic through the internet via your mobile hotspot.

### The (special) case for another network

However, we need to establish an additional network for AgOpenGPS and your AGO board via a physical connection, an ethernet cable. And here is where things get a little tricky. In the wifi/hotspot situation, your phone told the computer what IP address to use - it handed it what's known as an IP allocation.

When you only have two physical devices tho - the tablet and the board - there's nobody to hand out those IP addresses, to advise them what they should be. So you are going to have to configure your network card on the tablet manually. This is a one-off action, you shouldn't need to do this often.

On your tablet/laptop, click the Start button and type "ncpa.cpl". You should see something similar to the following:

![](<../../.gitbook/assets/image (6).png>)

Open that program

TODO: screenshots from tablet, how to pick a subnet, etc etc and how to tell the AOG board how to follow you to the new network
