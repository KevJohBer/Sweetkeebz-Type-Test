# SweetKeebz Typing Test

This website, as the name suggests, is a typing test. It measures how many words per minute (WPM) you type. It also tracks the number of keystrokes that are correct aswell as the number of keystrokes which are incorrect. This website is perfect for anyone who would like to polish up their touchtyping skills or for anyone who just wants to stimulate their hands. 

![Typing test on multiple devices](assets/images/multiple-devices.jpg)

## Features

### Typing area

The first thing you will see on the page is 3 rows of randomly selected words that pops up at the center of the screen. When you type the words out, the characters you type changes color bisque if they are correct and red underlined if they are incorrect. The letter you are currently on is also highlighted with a bisque background to indicate which letter you are supposed to type.

![](assets/images/paragraph.jpg)

### Timer and restart

Below the paragraph, you can see the number 30 aswell as a circular arrow. The number 30 is a timer that counts down to 0 as soon as you begin typing. When the timer reaches 0, the user will be unable to type and the final result of the test will be displayed below. The circular arrow is a restart button. You can either click it or press tab + enter to restart. When restarted, the page will load 3 new rows of text and the timer will wait for you to begin typing again.

![](assets/images/timeandrestart.jpg)

### Results

Below the timer and restart section, you can see three symbols. First to the left is a check mark and represents the number of correct keystrokes that you entered. In the middle is an x symbol. This represents the amount of incorrect keystrokes that you have entered. To the far right, it says WPM, which is an acronym for Words Per Minute. This measures how fast you type. It does this by taking your number of correct keystrokes and dividing it by 5 and normalizing the result to a minute (since the test is 30s).

![](assets/images/resultarea.jpg)

### Caps lock warning

The website checks if caps lock is on and alerts the user as this can interefere with the accuracy of the test if not used properly.

![](assets/images/capslockon.jpg)

### Change themes

at the bottom of the UI we see a clickable pallette icon. If you click it, the website will cycle between 3 unique color themes, first one being inspired by sand, second one being inspired by pizza and the last one being inspired by wood.

![](assets/images/theme-change-button.jpg)
## Testing

The website has been tested on Chrome, Safari and Microsoft edge without any issues. 

Firefox and Opera does not support webkit so the text wont blur when the time is up.

The website has been tested for responsiveness using devtools device toolbar and mobile devices

I have tested other typing tests such as monkeytype and 10fastfingers to make sure that the words per minute results are consistent and accurate to the user.

![](assets/images/lighthousetest.jpg)

### Validator testing
* HTML 
    * The website HTML passed the official W3C validator without any errors
* CSS
    * CSS passed the jigsaw validator without any errors
* JavaScript
    * JS code passed the JShint validator. It does not like the 'let' keyword however.
        * Metrics
        * There are 15 functions in this file.

        * Function with the largest signature take 1 arguments, while the median is 0.

        * Largest function has 23 statements in it, while the median is 3.

        * The most complex function has a cyclomatic complexity value of 5 while the median is 1.

## Unfixed bugs

* There are currently no known bugs

## Fixed bugs

* Each time a finished row was removed, 1 point was added to the mistake counter. This was because each time a row was removed, the program would change the input value to '' (empty string), which the program then interpreted as a mistake as there is no '' span. I solved this by simply subtracting one mistake point each time a row is removed.

* Each time a finished row was removed, the first character would not get highlighted. The problem was that the code that adds the highlight, is also the one that removes it. I solved this problem by moving the code that adds and removes the highlight below the code that added the new row. This way the highlight is added after the row is complete so it is not prompted to remove the highlight.

## Deployment

* The website was deployed to Git Hub pages.
    * In the Git Hub repository, navigate to the Settings tab
    * From the source section drop-down menu, select the Master Branch
    * Once the master branch has been selected, the page will be automatically refreshed with a detailed ribbon display to indicate the successful deployment.

The live link can be found here: https://kevjohber.github.io/Sweetkeebz-Type-Test/
## Credits

* The code to make the characters react to keypresses and timer was based on [Typing Speed Test Game in HTML CSS & JavaScript](https://www.youtube.com/watch?v=Hg80AjDNnJk)

* The design was Inspired by [Monkeytype](https://monkeytype.com/)

* Icons in the restart and result area are taken from [Font Awesome](https://fontawesome.com/)