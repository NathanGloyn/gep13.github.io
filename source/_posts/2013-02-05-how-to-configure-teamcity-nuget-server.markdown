---
author: gep13
comments: true
date: 2013-02-05 20:00:45+00:00
layout: post
slug: how-to-configure-teamcity-nuget-server
title: How to configure TeamCity NuGet Server
wordpress_id: 1899
categories:
- Chocolatey Series
tags:
- chocolatey
- Nuget
- TeamCity
---

# What is TeamCity NuGet Server?


Within TeamCity, it is possible to integrate the NuGet Package Manager, which then allows you to:


<blockquote>

> 
> 
	
>   * Install and update packages: [NuGet Installer](http://confluence.jetbrains.com/display/TCD7/NuGet+Installer) build runner;
> 
	
>   * Pack packages: [NuGet Pack](http://confluence.jetbrains.com/display/TCD7/NuGet+Pack) build runner;
> 
	
>   * Publish packages to a feed of your choice: [NuGet Publish](http://confluence.jetbrains.com/display/TCD7/NuGet+Publish) build runner. Alternatively you can use TeamCity as NuGet server.
> 

</blockquote>


If you want to find out more information about the TeamCity NuGet Server, you can find it [here](http://confluence.jetbrains.com/display/TCD7/NuGet)

The following blog post walks through the steps to set up the TeamCity Nuget Server.


# Installation Steps


**NOTE: **The following configuration steps and screenshots were taken from a virtual machine with Windows Server 2008 R2 Service Pack 1, running Hyper-V on a Windows 8 Host Machine.

These instructions are specific to version 7.1.3 of TeamCity, however, later version will likely follow very similar steps.

You can see screenshots of each of these steps in the gallery at the bottom of this blog post.



	
  1. Assumption is that you already have [TeamCity](http://gep13.me/VAeRiX) installed

	
  2. Log into your TeamCity instance

	
  3. Click on the Administration link at the top right hand corner

	
  4. Click on NuGet Settings down the left hand side

	
  5. By default, the NuGet Server will be disabled, so simply click on Enable to start it up

	
  6. By default, public access to the NuGet Server is not enabled, as the Guest User access will not be set up.  However, this can be done within Global Settings.  Assuming that you are wanting to easily gain access to the Feed that TeamCity provides, enabling this public access is recommended.  This is what we will do in the next few steps.

	
  7. Click on Global Settings

	
  8. Make sure that the "Allow to login as a guest user" checkbox is checked

	
  9. Go back to NuGet Settings, and you should now see that the Public Feed URL is enabled, and a URL to the feed to provided

	
  10. Click on the "NuGet Commandline" tab.  In here you can actually have multiple versions of the NuGet.exe installed, ready for use within different Build Configurations.  Click on "Add NuGet".

	
  11. Select the version that you want to install, and click Add.

	
  12. And that's that!




# Installation Screenshots


[gallery ids="1900,1901,1902,1903,1904,1905,1906,1907,1908,1909,1910"]
