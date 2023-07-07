
# Lifting the Bar 🚀
 

  ## Introduction 🤝


  <p align="left">
    Howdy, fellow Lifting the Bar researcher! 
	  
Here, you will find the code and documentation for the survey we distribute to students that are reintegrating into school. This document is designed to take you through how we have designed our code in Qualtrics (the survey engine) so that future edits and overhauls can be made! To see the code for every question, just click through the folders in the repository. 
    <br />
    <br />
    <br />
    <a href="https://stanforduniversity.qualtrics.com/jfe/form/SV_4GxtjbJHxrT6v0G">View Demo</a>
    ·
    <a href="https://github.com/mikebrock03/Lifting-The-Bar/issues">Report Bug</a>
    ·
    <a href="https://github.com/mikebrock03/Lifting-The-Bar/issues">Request Feature</a>
  </p>
</div>



<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>



<!-- ABOUT THE PROJECT -->
## About The Project

We want to ensure high engagement with the survey. We also want people to be able to edit the code in the future! So, this repository holds the code and documentation for this survey. 

The goal is for it to be easy to make a cookie-cutter edit and comprehensive enough to make an overhaul.

### Built With

* HTML
* JavaScript

<!-- GETTING STARTED -->
## Getting Started

Log into Qualtrics and open up the project (linked soon).


<!-- USAGE EXAMPLES -->
## Understanding the code

These examples will demonstrate how to use both types of code in this project (HTML and Javascript). HTML is primarily used for text and generic entry pages that do not have custom properties. Javascript is primarily used for pages with custom entry properties.

### HTML

[insert image soon]

To make editing easy, we have utilized Custom CSS so that you can call a "class" that determines a font size / spacing, rather than having to do it everytime. Here is an example of using that: 

```
    <div class="section main-title">What older students shared</div>
```
In this case, in order to change anything about "What older students shared", you must go into the Custom CSS which looks like this:

```
.main-title {
    font-family: Helvetica, sans-serif;
    font-size: 32px;
    font-weight: bold;
    line-height: 1.5;
    text-align: center;
}
```
And you could change any of the respective values. With a Google Search, any of the properties are obvious and similar to what a text editor like Google Docs can do.

So, now you know that "class" calls back to something in Custom CSS and you know how to read CSS, HTML should be straight forward! 

Sometimes, it can get complicated. For example, the emoji list you see above cannot just be done in the same way we saw above. In that case, we call them individually, like in this example: 

```
<div style="margin-top:40px; display: flex; align-items: center;" class="section title">
        <span style="font-size:64px;margin-right:20px;">👩‍🏫</span>
        <div>Students were able to develop positive relationships with teachers and other adults in school.</div>
</div>
```
In this case, there is a space of 40px on top and the text is inherited by the CSS property of "title." However, notice there is a property called "display: flex" and "align-items: center". "Flex" is called to have the items fit side by side and they are "centered" so the emoji is in the middle of the paragraph. 

Often, the best properties to be used will not be obvious but a well-worded Google Search or ChatGPT prompt will help steer you in the right direction.

Here is the whole code for the image above, and you have learned how HTML is used in this project! 

```
<div class="wrapper">

<!-- TO CHANGE THE TEXT BELOW, CHECK THE CLASS "MAIN-TITLE" IN CSS. --->

    <div class="section main-title">What older students shared</div>

<!-- TO CHANGE THE TEXT BELOW, CHECK THE CLASS "NORMAL-TEXT" IN CSS. --->

    <div class="section normal-text">Second, students said that their experience in school got better with time. For example:&nbsp;</div>

<!-- BEGIN LIST OF EMOJIS WITH TEXT --->

<!-- CHANGE SPACE BY ADJUSTING "MARGIN-TOP", CHANGE TEXT BY ADJUSTING "TITLE" IN CSS --->

<!-- EMOJIS ARE TO THE LEFT AND MIDDLE OF THE RESPECTIVE TEXT BY USING "DISPLAY" AND "ALIGN-ITEMS" --->

    <div style="margin-top:40px; display: flex; align-items: center;" class="section title">
<!-- CHANGE EMOJI SIZE BY ADJUSTING "FONT-SIZE", CHANGE TEXT BY ADJUSTING "MARGIN-RIGHT" IN CSS --->
        <span style="font-size:64px;margin-right:20px;">👩‍🏫</span>
        <div>Students were able to develop positive relationships with teachers and other adults in school.</div>
    </div>

    <div style="margin-top:40px; display: flex; align-items: center;" class="section title">
        <span style="font-size:64px;margin-right:20px;">✏️</span>
        <div>Students made progress on their schoolwork.</div>
    </div>

    <div style="margin-top:40px; display: flex; align-items: center;" class="section title">
        <span style="font-size:64px;margin-right:20px;">🧩</span>
        <div>Students were able to get involved in activities and groups that they valued.</div>
    </div>

    <div style="margin-top:40px; display: flex; align-items: center;" class="section title">
        <span style="font-size:64px;margin-right:20px;">🎯</span>
        <div>Students felt confident they were making progress on things that mattered to them.</div>
    </div>

<!-- END OF LIST --->

<!-- AUDIO CONTAINER AT BOTTOM --->

    <div class="audio-next-container"><div class="audio-control-container">
        <audio width="320" preload="auto" height="40" controls="true" class="qmedia" autoplay="true">
            <source type="audio/mp3" src="https://stanforduniversity.qualtrics.com/CP/File.php?F=F_8ufbYQVlq8LuonQ">
        </audio>
    </div>
    </div>
</div>
```
## Javascript

