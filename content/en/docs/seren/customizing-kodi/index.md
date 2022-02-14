---
title: "Customizing Kodi"
description: ""
lead: ""
date: 2022-02-12T13:38:28Z
lastmod: 2022-02-12T13:38:28Z
draft: false
images: []
menu:
  docs:
    parent: "seren"
weight: 300
toc: true
---

For some parts of this explanation we'll assume you are more comfortable navigating in Kodi so we'll illustrate steps with fewer images and provide a more step by step approach for things we covered before like [adding repositories](/seren/installing-seren/#adding-a-repository) and [installing addons](/seren/installing-seren/#installing-an-addon).

## Installing the Arctic Horizon Skin

We'll start by installing a custom skin, an add-on that changes the look and feel of Kodi.

{{< alert icon="👉" text="This tutorial will only cover the Arctic Horizon skin but there are lots of other skins you can try" />}}

We'll start by adding a new repository, by going to `File Manager` → `Add source` and entering the following url:

```
https://jurialmunkey.github.io/repository.jurialmunkey/
```

Give it a name like `jurialmunkey` and confirm.

Now in the `Install from zip` option of the `Add-ons` settings page install the `repository.jurialmunkey-2.2.zip` file found on the `jurialmunkey` source we added in the previous step.

After the installation is complete we will now install 3 different add-ons from this new repository. Navigate to `Addons` → `Install from repository` → `jurialmunkey Alpha Repository`.

In `Context menus` install the `TMDbHelper` add-on.

In `Program add-ons` install the `Skin Variables` add-on.

After the previous two add-ons are installed you can finally install the skin by going to `Look and feel` → `Skin` → `Arctic Horizon`.

A popup will ask you if you'd like to switch to the installed skin, simply press `Yes`.

A `Skin Setup Wizard` popup might appear, if so, select `OK` on the right side. Before accepting you can also change the `Colour scheme` to your liking.

![Skin Setup Wizard](skin-setup-wizard.png)

You can now see all of Kodi looks different. This means that the skin is successfully installed and in use. Your Kodi home screen should look something like this:

![Arctic Horizon Home](arctic-home.png)

## Installing the Arctic Horizon Seren Theme

Arctic Horizon also includes a custom theme for Seren. Go to `Seren` → `Tools` → `Open Settings Menu`.

![Seren Install Theme](seren-install-theme.png)

In the `Interface` section select `Install theme` → `Web Location...` and enter the following url:

```
https://www.github.com/drinfernoo/seren.theme.ah/zipball/master/
```

a popup will appear asking you to switch to the installed theme just press `YES`.

## Configuring the Main Menu

We will now configure the Kodi home screen to be more useful for our purposes. We will map some of Seren's pages and functionalities to the main menu so they are easily accessible.

Let's start by going to `Skin Settings` → `Home` → `Customise home menu`.

![Skin settings](skin-settings.png)

On the left you'll see all your main menu shortcuts listed. We'll remove all the unnecessary ones and keep `TV Shows`, `Movies`, `Search`, `Add-ons` and `Settings`.

![Main Menu order](main-menu-order.png)

We'll now have to link the `TV Shows` shortcut to an `Action` that triggers when clicked. When we click on `TV Shows` we want Kodi to send us to Seren's `Discover TV Shows` page.

{{< alert icon="👉" text="While using Arctic Horizon you have to set a shortcut action in order for that shortcut section to appear in the Main Menu so don't skip this stage" />}}

In the `TV Shows` section go to `Action` → `Add-On` → `Video Add-on` → `Seren` → `Discover TV Shows` → `Create menu item to here`.

#### Adding a widget

Next we'll add a widget to the TV Shows section. A widget is a way of displaying information from addons on the screen. We'll be adding a *Next up* widget to the home screen to quickly access the next episode to watch.

Inside the `TV Shows` shortcut navigate to `Widgets - Home` to manage the page's widgets.

![Widgets - Home](widgets-home.png)

In here you can create different views that you have access in the home screen. Remove all the default views with the `✕` until you see `<None>`.

![None widgets](widgets-none.png)

We'll now associate this blank widget with the `Next Up` section of the `Seren` plugin.

Go to `Choose widget` → `Add-On` → `Video Add-On` → `Seren` → `My Shows` → `Next Up` → `Use as widget`. This will make the contents of that folder be loaded to our widget.

Next we'll choose how the widget looks by selecting one of the `Aspect` options below. 

**Poster**
![Widget Poster Aspect](widget-poster.png)

**Square**
![Widget Square Aspect](widget-square.png)

**Landscape**
![Widget Landscape Aspect](widget-landscape.png)

**Banner**
![Widget Banner Aspect](widget-banner.png)

**Icon**
![Widget Icon Aspect](widget-icon.png)

**Lovefilm**
![Widget Lovefilm Aspect](widget-lovefilm.png)

We'll be using the `Landscape` option.

Doing the same for the `Movies` shortcut, we'll map it's `Action` to the `Discover Movies` page of Seren.

On the `Movies` subsection go to `Action` → `Add-On` → `Video Add-On` → `Seren` → `Discover Movies` → `Create menu item to here`.

![Shortcuts Movies section](shortcuts-movies.png)

Let's also add some movie widgets to the home screen. Go to `Widgets - Home` and add a widget for recent popular movies. `Choose widget` → `Add-On` → `Video Add-On` → `Seren` → `Discover Movies` → `Popular Recent Movies` → `Use as widget`.

We also added a Watchlist (`Seren` → `My Movies` → `Watchlist`) shortcut that will display the movies you add to your Trakt watchlist and a Finish Watching (`Seren` → `My Movies` → `Finish Watching`) shortcut that will show you the movie you just couldn't finish yesterday.

![Movie widgets](widgets-movies.png)

We'll finish off by assigning an `Action` to the `Search` shortcut. This is where you'll go to search for something you want to watch, we'll link it to Seren's `Search` page.

In the `Search` shortcut go to `Action` → `Add-On` → `Video Add-On` → `Seren` → `Search...` → `Create menu item to here`.

![Shortcuts Search section](shortcuts-search.png)

After returning to the home screen and waiting for the skin to load you'll see your new home screen.

{{< alert icon="👉" text="Some widgets might not appear if you don't have information on your trakt account yet. This will automatically update when you start watching movies and shows using Seren" />}}

**TV Shows**
![TV Shows Main Menu](main-menu-tv-shows.png)

**Movies**
![Movies Main Menu](main-menu-movies.png)

**Search**
![Search Main Menu](main-menu-search.png)

Use this `Search` button on the home screen to find the content you want to watch. You can now create your own widgets and customize the Seren experience to your liking using the information you learned from this guide. You can also experiment with other options in the `Skin settings`.