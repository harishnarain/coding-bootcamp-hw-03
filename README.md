# Password Generator - Homework Assigment 3

This application generates a random password based on user-selected criteria. This app will run in a browser and feature dynamically updated HTML and CSS powered by JavaScript code. It will also feature a clean and polished user interface and be responsive, ensuring that it adapts to multiple screen sizes.

## Objective
AS AN employee with access to sensitive data
I WANT to randomly generate a password that meets certain criteria
SO THAT I can create a strong password that provides greater security

## Acceptance criteria
* GIVEN I need a new, secure password
* WHEN I click the button to generate a password
* THEN I am presented with a series of prompts for password criteria
* WHEN prompted for password criteria
* THEN I select which criteria to include in the password
* WHEN prompted for the length of the password
* THEN I choose a length of at least 8 characters and no more than 128 characters
* WHEN prompted for character types to include in the password
* THEN I choose lowercase, uppercase, numeric, and/or special characters
* WHEN I answer each prompt
* THEN my input should be validated and at least one character type should be selected
* WHEN all prompts are answered
* THEN a password is generated that matches the selected criteria
* WHEN the password is generated
* THEN the password is either displayed in an alert or written to the page

## Files included
|File|Relative Path|Description|
|---|---|---|
|index.html|index.html|Main application|
|style.css|assets/css/style.css|Main stylesheet|
|index.js|assets/js/index.js|All handler functions|
|passgen.js|assets/js/passgen.js|Password generating logic and algorithms|

## Accessing the site
Please visit the [site](http://www.harishnarain.com/coding-bootcamp-hw-03/) hosted on GitHub Pages.

## Screenshot
![Screenshot 1](https://github.com/harishnarain/coding-bootcamp-hw-03/blob/master/Screenshot1.png)

## Algorithm used
1. Make each unicode character set it's own JavaScript object called a collection that maintains it's state (selected or not) and it's content (characters used).
2. Based on the selection, the appropriate collections will be pushed into an available collection set.
3. When a password is generated:
	* Alternate through each collection when generating characters in password
	* Run a Durstenfeld shuffling algorithm after generating the password

Durstenfeld shuffling algorithm is an optimized version of the Fisher-Yates shuffling algorithm and has a O(n) linear time complexity. Here is the algorithm implemented in JavaScript:
```javascript
// Run Durstenfeld shuffle algorithm on array
const shuffleArray = (array) => {
  for (let i = array.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    const temp = array[i];
    array[i] = array[j];
    array[j] = temp;
  }

  return array;
};
```

## License
Due to the nature of this exercise, no license has been included.

## Tools used
* [GitHub](https://github.com/) - Code repository and page hosting via GitHub Pages
* [Visual Studio Code](https://code.visualstudio.com/) - For editing and authoring code
* [Prettier](https://prettier.io/) - For opinionated code formatting
* [Chrome Devtools](https://developers.google.com/web/tools/chrome-devtools) - For editing pages on the fly and diagnosing problems
* [iTerm2](https://www.iterm2.com/) - For all my terminal needs on macOS
* [MacDown](https://github.com/MacDownApp/macdown) - For creating the README.md and all things Markdown related