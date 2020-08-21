---
layout: post
title: Command line free tutorial for deploying your learnr tutorial
---

Congrats! Now you have configured the shiny server on your virtual machine. Let's open an terminal and `scp` your tutorial. What? You said you hate command line. Ok, this blog will show you how to deploy a learnr tutorial without a single command line.

My collegue Amy Nussbaum recently introduced me to this wonderful tool called the Cyberduck. According to their website, "Cyberduck is a libre server and cloud storage browser for Mac and Windows with support for FTP, SFTP, WebDAV, Amazon S3, OpenStack Swift, Backblaze B2, Microsoft Azure & OneDrive, Google Drive and Dropbox." You can download Cyberduck from their webpage [https://cyberduck.io](https://cyberduck.io) directly. 

## Step 1: open a connection on cyberduck

[im1](https://github.com/sshanshans/writing/blob/master/images/post/cyberduck1)

Click on the open connection button in the tool bar.

## Step 2: connect to your virtual machine
Now let's make a folder to host your learnr tutorial. Run the following in your terminal.

[im2](https://github.com/sshanshans/writing/blob/master/images/post/cyberduck2)

- In the dropdown menu, select  `SFTP (SSH File Transfer Protocol)`.
- Type your [host_address] at `Server`
- Type in your username
- Type in your passwork
- Click Connect

## Step 3: go to the `/srv/shiny-server/` folder
To host your learnr tutorial, you need to place the tutorial file (.Rmd) in the correct folder. Use the folder dropdown menu to change current working directory to `/srv/shiny-server/`. 

[im3](https://github.com/sshanshans/writing/blob/master/images/post/cyberduck3)

You can also create a new subfolder by right-clicking your mouse. Here I created a nests of subfolders `sshan/tutorials/unit1`.  Then simply use your mouse to drop the file(s) you want to deploy to this folder.

[im4](https://github.com/sshanshans/writing/blob/master/images/post/cyberduck4)


In general, it is recommended to create a separate folder for each learnr tutorial/shiny app. 

## Your tutorial is now up in the air
Violin! (Sorry viola-gang.) You have just uploaded and deployed your first learnr tutorial on the shiny server. You can view it by going to that folder's URL listened on the IP address `138.110.84.108`  with port `3838`. 
```
http://http://138.110.84.108:3838/[remote_folder]/tutorial.Rmd
```
