# DrLulz Anki Template

![gif](readme_images/anki.gif)

This repository adds extra functionality and styling to Anki cards. 

1. [Magnific Popup](http://dimsemenov.com/plugins/magnific-popup/) for Images
2. Image [Zoom](http://www.jacklmoore.com/zoom/)
3. Notifications via [Noty](http://ned.im/noty/#/about) (For Reinforcement)
4. [Bootstrap](http://getbootstrap.com)
5. Dark Styling loosely based on [Tomorrow Night Theme](https://github.com/chriskempson/tomorrow-theme)
6. URL button in cards
7. With the exception of bootstrap & styling, the plugins above will not load on mobile. (You can include their .js in the template if you want it on mobile)


## Usage

##### Magnific Popup & Zoom

- All images will have popup and zoom enabled.  
- Images placed in fields `Front Image` and `Back Image` will have their width limited/reduced.  
-- With popup and zoom there's no need for full size images.  

<br />
##### Noty
- Use sparingly.  
- Anki doesn't allow linking cards (always showing card y after card x). There's good reason for [this](http://ankisrs.net/docs/manual.html#can-i-link-cards-together-add-dependencies-how-should-i-handle-synonyms). However, there are times when I'd like to be reminded of an related idea after answering a card, so this is where Noty is useful in Anki cards.  
- The field `NotyFront` will display a notification on the front side, etc.  
- If you leave fields `NotyFront` and `NotyBack` empty then no notification will be shown.  

<br />
##### URLs
- URLs should be in the form `www.google.com` or `google.com` (ie leave out the `http://`).  
- If present the link will display in the lower right.  

<br />
##### Cloze Cards
- Cloze cards will automatically align to the left. If you type <kbd>center</kbd> in the field `class` then the card will center align.  

<br />
##### Basic & Basic-Double Cards
- Basic cards will automatically align to the center. If you type <kbd>left</kbd> in the field `class` then the card will left align.  

<br />
##### Other Notes
- If you bold text when creating cards the css will automatically assign it a color.
- The `Back` field on Basic cards is givin the same color as cloze deletions.

<br />
## Install

#### 1. Install JS Booster Anki Addon

- [JS Booster](https://ankiweb.net/shared/info/1280253613)

<br />
#### 2. Download the .zip of this repository (right sidebar)
<br />
#### 3. Locate your Anki user folder

The default location is `/Anki/User 1`  
If you changed your username then `/Anki/DrLulz`  

To ensure you’re in the right place look for directories
- `/Anki/DrLulz/collection.media`
- `/Anki/DrLulz/backups`

<br />
#### 4. Add jQuery directories and image file

After unzipping move the folders `jquery` & `js`, and the file `man_sm.png` into your user folder.

- `/Anki/DrLulz/jquery`
- `/Anki/DrLulz/js`
- `/Anki/DrLulz/man_sm.png`

<br />
#### 5. Create / Modify Note Types

![notes](readme_images/types.png)

You can either create new note types or modify existing types.

- Go to `Tools > Manage Note Types`
- Click `Add` and then select `Add: Basic`
- Assign a unique name to the note type

- In this tutorial we’ll add a basic note type using `basic-single.html`. When finished repeat this process for `basic-double.html` and `cloze.html`

<br />
#### 6. Add Header / Footer to Note Type

Select your newly created note type, and click the `options` button.

- In the .zip folder locate the file `header-footer.tex`. Optionally, you could just grab the text from the repository.
- Copy `lines 1-11` to the header field, and `line 20` to the footer field.

![notes](readme_images/options.png)

<br />
#### 7. Add Fields to Note Type

There are two defaults fields `front` and `back`. To use this template exactly you will need to add eight more fields. You could of course modify this to suit your needs.

##### Add the following fields:

- `Front S/S`
- `Front Image`
- `Back S/S`
- `Back Image`
- `NotyFront`
- `NotyBack`
- `URL Title`
- `URL`
- `class`


##### Reposition the fields to match the picture.
![notes](readme_images/fields.png)

<br />
#### 8. Add the HTML

Still in the note types window click the `Cards` button. On the left is the `Front Template`, `Styling` and `Back Template`. 

##### From `basic-single.html` 

- Copy `lines 3-71` to the `Front Template` field
- Copy `lines 77-148` to the `Back Template` field


##### From `anki.css`

- Copy everything to the `Styling` field. 

![cards](readme_images/cards.png)

<br />
#### 9. Create cards & enjoy

<br />
<br />
## LaTeX Styling

- LaTeX Equations Match the Background
- So the equation `[$]SEM=\frac{\sigma}{\sqrt{{{c1::n}}}}[/$]` would display as:

![latex](readme_images/latex_cloze.png)


  
- Optionally, you can color the cloze using HEX color code or naming basic colors:
	- `[$]SEM=\frac{\sigma}{\sqrt{\color[HTML]{E8BF6A}{{c1::n}}}}[/$]`
	![latex](readme_images/latex_cloze_color1.png)
	
	
	- `[$]SEM=\frac{\sigma}{\sqrt{\color{green}{{c1::n}}}}[/$]`
	![latex](readme_images/latex_cloze_color2.png)
	

## Changelog

````
03.17.15
	bootstrap
	cleaned up css
````