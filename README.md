# Underworld cloud on digital ocean 

This is a template repository for setting up a [digital ocean](https://www.digitalocean.com/) jupyterhub running underworld codes. It can be used as a starting point for quickly setting up a new lightweight jupyterhub service. 

## Description

This repository can build itself into a digital ocean droplet that runs (the littlest) jupyterhub with the underlying dependencies that you specify in a conda environment `yml` file. The configuration of the droplet
is stored in the repository secret variables. Github actions are configured to monitor the repository and update
the content of the server when changes to the configuration are pushed. The actions also check to see if the server
is alive and well. 

This template repository contains a couple of test notebooks to ensure that the hub is working and that the software stack is correctly installed. Once running, however, it can be used to run arbitrary content via [nbgitpuller](https://jupyterhub.github.io/nbgitpuller)
 
![Health check](https://github.com/ underworld-geodynamics-cloud/underworld-cloud-droplet/workflows/Health%20check/badge.svg)


## How to use this template

The full set of instructions is given in the [Documentation](Documentation) folder. The steps are:

  - Create a suitable server ([instructions are for a Digital Ocean droplet](Documentation/DigitalOcean.md))
  - Make a clone of this template repository (See [Github.md](Documentation/Github.md))
  - Update the cloned repository with information about the server that you have set up
  - Commit the updates on Github to trigger the build / rebuild of the content of the server
  - Create links for `nbgitpuller` for users of the server and test them (See [nbgitpuller.md](Documentation/nbgitpuller.md )) 
  - Add your users to the `jupyterhub` ([ManagingUsers.md](Documentation/ManagingUsers.md))


## Try out the Nbgitpuller

To make a "binder-like" link to a repository on a droplet that you have set up, you can read the [nbgitpuller documentation](https://jupyterhub.github.io/nbgitpuller/link.html) or fill out a form here:

[![https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>](https://img.shields.io/badge/Admin-LinkMaker-Red)](https://jupyterhub.github.io/nbgitpuller/link.html?hub=https://demon.underworldcloud.org&repo=https://github.com/underworld-geodynamics-cloud/underworld-cloud-droplet)

<!-- You can launch this example particular example to try it out by clicking on this link. Your work is persistent. 

[![https://img.shields.io/badge/<LABEL>-<MESSAGE>-<COLOR>](https://img.shields.io/badge/Launch-Demo-blue)](http://demon.underworldcloud.org/hub/user-redirect/git-pull?repo=https%3A%2F%2Fgithub.com%2FANU-RSES-Education%2Fdroplet-template&urlpath=tree%2Fdroplet-template%2FStartHere.ipynb&branch=master) -->
    
## Administration tasks
    
If the hub has a signup page it can be reached here:
    
[![Signup](https://img.shields.io/badge/User-Signup-blue)](https://demon.underworldcloud.org/hub/signup)

And the corresponding page for an admin user to authorise the users after they sign-up is
    
[![Authorize](https://img.shields.io/badge/Admin-Authorize-Red)](https://demon.underworldcloud.org/hub/authorize)
   
Admin users also have access to the hub control panel to shut down wayward servers and add / remove users. 
    
[![ControlPanel](https://img.shields.io/badge/Admin-HubControlPanel-Red)](https://demon.underworldcloud.org/hub/admin)
    
    


