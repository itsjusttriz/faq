# Creating an Instance

This guide is to try to help creating instances easier for those using the AMP panel.

## Table of Contents
1. [Step 1](#step-1)
2. [Step 2](#step-2)
3. [Step 3](#step-3)
4. [Step 4](#step-4)
5. [Step 5](#step-5)

---

## Step 1
Using the image below as a reference, you need to hit the **blue** `Create Instance` button within the top navbar of the site.

<img width="1915" height="961" alt="image" src="https://github.com/user-attachments/assets/7d8ca786-2b37-468c-a92e-a0332416fcaf" />

> [!NOTE]
> If you have enabled sorting with `Group by group name`, then you may click on **any** of the `Create Instance` buttons available. While you cannot manage the groups in which an instance is located, a Super Admin can change this later on.

## Step 2
As shown below, you can now configure the basic needs for your instance.

<img width="834" height="463" alt="image" src="https://github.com/user-attachments/assets/8a8c579e-d383-423c-b50f-fcc7ec4d65a1" />

- Select the game, that this instance will be running. This allows AMP to setup the default config for you to edit later.
- Choose a custom name to help identify your new instance on the panel.
- Once youve completed both mentioned above, hit "Create Instance" on the bottom of the popup.

## Step 3

Once created, youll see your new creation sittig neatly inline with the others. **BUT**, it is in an "idle" state. 
So double click the bar itself, or click the lil square on the far right surrounded in a green outline.

<img width="1621" height="112" alt="image" src="https://github.com/user-attachments/assets/6fa71737-b3c8-453e-a200-2ff8ce08e161" />

This should bring you to that instance's own "panel", so to speak. From here, you can meddle to your hearts content, as you would on any other Server Hosting provider.

## Step 4

The Orange square is where you will find the Start/Stop/Kill/Restart buttons. Pretty self-explanatory.

The Yellow square is where youre going next.

<img width="1180" height="691" alt="image" src="https://github.com/user-attachments/assets/0831aaa7-d308-455f-8e14-ef4882a14ebd" />

Inside `Your Instance -> Configuration -> Minecraft` you will the simple setup options for building a server, such as RAM allocation, Java versioning, other general `server.properties` options.

- Inside `Java and Memory`
  - Start by setting the RAM allocation to 8GB, or 8192MB.
  - Next, change the Java version.
    - MC versions 1.7.10 to 1.16 needs Java 8.
    - MC versions 1.16 to 1.19 needs Java 17.
    - MC versions 1.20 & above needs Java 21.
- Time to switch tabs, to `Server and Startup`.
  - Toggle `Skip startup EULA check` to `TRUE`.
  - Change `Server Type` to the modloader required for your chosen modpack. e.g. Forge, Fabric, Neoforge, etc.
  - Change `Official version` the whatever version is shipped with the server files for your chosen modpack.
- Head over to the `Gameplay and Difficulty` tab.
  - (Optional) Change the `Difficulty` to whatever you choose. e.g. Easy, Normal, Hard.
  - Toggle `Allow Flight` to `TRUE`. This allows for modded items that provides creative flight.
  - Toggle `Allow Command Blocks` to `TRUE`. This allows for setting up "server lobbies" if needed, to initialise a players "island" or other types of bases.
  - Set `Max Tick Time` to `-1`. This prevents unneccessary watchdog errors & tells us the cause of issues, DIRECTLY.

## Step 5

<img width="526" height="515" alt="image" src="https://github.com/user-attachments/assets/2f569875-c63d-403b-a3b6-88a2aba9f692" />

- Download the server files from the chosen Modpack Provider.
- Head to `File Manager`.
- Paste the ZIP folder containing your server files here. Then click the 3 dots to the right side of this file and click `Extract Here`.

<img width="234" height="679" alt="image" src="https://github.com/user-attachments/assets/f1fc16e3-4147-4303-ad5f-17ca1b513ea7" />

If everythings setup right, you should then be able to start the server, using the actions bar mentioned earlier.
