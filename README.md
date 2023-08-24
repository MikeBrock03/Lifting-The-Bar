
# Lifting the Bar 🚀
 

  ## Introduction 🤝


  <p align="left">
    Howdy, fellow Lifting the Bar researcher! 
	  
Here, you will find the code and documentation for the survey we distribute to students reintegrating into school. This document is designed to take you through how we have created our code in Qualtrics (the survey engine) so that future edits and overhauls can be made! To see the code for every question, just click through the folders in the repository. 
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

Log into Qualtrics and <a href="https://stanforduniversity.qualtrics.com/survey-builder/SV_3WMGla3ynz7osPI/edit">open up the project.</a>


<!-- USAGE EXAMPLES -->
## Understanding the code

These examples will demonstrate how to use both types of code in this project (HTML and Javascript). HTML is primarily used for text and generic entry pages that do not have custom properties. Javascript is primarily used for pages with custom entry properties.

### HTML

To make editing easy, we have utilized Custom CSS so that you can call a "class" that determines a font size/spacing, rather than having to do it everytime. Here is an example of using that: 

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/WhatOlderStudentsShared.png" alt="What older students shared" width="500" style="padding: 20px;" />


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

So, now you know that "class" calls back to something in Custom CSS and you know how to read CSS, HTML should be more straightforward and organized! 

However, sometimes, it can get complicated. For example, this emoji list cannot just be done in the same way we saw above. 

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/EmojiList.png" alt="Emoji List" width="500" style="padding: 20px;" />

In that case, we call them individually, like in this example: 


```
<div style="margin-top:40px; display: flex; align-items: center;" class="section title">
        <span style="font-size:64px;margin-right:20px;">👩‍🏫</span>
        <div>Students were able to develop positive relationships with teachers and other adults in school.</div>
</div>
```
In this case, there is a space of 40px on top, and the text is inherited by the CSS property of "title." However, notice there is a property called "display: flex" and "align-items: center". "Flex" is called to have the items fit side by side and they are "centered" so the emoji is in the middle of the paragraph. 

Often, the best properties to be used will not be obvious but a well-worded Google Search or ChatGPT prompt will help steer you in the right direction.

Here is the whole code for the image above, and you have learned how HTML is used in this project! 

```
<div class="wrapper">

    <div class="section main-title">What older students shared</div>

    <div class="section normal-text">Second, students said that their experience in school got better with time. For example:&nbsp;</div>

    <div style="margin-top:40px; display: flex; align-items: center;" class="section title">

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

    <div class="audio-next-container"><div class="audio-control-container">
        <audio width="320" preload="auto" height="40" controls="true" class="qmedia" autoplay="true">
            <source type="audio/mp3" src="https://stanforduniversity.qualtrics.com/CP/File.php?F=F_8ufbYQVlq8LuonQ">
        </audio>
    </div>
    </div>
</div>
```
## Javascript

There are two primary places where Javascript is used in this project. First, it is used to add prefilled text as it is not supported by Qualtrics. Second, to make custom data fields (either in multiple-choice form or in text).

When clicking on a question and opening up "Javascript", you get presented with a blank text box only containing: 