There are two primary places where Javascript is used in this project. First, it is used to add prefilled text as it is not supported by Qualtrics. Second, to make custom data fields (either in multiple choice form or in text).

When clicking on a question and opening up "Javascript", you get presented with a blank text box only containing: 

```
Qualtrics.SurveyEngine.addOnload(function() {
	/*Place your JavaScript here to run when the page is onloading*/

});

Qualtrics.SurveyEngine.addOnReady(function()
{
	/*Place your JavaScript here to run when the page is fully displayed*/

});

Qualtrics.SurveyEngine.addOnUnload(function()
{
	/*Place your JavaScript here to run when the page is unloaded*/

});
```

#### First, we will be implementing prefilled text. 

First, you must create a question container and text area field, which is done like this:

```
// Get the question container
    var container = this.getQuestionContainer();

// Get the textarea field
    var textarea = container.querySelector('textarea');
```

Then, give your pre-filled text  properties similar to how you would in HTML (but in Javascript):

```
 // Pre-filled text
    var preFilledText = "Don't worry about using complete sentences, grammar, or spelling! Just share what you think.";
    textarea.value = preFilledText;
    textarea.style.color = '#3A95FF';
    textarea.style.opacity = '0.6';
    textarea.style.fontSize = '20px';
    textarea.style.fontFamily = 'Helvetica, sans-serif';
```

And finally, have Qualtrics set the variable of the edited text box to the variable "SIB_challenge", which is where we want it stored in the end:

```
    // Add event listener to input box
    textarea.addEventListener('focus', function() {
	// if empty, set value to nothing 
        if (textarea.value === preFilledText) {
            textarea.value = '';
            textarea.style.opacity = '1';
        }
    });

    textarea.addEventListener('blur', function() {
        if (textarea.value === '') {
            textarea.value = preFilledText;
            textarea.style.opacity = '0.6';
	// if empty, set value to prefill text and slightly transparent
        } else {
	// otherwise, set variable to be equal to what user inputted
            Qualtrics.SurveyEngine.setEmbeddedData('SIB_challenge', textarea.value);
        }
    });
```

Notice that our first "if" statement checks to see if the text field is the same as the prefilled text, in which case it does nothing except ensure the variable's value is blank. Otherwise, our variable is updated to what the user inputted.

Putting it all together, we have:

```
Qualtrics.SurveyEngine.addOnload(function() {
    // Get the question container
    var container = this.getQuestionContainer();

    // Get the textarea field
    var textarea = container.querySelector('textarea');
    
    // Pre-filled text
    var preFilledText = "Don't worry about using complete sentences, grammar, or spelling! Just share what you think.";
    textarea.value = preFilledText;
    textarea.style.color = '#3A95FF';
    textarea.style.opacity = '0.6';
    textarea.style.fontSize = '20px';
    textarea.style.fontFamily = 'Helvetica, sans-serif';

    // Add event listener to input box
    textarea.addEventListener('focus', function() {
        if (textarea.value === preFilledText) {
            textarea.value = '';
            textarea.style.opacity = '1';
        }
    });

    textarea.addEventListener('blur', function() {
        if (textarea.value === '') {
            textarea.value = preFilledText;
            textarea.style.opacity = '0.6';
        } else {
            Qualtrics.SurveyEngine.setEmbeddedData('SIB_challenge', textarea.value);
        }
    });
});

Qualtrics.SurveyEngine.addOnReady(function()
{
	/*Place your JavaScript here to run when the page is fully displayed*/

});

Qualtrics.SurveyEngine.addOnUnload(function()
{
	/*Place your JavaScript here to run when the page is unloaded*/

});
```

And now you know how to implement pre-filled text!

#### Next, we will be looking at how to implement a custom multiple choice form.

First, design your choices in a list:

