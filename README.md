# HTML5 World IO
An experimental HTML5 online multiplayer game I was planning on creating. Due to time constraints and college, I wasn't able to achieve what my original goals were with the project. Therefore, I've decided to open-source the source files for anybody to hack-on and improve.

# Dependencies
`cd` into the bin folder and execute `pip install -r requirements.txt`

# Configuration
In the `etc` folder, the `serve.json` file contains the configurations to the SocketIO server. Modify it to your liking.  

In the `hub.js` file inside the `src/client/world/rooms/hub` folder, change the value of the `socket` variable to your host and port. Note that whenever creating new rooms or updating the hub using the `hub.fla` as a template, you'll need to modify the `socket` variable everytime to match the configuration from `serve.json`.

# Running The Server
Inside the bin folder, there's a file named `serve.py`. Use `python serve.py` to run it and successfully start the SocketIO server.  

The project's rooms operate synonmously with its namespace, so they share the same identifiers. In order to load the base room, go to the `src/client/world/rooms/hub` folder and open the `hub.html` file in another web-browser. 

# Hacking-on and Improvements
If you wish to create your own rooms, then open the `hub.fla` file in Adobe Animate CC and utilize it as a template to create other rooms.
For each room you create, the server-side for the room should programmed in the `src/server/world/rooms/` directory to maintain organization.
