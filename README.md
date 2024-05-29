# 🔴 How People Can Interact With My Avatar In Live ? 👥

![Group 564](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/fc085160-6bb6-41eb-a3e1-0c737d851392)

# Hey there, it's Hyroe ! :3

I will explain to you how people in your TikTok Live can interact with your avatar on VRChat.

## 1. First Step: Link TikTok Chat and Send It to the OSC Server

→ First, download PyCharm Community from this [link](https://www.jetbrains.com/pycharm/download/download-thanks.html?platform=windows&code=PCC).

→ Create a new Python project and create a Python file in this folder.

![New Python Project](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/983f4efb-e8aa-4b4a-a22f-8c6d1c4c356b)
![Create Python File](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/e8fccf90-bea9-4789-bfa1-5dd68f568ac3)

→ Copy and paste the code and install all the necessary libraries:
- In Python packages, import "TiktokLive" and install it.

![Install TiktokLive](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/4597f5a0-6f6a-447b-8261-60fee8fabf33)
![Python Packages](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/70d99656-a8be-43d9-b0ac-42cd85861908)

- Import this GitHub repository: [python-osc](https://github.com/attwad/python-osc)
  "Add Package" → "From Version Control" → Copy & paste the link and press "OK".

![Add Package from Version Control](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/c7d4fa9b-0182-4f69-a528-291f2a9bcf48)
![Import python-osc](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/3a1c149f-da94-4813-a915-6bd088551d52)

→ Put your TikTok name tag (for me it is @hyroe at line 51) and run the Python program when you are live.

![Insert TikTok Name Tag](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/100a0e86-8733-46ae-927f-052b550b4581)

## 2. Link Parameters in Your “.json” File

With the help of the OSC server, we will be able to send and receive data.
For example, in the code provided, if someone sends “boop” in the TikTok chat, BoopToggle is set to 1.

### You now need to add this parameter to the text file of your avatar.

→ To understand how the OSC parameters work, here is the link from the official VRChat webpage (Please read it :3): [VRChat OSC Avatar Parameters](https://docs.vrchat.com/docs/osc-avatar-parameters).

→ Copy the Blueprint ID in your Pipeline Manager Component of your avatar in your Unity project.

![Copy Blueprint ID](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/24a76fe5-8c09-4d54-9ab6-4e35a7a5a23b)

→ Open this folder: `C:\Users\YourName\AppData\LocalLow\VRChat\VRChat\OSC`

Search (CTRL+F) by pasting your ID and open the `.json` file.
You should see something like this with different parameters:

![JSON Parameters](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/aeea7185-e6a8-48ce-b9f0-ce510e7440cb)

Now we want to add our new parameter, “BoopToggle”:
```json
{
  "name": "BoopToggle",
  "input": {
    "address": "/avatar/parameters/BoopToggle",
    "type": "Boolean"
  },
  "output": {
    "address": "/avatar/parameters/BoopToggle",
    "type": "Boolean"
  }
}
```
> Check if your parameter in your Unity project is a Boolean; if not, change the type.

## 3. Test on VRChat :3

→ Enable OSC Server.

![Enable OSC Server](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/3411ea1b-76cd-4bc1-b9fe-a91c14ae7df7)
![OSC Server Settings](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/78359d0e-7062-4bb9-b16a-b3816f448580)

→ After starting your TikTok Live and running your code, you should see this in your OSC Debug Panel:

![OSC Debug Panel](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/5b4cf95a-1ff3-4b30-a78a-72b157a58a08)
![OSC Debug Panel Details](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/9524090b-ffe9-4c01-90c9-57908f367a52)

> Sometimes it doesn’t work for some people in my lives, so if you have any ideas, let me know! :3

Have a wonderful day/night!

→ Follow me on my socials:
- [TikTok](https://www.tiktok.com/@hyroe)
- [Twitter](https://x.com/_Hyroe_)
- [Instagram](https://www.instagram.com/hyroevr/)

Boop from Hyroe :3
