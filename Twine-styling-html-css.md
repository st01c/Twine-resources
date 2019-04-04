# TWINE STYLING USING HTML AND CSS

_Part of a collection of resources and links related to the Twine digital storytelling platform, initially created for students in Digital Media Practice at Anglia Ruskin University._

Below are some *very* basic tips to style your project using simple HTML and CSS tags.

---

### IMAGES on your passages:

Images used in your Twine must be located online, and you insert them using their URL location. Remember my recommendation that you use the free online service [IMGUR](https://imgur.com/) for this purpose.

Step-by-step instructions:

1. Create an Imgur membership
2. Locate an image you want to use online.
3. Download the image to your harddrive (as a .jpg or .png file)
4. Upload the file to Imgur.
5. In your list of images on Imgur, click on an image, and note that all kinds of 'embed code' is provided on the right.
6. Click on the button to copy the 'Direct Link' (this is the URL address of your image).

7. Now, the easiest way to insert images into your project is to use a simple HTML code snippet, like so:

```Html
<img src="https://i.imgur.com/F7Cv48x.jpg" alt="spongebob" width="300" height="128">
```
 
Note that you can manipulate the width and height of all images (the spongebob in my example is probably rather squashed.)


### VIDEO in your passages (can also be used to create SOUND EFFECTS)

The use of videos is pretty straightforward. Basically, you'll simply embed YouTube videos - so again, you need the URL of the video.

1. Browse to the YouTube video you've chosen.
2. Right-click the video.
3. Click on 'Copy embed code'
4. Paste the code into your Twine passage.
The code will look something like this:
```HTML
<iframe width="1273" height="716" src="https://www.youtube.com/embed/euHoHdpGOa0" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
```
5. Now you have to manipulate the code a little bit. Specifically, we want the video to start playing automatically. The way to achieve this is to enter a bit of code that tells YouTube to start playing the video automatically (without the user having to click):
```HTML
<iframe width="0" height="0" src="https://www.youtube.com/embed/vNwYtllyt3Q?autoplay=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
```
In this example, first of all I added `?autoplay=1` at the end of the basic video URL (which is `https://www.youtube.com/embed/vNwYtllyt3Q` in the example).

6. SOUND EFFECT TIP: Note that in the example above, I also added `width="0" height="0"` in the beginning. This sets the size of the video to 0 (making it invisible). In other words, you can choose a video with a relevant sound effect for your passage, and then automatically have it play in the background.

### CHANGING THE STORY STYLESHEET

If you click the name of your Twine project on the bottom left of the main screen, several options come up, including edit 'Story Stylesheet'. Here, you can add CSS code to style your project (change color, fonts, background, etc.)
I'm including some basic examples below, but the possibilities are endless --- have a look at a CSS cheatsheet such as [this one](https://adam-marsden.co.uk/css-cheat-sheet) for some ideas of what you could do. Basically, if you've learned any CSS coding before, you can use it here.

Basic CSS coding examples:

```CSS
tw-story /* this indicates the main text body of the project */
{ 
  background-color: grey;
  
  background:url("https://i.imgur.com/xyMTp36.jpg") no-repeat;
  background-size: 100%;
  backgroud-height: 100%;

  color: orange; /* changes text color */
  
  font-family: Helvetica, sans-serif; /* changes to font style */
  font-style: italic;
  font-size: 100%;
  
  border: 5px solid red; /* a simple border around the passage */
  padding: 25px;
  margin: 25px;
  width: 75%;
}

tw-link /* this indicates the links within passages */
{
  color: white;
}
```
Obviously, this barely scratches the surface. There is a lot more you can do with CSS!

### _Note that there are additional options to style individual passages or text bits directly within the individual Twine passages! Have a look at the relevant parts of the [Harlowe style manual](https://twine2.neocities.org/#macro_background) to get started._
