---
layout: post
title: Globus File Transfer Instructions
date: '2025-02-17'
categories: Analysis
tags: [Bioinformatics]
---

## How to move files from Andromeda to Unity

Based on https://daniellembecker.github.io/DanielleBecker_Lab_Notebook/Data-Transfer-Andromeda-GlobusConnectPersonal-Pipeline/

### The first time you do this in Andromeda, you have to set up your access/account:

1. Load modules and start setup

```
interactive
module load GlobusConnectPersonal/3.2.0
globusconnectpersonal
```

2. Your terminal will say:

```
Will now attempt to run globusconnectpersonal -setup
Globus Connect Personal needs you to log in to continue the setup process.
We will display a login URL. Copy it into any browser and log in to get a single-use code. Return to this command with the code to continue setup.
```

3. Follow the link (starts with https://auth.globus.org), login with URI SSO credentials, to receive authorization code 
 
4. Enter the auth code into the terminal
5. Enter "~/data/putnamlab/" as endpoint when prompted
   1. **Record the endpoint string that is given here**
6. Edit your globus config file to make the endpoint readable and writeable

```
nano ~/.globusonline/lta/config-paths
```

Enter the following and save the file:

```
/data/putnamlab/,0,1
```

### Once you're set up, here is how to transfer files:

1. You first need to activate the endpoint from Andromeda:

```
interactive
module load GlobusConnectPersonal/3.2.0
globusconnectpersonal -start &
```

2. On Globus Connect in your browser (https://www.globus.org):
   1. Login
   2. Go to the File Manager and in the Collection field on the left, enter the personal endpoint string that was spit out by the globus setup above 
   3. Select acda5457-9c06-4564-8375-260ba428f22a (exact address of Unity) in the collection field on the right
   4. Select the files or folders you want to transfer from Andromeda to Unity and press ‘Start’.
  