```
const data = [
    { emoji: "🦸🏻‍♂️", text: "Be a good role model for my younger brother or sister" },
	
    { emoji: "💼", text: "Learn skills that could help me get a good job" },
	
    { emoji: "👨‍👩‍👦", text: "Make my parents proud of me" },
	
	{ emoji: "📚", text: "Try my best in school" },
		
	{ emoji: "🎓", text: "Prepare myself for college" },
	
    { emoji: "📈", text: "Help support my family" },
	
	{ emoji: "🎨", text: "Use art or music as a way to express myself" },
	
    { emoji: "❤️", text: "Have good relationships with people" },
    // Add more choices as needed.
];
```

Then, we want to create a container that holds all of the options:

```
// Create container that will hold all of the choices
const container = document.getElementById("choiceContainer");
```

Then for every item in data we want to create a box that will hold the particular option: 

```
// Create choices.
data.forEach((item, index) => {
// create the outer box
    const box = document.createElement("div");
// "choice-box" design properties comes from CSS "choice-box" 
    box.classList.add("choice-box");
```

Inside that box, we want to add and style the emoji and caption. Notice that we have to create the space and style first, then add the actual emoji from data:

```
// create the emoji space on top
    const emoji = document.createElement("div");
// add the emoji with properties from CSS "emoji"
    emoji.classList.add("emoji");
// add the actual emoji
    emoji.innerText = item.emoji;

// create the caption space below the emoji space
    const caption = document.createElement("div");
// choose the style properties from CSS "caption"
    caption.classList.add("caption");
// add the actual text
    caption.innerText = item.text;

// put emoji and caption into the box
    box.appendChild(emoji);
    box.appendChild(caption);
```

Now, we need to listen for when the box is selected, in which we will make the outline blue (from CSS style class "selected") and add it to data using the function "updateEmbeddedData" (which we will cover soon):

```
 box.addEventListener("click", function() {
        this.classList.toggle("selected");
// below is the function to update how to track which box is selected
        updateEmbeddedData();
});
```

Finally, we add the finished box into the parent container:

```
container.appendChild(box);
```

However, the "other" box is not in the data that will be looped through. We need to add it manually in the same way we made the other options, but replacing the emoji header with a title "Other" and the subtitle with an entry box. Because it is the same format as detailed above, here it is all together: 

```
// Create an "Other" input field.

const otherContainer = document.createElement("div");
otherContainer.classList.add("choice-box", "other-container");

// Like the other boxes, the label won't be an emoji, it will be the title "Other"

const otherLabel = document.createElement("div");
otherLabel.classList.add("caption");
// Add 'caption' class to make it look like the rest of the boxes
otherLabel.innerText = "Other:";

// Then, where the subtitle would usually go, we have a text input.

const otherInput = document.createElement("input");

// This "type" is the key to having it appear as an input rather than a subtitle.

otherInput.type = "text";
otherInput.classList.add("other-input");

otherContainer.appendChild(otherLabel);
otherContainer.appendChild(otherInput);

// set the embedded data for the input box to be a different embedded variable from the other options.

otherContainer.addEventListener("input", function() {
Qualtrics.SurveyEngine.setEmbeddedData("important_other", otherInput.value);
});

container.appendChild(otherContainer);
```

Finally, we need to make the function "updateEmbeddedData" that will be called after any option is selected. It loops through all selected items and adds the captions to a single embedded data array.

```
function updateEmbeddedData() {
	// go through every item
	
	const selectedItems = Array.from(container.getElementsByClassName("selected"));
	
	// collect all of the captions from each item
	
	const selectedTexts = selectedItems.map(item => item.getElementsByClassName("caption")[0].innerText).join(", ");
	
	// set that equal to the array "important" in embedded data
	Qualtrics.SurveyEngine.setEmbeddedData("important", selectedTexts);
}
```

All together, we have:

