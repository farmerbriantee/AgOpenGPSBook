# Assembling the board

So, the mail/post/delivery has arrived, you've opened the box and reality has hit home. No going back now.

First, let's see what you might typically have received in your post from JLCPCB. Here's a sample micro as it came out of the packet (as you can see, this one had quite a few parts in stock at JLC when it was built, as such not a lot were missing):

![](<../../.gitbook/assets/image (11).png>)

The parts ringed in red where things that this board required. Top two are LEDs, the 3-pin in the centre was the 7803 voltage regulator, the two circles on the right were two 1uf capacitors and also had to solder the 12V line as this one was going to be sending 12V out rather than 24V.

So, that was taken care of, and:

![](<../../.gitbook/assets/image (1).png>)

Two jumpers were also needed to link up the left and right outputs of the Cytron to the connector on the edge of the board:

![](../../.gitbook/assets/image.png)

Now... your mileage may vary here - obviously it's difficult to decipher what all is missing when you don't know, but going on the above, all that was needed to get this board working was a loom, the Teensy, the Micro GPS modules and the Cytron.

The eagle-eyed will notice that leaves a lot of bits with nothing in them - and that's because it was for things or features I wasn't needing. The PCB layout will help identify what some areas are used for (the part at bottom left is for an XBee radio for example), but if you're unsure, compare your board with the above, take a photo, and ask questions in Discourse or Telegram at the below location:

{% content-ref url="../../frequently-asked-questions/frequently-asked-questions/help-i-need-to-speak-to-someone.md" %}
[help-i-need-to-speak-to-someone.md](../../frequently-asked-questions/frequently-asked-questions/help-i-need-to-speak-to-someone.md)
{% endcontent-ref %}

TODO: what pieces you can do without, changes you need to make (solder the supply line, jumpers etc), fitting the Teensy, the
