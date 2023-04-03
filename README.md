# garlic-onion-skraper-mix

Create great box art for [Garlic](https://www.patreon.com/posts/76561333) or [Onion](https://github.com/OnionUI/Onion)

**choose your style:**
* [Full Height Mix](#full-height-mix)
* [3-Images Mix](#3-images-mix)

# Full Height Mix

![GarlicOS_001](https://user-images.githubusercontent.com/57577242/227276625-7772e477-e1f7-4656-9a29-2725ced99c00.png)
![GarlicOS_002](https://user-images.githubusercontent.com/57577242/227276635-a965ad3d-6b5f-4edd-8836-38a72345c6d2.png)
![GarlicOS_003](https://user-images.githubusercontent.com/57577242/227277696-80248862-98a8-4a58-a467-fa93f9cc9a72.png)
![MainUI_001](https://user-images.githubusercontent.com/57577242/227276651-25dbf081-ef71-48fc-b920-239e3c0b7188.png)
![MainUI_002](https://user-images.githubusercontent.com/57577242/227276660-2e478459-9670-41cb-ae4d-f8f5dae57993.png)
![MainUI_003](https://user-images.githubusercontent.com/57577242/227277983-961c627e-0021-4ca4-889e-281bbfb6c204.png)

## About

This was inspired by the following guides:  
- [Scraping Onion Artwork](https://github.com/OnionUI/Onion/wiki/Scraping-artwork-for-games)  
- [Retro Game Corps RG35XX starter guide](https://retrogamecorps.com/2023/01/03/anbernic-rg35xx-starter-guide/)  

I loved this template created by AchillesPDXI so I updated it to create a 333 x 480 version which should look good on the miyoo mini as well as the MM+ and RG35XX which have a slightly larger screen.

## Instructions  

### Set-up Skraper and Skrape with custom mix template

- Download the Garlic-Onion-Mix folder from this project
- Download and run [Skraper](https://www.skraper.net/)
- You may want to run through the following guide to familiarize yourself with Skraper: [Retro Game Corps Skraper Guide](https://retrogamecorps.com/2021/04/02/quick-guide-skraper-for-retro-handheld-devices/)
- Select "All Systems"
- In the "Media" tab for Skraper set the Media type to "User Provided Mix"
- Click the "page" icon next to media type and select the `Garlic-Onion-Mix.xml` file you downloaded from this repo
- Set the "Output Folder to: `%ROMROOTFOLDER%\Imgs` and select "Cleanup output folder before generating new medias" checkbox
- Leave "Resise Width to" "Resize height to" and "Keep image ratio" blank.
- Your Skraper screen should look like this:  

![skraper](https://user-images.githubusercontent.com/57577242/227281809-60ac13e7-b88b-437e-bccc-b221e584bb76.png)

- Skrape all of your systems
- Delete any gamelist.xml files that the skraper created
- If you are using Onion you are done!

### Additional Garlic Steps

- On your SD1 card, navigate to CFW > skin > settings.json
- Edit settings.json to use the following:  
`"text-alignment": "left",`    
`"text-margin": 352,      `   
- Download and install [ImageMagick](https://imagemagick.org/script/download.php)
- Follow one of the options below:

#### Modify individual Imgs folders
- Navigate to each Imgs folder and then hold SHIFT and right-click in that folder
- Select “Open PowerShell window here”. A command line will open up (for mac you can use terminal)
- type the following into the command line:  

`magick mogrify -monitor -resize 340x480 -extent 640x480 -gravity West -background none *`

#### Bulk Modify ALL Imgs Folders (Windows Only)
- Navigate to the Roms folder and then hold SHIFT and ricght-click in that folder
- Select "Open PowerShell window here".  A command line will open up
- type the following into the command line:

`Get-ChildItem -recurse | where {$_.name -eq "Imgs"} | foreach {cd -LiteralPath $_.FullName; magick mogrify -monitor -resize 340x480 -extent 640x480 -gravity West -background none *;}`

# 3-Images Mix

![GarlicOS_3img-000](https://user-images.githubusercontent.com/57577242/229637443-5cd16761-374c-41f4-921c-ba3380a80664.png)
![GarlicOS_3img-001](https://user-images.githubusercontent.com/57577242/229637455-d408f25b-138c-4440-81e3-2a312f93b80c.png)
![GarlicOS_3img-002](https://user-images.githubusercontent.com/57577242/229637482-b940eca7-7144-4b61-bed2-9bbc65ce7b08.png)
![MainUI_3img-002](https://user-images.githubusercontent.com/57577242/229637505-99084c5c-79c7-4f1c-a671-bce569a5547c.png)
![MainUI_3img-001](https://user-images.githubusercontent.com/57577242/229637517-c5826b4f-121d-40bd-8aaa-3ba24dc61251.png)
![MainUI_3img-000](https://user-images.githubusercontent.com/57577242/229637530-891f00db-da25-4368-90d5-020d0510cd3b.png)

## Instructions  
### Set-up Skraper and Skrape with custom mix template

- Download the 3 Image Mix - Onion or 3 Image Mix - Garlic folders from this project
- Download and run [Skraper](https://www.skraper.net/)
- You may want to run through the following guide to familiarize yourself with Skraper: [Retro Game Corps Skraper Guide](https://retrogamecorps.com/2021/04/02/quick-guide-skraper-for-retro-handheld-devices/)
- Select "All Systems"
- In the "Media" tab for Skraper set the Media type to "User Provided Mix"
- Click the "page" icon next to media type and select the `3_img_mix_onion.xml.xml` or `3_img_mix_garlic.xml.xml` file you downloaded from this repo
- Set the "Output Folder to: `%ROMROOTFOLDER%\Imgs` and select "Cleanup output folder before generating new medias" checkbox
- Leave "Resise Width to" "Resize height to" and "Keep image ratio" blank.
- Your Skraper screen should look like this:  

![skraper](https://user-images.githubusercontent.com/57577242/227281809-60ac13e7-b88b-437e-bccc-b221e584bb76.png)

- Skrape all of your systems
- Delete any gamelist.xml files that the skraper created
