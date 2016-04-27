# grubsettings-g20aj
I used these grub settings to install Debian Jessie on an asus g20aj w/ gtx970, i74790

{rm} stands for remove from default grub setting.
KO means no output at all
num lock means keyboard lights work as expected but no video is displayed - which means something, dunno not an electronic engineer over here
software rendering means software rendering
If you're not sure, just look at yboot rows - that means it worked

Settings are in chronological order. 
First manage to install nvidia drivers with the graphics card power supply plugged in, then make the changes permanent



{rm}quiet text - KO
{rm}quiet nomodeset - noboot num lock, reboot
{rm}quiet pci=nocrs - yboot software rendering
{rm}quiet pci=nocrs text - yboot software rendering
{rm}load_video {rm}quiet text - KO
{rm}load_video {rm}quiet pci=nocrs text - yboot software rendering
RECOVERY MODE
 - noboot num lock
pci=nocrs - noboot num lock
{rm}load_video - noboot num lock
{rm}load_video pci=nocrs - noboot num lock
{rm}load_video nomodeset - noboot num lock
{rm}load_video nomodeset pci=nocrs - yboot

-----------------------NVIDIA DRIVERS INSTALLED-----------------------------------

 - num lock
{rm}quiet - num lock
{rm}quiet pci=nocrs - yboot ok
