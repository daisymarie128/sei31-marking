# SEi31 Final Project Marking

## What does your face sound like
### Author: Anthony
Repo: https://github.com/AnthonyGDoueihi/what-does-your-face-sound-like
[Live Site](https://anthonygdoueihi.github.io/what-does-your-face-sound-like/)

#### General comments
Love the app!!! 😍😍😍 Great use of creative coding and loved seeing the final demo! Well done you should be proud for getting a fun application like this working in the week.

#### Code feedback
Your readme is great, good use of image and list of libraries used in the project with links, aces 👍
To improve on this I would advise even though it doesn't require anything like `yarn install` etc but also giving them the basic command of running a local server would be helpful, always assume the audience knows nothing to make things more accessable.

Good use in creating helper functions for yourself. You could take this further however. As you are just using static files, you `main.js` file does get quite long and becomes increasingly hard to read.

At the very bottom you have the draw functions which get repeated quite abit even though it is usually only changing to values.

This could be re-written into something like this:

```js
function drawJaw(sideWidth, camWidth, shiftDown) {
	curveVertex( sideWidth + (camWidth * 0.249), shiftDown + (camHeight * 0.319));
  curveVertex( sideWidth + (camWidth * 0.272), shiftDown + (camHeight * 0.385));
  curveVertex( sideWidth + (camWidth * 0.298), shiftDown + (camHeight * 0.451));
  curveVertex( sideWidth + (camWidth * 0.302), shiftDown + (camHeight * 0.506));
..... etc
	}


function drawFace(){
	drawJaw(sideWidth, camWidth, shiftDown)
```

This will just help witth readability in the future and seperating logic out.

With a reo like this I highly recommend looking into trying and implementing a linter. [Linter](https://eslint.org/). This isn't needed but can help maintain coding patterns in your repo.

Good work, looking forward to seeing more!