```
Qualtrics.SurveyEngine.addOnload(function()
{
// Options
const data = [
    	{ emoji: "🦸🏻‍♂️", text: "Be a good role model for my younger brother or sister" },
	
    	{ emoji: "💼", text: "Learn skills that could help me get a good job" },
	
    	{ emoji: "👨‍👩‍👦", text: "Make my parents proud of me" },
	
	{ emoji: "📚", text: "Try my best in school" },
		
	{ emoji: "🎓", text: "Prepare myself for college" },
	
    	{ emoji: "📈", text: "Help support my family" },
	
	{ emoji: "🎨", text: "Use art or music as a way to express myself" },
	
    	{ emoji: "❤️", text: "Have good relationships with people" },
    	// Add more choices as needed.
];
	
// Create container that will hold all of the choices

const container = document.getElementById("choiceContainer");

// Create choices.

data.forEach((item, index) => {
	// create the outer box
    	const box = document.createElement("div");
	// "choice-box" design properties comes from CSS "choice-box" 
    	box.classList.add("choice-box");

	// create the emoji space on top
    	const emoji = document.createElement("div");
	// add the emoji with properties from CSS "emoji"
    	emoji.classList.add("emoji");
	// add the actual emoji
    	emoji.innerText = item.emoji;

	// create the caption space below the emoji space
    	const caption = document.createElement("div");
	// choose the style properties from CSS "caption"
    	caption.classList.add("caption");
	// add the actual text
    	caption.innerText = item.text;

	// put emoji and caption into the box
    	box.appendChild(emoji);
    	box.appendChild(caption);

	// listen for when the box is selected
    	box.addEventListener("click", function() {
        this.classList.toggle("selected");
	// below is the function to update how to track which box is selected
        updateEmbeddedData();
    });

	// add the box into the parent container
    	container.appendChild(box);
});
	
// Create an "Other" input field.
const otherContainer = document.createElement("div");
otherContainer.classList.add("choice-box", "other-container"); 

// Like the other boxes, the label won't be an emoji, it will be the title "Other"
const otherLabel = document.createElement("div");
otherLabel.classList.add("caption"); // Add 'caption' class to make it look like the rest of the boxes
otherLabel.innerText = "Other:";

// Then, where the subtitle would usually go, we have a text input.
const otherInput = document.createElement("input");
// This "type" is the key to having it appear as an input rather than a subtitle.
otherInput.type = "text";
otherInput.classList.add("other-input");

otherContainer.appendChild(otherLabel);
otherContainer.appendChild(otherInput);

// set the embedded data for the input box to be a different embedded variable from the other options.
otherContainer.addEventListener("input", function() {
	Qualtrics.SurveyEngine.setEmbeddedData("important_other", otherInput.value);
});

container.appendChild(otherContainer);


// Update embedded data.
function updateEmbeddedData() {
	// go through every item
        const selectedItems = Array.from(container.getElementsByClassName("selected"));
	// collect all of the captions from each item
        const selectedTexts = selectedItems.map(item => item.getElementsByClassName("caption")[0].innerText).join(", ");
        // set that equal to the array "important" in embedded data
	Qualtrics.SurveyEngine.setEmbeddedData("important", selectedTexts);
    }
});

Qualtrics.SurveyEngine.addOnReady(function()
{
	/*Place your JavaScript here to run when the page is fully displayed*/

});

Qualtrics.SurveyEngine.addOnUnload(function()
{
	/*Place your JavaScript here to run when the page is unloaded*/

});
```

Yay! Now you know how to implement a custom multiple choice field in Qualtrics. Once again, you can copy/paste this as a reference or use Stack Overflow/ChatGPT for unique implementations.

#### Custom written response 



<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [x] Add Changelog
- [x] Add back to top links
- [ ] Add Additional Templates w/ Examples
- [ ] Add "components" document to easily copy & paste sections of the readme
- [ ] Multi-language Support
    - [ ] Chinese
    - [ ] Spanish

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a full list of proposed features (and known issues).

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".
Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE.txt` for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Use this space to list resources you find helpful and would like to give credit to. I've included a few of my favorites to kick things off!

* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Malven's Flexbox Cheatsheet](https://flexbox.malven.co/)
* [Malven's Grid Cheatsheet](https://grid.malven.co/)
* [Img Shields](https://shields.io)
* [GitHub Pages](https://pages.github.com)
* [Font Awesome](https://fontawesome.com)
* [React Icons](https://react-icons.github.io/react-icons/search)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
[Next.js]: https://img.shields.io/badge/next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white
[Next-url]: https://nextjs.org/
[React.js]: https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB
[React-url]: https://reactjs.org/
[Vue.js]: https://img.shields.io/badge/Vue.js-35495E?style=for-the-badge&logo=vuedotjs&logoColor=4FC08D
[Vue-url]: https://vuejs.org/
[Angular.io]: https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white
[Angular-url]: https://angular.io/
[Svelte.dev]: https://img.shields.io/badge/Svelte-4A4A55?style=for-the-badge&logo=svelte&logoColor=FF3E00
[Svelte-url]: https://svelte.dev/
[Laravel.com]: https://img.shields.io/badge/Laravel-FF2D20?style=for-the-badge&logo=laravel&logoColor=white
[Laravel-url]: https://laravel.com
[Bootstrap.com]: https://img.shields.io/badge/Bootstrap-563D7C?style=for-the-badge&logo=bootstrap&logoColor=white
[Bootstrap-url]: https://getbootstrap.com
[JQuery.com]: https://img.shields.io/badge/jQuery-0769AD?style=for-the-badge&logo=jquery&logoColor=white
[JQuery-url]: https://jquery.com 
