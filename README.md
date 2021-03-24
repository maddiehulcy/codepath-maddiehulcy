# Pre-work - _Memory Game_

**Memory Game** is a Light & Sound Memory game to apply for CodePath's SITE Program.

Submitted by: **Maddie Hulcy**

Time spent: **3** hours spent in total

Link to project: (https://glitch.com/edit/#!/codepath-prework-maddiehulcy)

## Required Functionality

The following **required** functionality is complete:

- [x] Game interface has a heading (h1 tag), a line of body text (p tag), and four buttons that match the demo app
- [x] "Start" button toggles between "Start" and "Stop" when clicked.
- [x] Game buttons each light up and play a sound when clicked.
- [x] Computer plays back sequence of clues including sound and visual cue for each button
- [x] Play progresses to the next turn (the user gets the next step in the pattern) after a correct guess.
- [x] User wins the game after guessing a complete pattern
- [x] User loses the game after an incorrect guess

The following **optional** features are implemented:

- [x] Any HTML page elements (including game buttons) has been styled differently than in the tutorial
- [ ] Buttons use a pitch (frequency) other than the ones in the tutorial
- [ ] More than 4 functional game buttons
- [x] Playback speeds up on each turn
- [x] Computer picks a different pattern each time the game is played
- [ ] Player only loses after 3 mistakes (instead of on the first mistake)
- [ ] Game button appearance change goes beyond color (e.g. add an image)
- [ ] Game button sound is more complex than a single tone (e.g. an audio file, a chord, a sequence of multiple tones)
- [ ] User has a limited amount of time to enter their guess on each turn

The following **additional** features are implemented:

- [ ] List anything else that you can get done to improve the app!

## Video Walkthrough

Here's a walkthrough of implemented user stories:

![](https://i.imgur.com/1wnxCM7.gif)
![](https://i.imgur.com/kqxntLk.gif)

## Reflection Questions

1. If you used any outside resources to help complete your submission (websites, books, people, etc) list them here.
   https://developer.mozilla.org/en-US/docs/web/javascript/reference/global_objects/math/random

2. What was a challenge you encountered in creating this submission (be specific)? How did you overcome it? (recommended 200 - 400 words)
   I encountered some issues implementing the computer-generated random pattern for the game. At first, I struggled trying to directly manipulate pattern variable. Then I decided to create a new array and return it at the end of the function. However, this also presented issues as I was used to the C++ syntax for arrays, and was trying to access locations in the new array using bracket notation, but I had not yet specified its size. To fix this problem, I used push to add a new element into the array. Then, I could push a randomly generated number between 1 and 4 inclusive using Math.java to populate the array in a for loop that ends after 8 iterations so that the size of the array is 8. I checked that the function was working by using console.log, then assigned that random array value to the pattern variable with the line pattern = generatePattern(); in the startGame() function. I then used console.log(pattern) to ensure that the random pattern was successfully assigned to the pattern variable. At this point, I tested the game several times to make sure that it was actually random and to ensure that this implementation did not inadvertantly mess up other aspects of the game.

3. What questions about web development do you have after completing your submission? (recommended 100 - 300 words)
   What are the challenges and solutions to working on web development with a team? For this project, I was constantly checking the preview screen to see the effects of the changes in my code, but I can imagine this would be challenging if multiple people were working on the same project. I’m also interested in web development frameworks, like Angular and React. What are the advantages and challenges to using these frameworks? Also, how is the syntax and workflow different when using frameworks versus the approach I used on this project with HTML, CSS, and Javascript? My ability to create a simple but elegant game in just a few hours really got me excited about the possibilities of these skills on a much larger scale.

4. If you had a few more hours to work on this project, what would you spend them doing (for example: refactoring certain functions, adding additional features, etc). Be specific. (recommended 100 - 300 words)
   First, I would play around with the CSS to make the page align more with the principles of responsive design. The page looks good on a small screen like the side view in Glitch, or on a mobile phone, but when I had the game in full screen on my laptop, all its features were forced into the top left corner of the screen. I would want the size of the elements to adapt better to the size of the screen and align more in the center. I would also like to implements "levels" to the game. As the player advanced to the next level, the pause time would decrease and the length of the pattern and number of buttons would increase. This would add some more stakes and depth to the game.

## License

    Copyright [MADDIE HULCY]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