```
Qualtrics.SurveyEngine.addOnload(function() {
	/*Place your JavaScript here to run when the page is loading*/
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

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/prefilledText.png" alt="Prefilled text" width="500" style="padding: 20px;" />

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

#### Next, we will be looking at how to implement a custom multiple-choice form.

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/customMultipleChoice.png" alt="Custom multiple choice" width="500" style="padding: 20px;" />

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/customMultipleChoice2.png" alt="Custom multiple choice 2" width="500" style="padding: 20px;" />


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

We want to add and style the emoji and caption inside that box:

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

Notice that we have to create the space and style first, then add the actual emoji from the data.

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

However, the "other" box is not in the data that will be looped through (which just consist of emojis). 

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/customMultipleChoice2.png" alt="Custom multiple choice 2" width="500" style="padding: 20px;" />

We need to add it manually in the same way we made the other options, but replacing the emoji header with a title "Other" and the subtitle with an entry box. Because it is the same format as detailed above, here is the whole function to make the "other" input: 

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

Notice that a Qualtrics function is used and a Javascript operator ".map" and ".join". While ".map" can iterate through an array and ".join" connects them with commas, the function to use is not always obvious! Therefore, it is always encouraged to Google or StackOverflow or ChatGPT your particular use case! 

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

<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/customWrittenResponse.png" alt="Custom written response" width="500" style="padding: 20px;" />





Qualtrics usually has what you need when it comes to text input, particularly single line response, multiple lines, essay text box, and hidden password. However, we wanted to create a carousel where users could scroll through cards -- almost like a phone book or business cards. This is the use case detailed for this example.

First, like before, we have to create a container that is going to hold our whole custom element:

```
// Create a container to hold the cards
const container = document.createElement("div");
container.id = "cardContainer";
container.style.width = "65%";
container.style.height = "400px";
container.style.display = "flex";
container.style.margin = "0 auto";
container.style.justifyContent = "center";
container.style.alignItems = "center";
container.style.position = "relative";
this.getQuestionContainer().appendChild(container);
```

Notice these elements look like CSS ones, but in JavaScript's style.

Next, we need to create the previous/next button that users will click to go through their cards:

```
// Create navigation buttons
const prevButton = document.createElement("button");
prevButton.textContent = "<";
prevButton.style.position = "absolute";
prevButton.style.top = "50%";
prevButton.style.transform = "translateY(-50%)";
prevButton.style.left = "5px";  // decrease this value to move the button closer to the box
container.appendChild(prevButton);

const nextButton = document.createElement("button");
nextButton.textContent = ">";
nextButton.style.position = "absolute";
nextButton.style.top = "50%";
nextButton.style.transform = "translateY(-50%)";
nextButton.style.right = "5px";  // decrease this value to move the button closer to the box
container.appendChild(nextButton);
```

Notice that we use the standard JavaScript "button" library (in createElement) and simply append it to our container. 

Now, we create the data fields that we want the user to input to. For our case, we want them to input three adults. We are about to build the cards, so we create an empty array:

```
const data = ["Adult 1", "Adult 2", "Adult 3"];
let cards = [];
```

Next, we create a card for each item of data! It seems extensive, but we are just making styling components, then creating a title and text input options for their name and job title. Finally, we append it to our empty array "cards" and to the container:

```
    data.forEach((adult, index) => {
        // Create a card for each adult
        const card = document.createElement("div");
        card.classList.add("card");
        card.style.backgroundColor = "#2387FC";
        card.style.borderRadius = "10px";
        card.style.padding = "10px";
        card.style.margin = "10px";
        card.style.width = "350px";
        card.style.height = "350px";
        card.style.display = "flex";
        card.style.flexDirection = "column";
        card.style.alignItems = "center";
        card.style.justifyContent = "space-evenly";
        card.style.color = "white";
        card.style.position = "absolute";
        card.style.left = "50%";
        card.style.top = "50%";
        card.style.transform = "translate(-50%, -50%)";
        card.style.visibility = (index == 0) ? "visible" : "hidden";

        // Create title for card
        const title = document.createElement("div");
        title.textContent = adult;
		title.style.fontSize = "30px"; // add this line to increase the size of the "Adult" text
        card.appendChild(title);

        // Create input for name
        const nameInput = document.createElement("input");
        nameInput.placeholder = "Name";
        nameInput.id = "name" + index;
		nameInput.style.height = "40px";  // increase this value to make the input field larger
		nameInput.style.width = "300px";
        card.appendChild(nameInput);

        // Create input for job
        const jobInput = document.createElement("input");
        jobInput.placeholder = "Job";
        jobInput.id = "job" + index;
		jobInput.style.height = "40px";  // increase this value to make the input field larger
		jobInput.style.width = "300px";
        card.appendChild(jobInput);

        cards.push(card);
        container.appendChild(card);
    });
