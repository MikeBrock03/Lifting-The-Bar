
<a name="Lifting the Bar"></a>

<!-- PROJECT LOGO -->
<br />
<div align="center">
 

  <h3 align="left">Lifting the Bar</h3>

  <p align="left">
    Code and documentation on the survey to help young people succeed when they return to school.
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

We want to ensure high engagement with the survey. We also want people to be able to edit the code in the future! So, this repository holds the code and documentation for this survey. The goal is for it to be easy to make a cookie-cutter edit and comprehensive enough to make an overhaul.

### Built With

* HTML
* JavaScript

<!-- GETTING STARTED -->
## Getting Started

Log into Qualtrics and open up the project (linked soon).


<!-- USAGE EXAMPLES -->
## Examples & Usage

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

First, we will be implementing prefilled text. First, you must create a question container and text area field, which is done like this:

```
// Get the question container
    var container = this.getQuestionContainer();

// Get the textarea field
    var textarea = container.querySelector('textarea');
```

Then, set your pre-filled text with properties similar to HTML (but in Javascript):

```
 // Pre-filled text
    var preFilledText = "Don't worry about using complete sentences, grammar, or spelling! Just share what you think.";
    textarea.value = preFilledText;
    textarea.style.color = '#3A95FF';
    textarea.style.opacity = '0.6';
    textarea.style.fontSize = '20px';
    textarea.style.fontFamily = 'Helvetica, sans-serif';
```

And finally, have Qualtrics set the variable [STOPPED HERE]

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
