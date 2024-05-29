# 🔴 How People Can Interact With My Avatar in Live Streams 👥

![Group 564](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/fc085160-6bb6-41eb-a3e1-0c737d851392)

## Hey there, it's Hyroe! :3

Let me show you how people in your TikTok Live can interact with your avatar on VRChat.

## 1. First Step: Link TikTok Chat and Send It to the OSC Server

### Setup Your Python Environment

1. **Download PyCharm Community** : [Download Here](https://www.jetbrains.com/pycharm/download/download-thanks.html?platform=windows&code=PCC).

2. **Create a New Python Project** :
   - Open PyCharm and create a new project.
   - Create a new Python file in this folder.

   ![New Python Project](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/983f4efb-e8aa-4b4a-a22f-8c6d1c4c356b)
   ![Create Python File](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/e8fccf90-bea9-4789-bfa1-5dd68f568ac3)

3. **Install Required Libraries** :
   - In Python packages, import `TiktokLive` and install it.

   ![Install TiktokLive](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/4597f5a0-6f6a-447b-8261-60fee8fabf33)
   ![Python Packages](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/70d99656-a8be-43d9-b0ac-42cd85861908)

   - Import the GitHub repository : [python-osc](https://github.com/attwad/python-osc)
     - Go to "Add Package" → "From Version Control" → Copy & paste the repository URL and press "OK".

   ![Add Package from Version Control](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/c7d4fa9b-0182-4f69-a528-291f2a9bcf48)
   ![Import python-osc](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/3a1c149f-da94-4813-a915-6bd088551d52)

4. **Run the Python Program** :
   - Update the code with your TikTok username (for me it is @hyroe at line 51).
   - Run the Python program when you are live on TikTok.

   ![Insert TikTok Name Tag](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/100a0e86-8733-46ae-927f-052b550b4581)

## 2. Link Parameters in Your `.json` File

### Configure OSC Parameters

1. **Understand OSC Parameters** :
   - Read the [VRChat OSC Avatar Parameters Documentation](https://docs.vrchat.com/docs/osc-avatar-parameters).

2. **Get Your Avatar's Blueprint ID** :
   - Copy the Blueprint ID from the Pipeline Manager Component of your avatar in your Unity project.

   ![Copy Blueprint ID](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/24a76fe5-8c09-4d54-9ab6-4e35a7a5a23b)

3. **Edit the `.json` File** :
   - Open the folder: `C:\Users\YourName\AppData\LocalLow\VRChat\VRChat\OSC`
   - Search (CTRL+F) for your Blueprint ID and open the corresponding `.json` file.

   ![JSON Parameters](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/aeea7185-e6a8-48ce-b9f0-ce510e7440cb)

4. **Add the New Parameter** :
   - Add the following parameter to the `.json` file:
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
   - Ensure that the parameter type in your Unity project is Boolean.

## 3. Test on VRChat :3

### Enable OSC Server

1. **Enable OSC Server in VRChat**:
   - Go to VRChat settings and enable the OSC server.

   ![Enable OSC Server](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/3411ea1b-76cd-4bc1-b9fe-a91c14ae7df7)
   ![OSC Server Settings](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/78359d0e-7062-4bb9-b16a-b3816f448580)

2. **Start Your TikTok Live and Run Your Code**:
   - Once live and with your code running, check the OSC Debug Panel in VRChat to see the incoming data.

   ![OSC Debug Panel](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/5b4cf95a-1ff3-4b30-a78a-72b157a58a08)
   ![OSC Debug Panel Details](https://github.com/HyroeVRC/TiktokToOSC/assets/170990155/9524090b-ffe9-4c01-90c9-57908f367a52)

> If it doesn't work for some people, feel free to reach out with any ideas or questions! :3

Have a wonderful day/night!

→ Follow me on my socials:
- [TikTok](https://www.tiktok.com/@hyroe)
- [Twitter](https://x.com/_Hyroe_)
- [Instagram](https://www.instagram.com/hyroevr/)

Boop from Hyroe :3
