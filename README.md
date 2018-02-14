# Use the nio platform on your AIY Vision Kit

A blank project including special blocks to interact with the Vision Bonnet in your [Vision Kit](https://aiyprojects.withgoogle.com/vision/)

## How to Use

  After [installing nio](https://docs.n.io/installation/) to your RaspberryPi, create a new directory for your nio project(s):  
  `mkdir -p nio/projects && cd nio/projects`
  
  Use the Command Line Interface that was installed for you alongside nio to create a new project from this template:  
  `nio new -t aiy_kit my_project`
  
  Name it whatever you like, instead of `my_project`, these instructions will assume that you used `aiy_kit` for the project name
  
  `cd aiy_kit`  
  This is the root of your project directory. From here nio can be started by running `niod`, but it will stop running as soon as you close the window or press ctrl-C. Run `sudo ./setup_nio.sh` to stop and disable the Joy Detection demo, and optionally create a systemd service to start nio automatically (in the background) with your RaspberryPi. While this is not required, only one application has access to the Vision Bonnet at a time so you will need to make sure it is available to use the included blocks.

### The systemd Service

If you run `setup_nio.sh` from your project's root directory, and create a system service to start with your Pi, the name of the service will match the project's directory name, in this case `aiy_kit`   
`systemctl start|stop|enable|disable aiy_kit`  