```

Then, we create logic to determine which card to show based on if the user clicked on the next or previous button along with what "index" they are on at that moment! 

```
   let currentIndex = 0;

    // Event handlers for navigation buttons
    prevButton.onclick = function() {
        if(currentIndex > 0) {
            cards[currentIndex].style.visibility = "hidden";
            currentIndex--;
            cards[currentIndex].style.visibility = "visible";
        }
    };

    nextButton.onclick = function() {
        if (currentIndex < cards.length - 1) {
            cards[currentIndex].style.visibility = "hidden";
            currentIndex++;
            cards[currentIndex].style.visibility = "visible";
        }
    };
```

Great! You now know how to design a custom input (particularly a carousel) in Qualtrics! Now, for our use case, we needed to have verification to ensure that the user inputted at least two names. If they do not, we don't want to give them access to the "next" button.


<img src="https://github.com/MikeBrock03/Lifting-The-Bar/blob/main/images/nextButton.png" alt="Next button" width="500" style="padding: 20px;" />



First, we want to make the next button.
```
const qualtricsNextButton = document.querySelector(".NextButton");
```
Then, we have a function checkInputs that will go through the existing array and note how many names have something filled in.

```

const checkInputs = function() {
let filledNames = 0;
let name_adult = [];

for(let i=0; i<3; i++) {
    const nameValue = document.getElementById("name"+i).value;
    const jobValue = document.getElementById("job"+i).value;

    if (nameValue) {
	filledNames += 1;
	name_adult.push({ name: nameValue, job: jobValue });
    }
}
```

When counting that, if it is less than 2 (our desired amount), we want to not show them the nextButton. If this somehow gets bypassed, we also have an error message.

```

if (filledNames < 2) {
    qualtricsNextButton.disabled = true;
    errorMessage.textContent = "Please fill out at least two names.";
    errorMessage.style.display = "block";
} else {
    qualtricsNextButton.disabled = false;
    Qualtrics.SurveyEngine.setEmbeddedData("name_adult", JSON.stringify(name_adult));
    Qualtrics.SurveyEngine.setEmbeddedData("filledNames", filledNames.toString());
		
		for(let i = 0; i < name_adult.length; i++) {
		Qualtrics.SurveyEngine.setEmbeddedData("adult_name_" + (i + 1), name_adult[i].name);
		}
		
    errorMessage.style.display = "none";
}
};
```

We will run "checkInputs" after every change to an element:

```
for(let i=0; i<3; i++) {
document.getElementById("name"+i).addEventListener("input", checkInputs);
document.getElementById("job"+i).addEventListener("input", checkInputs);
}
```

### Congratulations! 

I think this will get you set up well to contribute to the LTB project. We have covered basic HTML, Javascript usage in Qualtrics and the ways I have leveraged it to make custom multiple choice functions, prefilled text, and custom writte responses. Qualtrics is quite a closed system, so being creative in it is hard, but I hope this is a good start!


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ROADMAP -->
## Roadmap

- [X] Create documentation
- [X] Add photos 
- [ ] Add separate files with the code 
- [ ] Add "components" document to easily copy & paste sections of the readme for different use cases.

See the [open issues](https://github.com/MikeBrock03/Lifting-The-Bar/issues) for a full list of proposed features (and known issues).

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

Michael Brockman - [@michaelnbrock](https://twitter.com/michaelnbrock) - mikebrockman [at] stanford.edu

Project Link: [https://github.com/MikeBrock03/Lifting-The-Bar](https://github.com/MikeBrock03/Lifting-The-Bar)

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

Anmol & Vicky & Joey & Luciana & Alexandra & Zahara & Greg Walton & all of the many wonderful days in building 420!

<p align="right">(<a href="#readme-top">back to top</a>)</p>
