# SEi31 Final Project Marking

## My News
### Author: Monica
Repo: https://github.com/monicamendesmontanha/my-news
[Live Site](https://mmm-my-news.herokuapp.com/)

#### General comments
It was a really great presentation, I loved the fact that you showed your app in a mobile view as thats what it is designed for. Mobile first thinking is very big in the industry and would be great to mention in your interviews.

You were very detailed and enagaging in your presentation, you seemed very comfortable explaining the technical parts of your code which is great. Especially showing us how the crawler worked. Great job Monica, your site is excellent especially with your text to speech and the accessability of it all. Big big claps 👏👏👏

#### Code feedback
You've got a very very good readme and should be proud, the readme isn't apart of the code but is something that is very well respected when it's written well. Good job including a gif showing what the app does, explaining the features and especially how to run your application locally. Great job!
To make it even better you could also consier adding the frameworks/languages you used and the version numbers for each.

`const BACKEND = process.env.REACT_APP_MY_NEWS_API || "http://localhost:8000";`

It's great to see you using env files, good job 👍

It's good to see you understand the concept of this:

`this.handleReadMoreClick = this.handleReadMoreClick.bind(this);`

To take your code further you could consider refactoring these parts to use arrow functions, it's important to learn what they are, and what they do. Because there are places you should and shouldn't use them. Try reading this article to get your head around them and implement them in your future work. [Useful article explaining arrow functions](https://www.sitepoint.com/es6-arrow-functions-new-fat-concise-syntax-javascript/)

So this line:
```js
this.handleReadMoreClick = this.handleReadMoreClick.bind(this);
}

handleReadMoreClick(item, feedId) {
 . . .
 ```

 Could be written as just 

```js
handleReadMoreClick = (item, feedId) => {
```

Becareful using `<>` instead of `<React.Fragment>` this is only because in future code bases you go into you'll have to make sure there using a new enough version of [Babel](https://babeljs.io/) to complie these tags. 

Try avoid using `z-index` where possible, it's useful for some things but can cause problems debugging when used to much, you can generally use other layout methods to get the desired effects with out this.

Great to see you using `rel="noreferrer noopener" target="_blank"` on links that opne in new tabs, good job.

It would be great to see some more functionality around stopping text-to-speech if you accidentally press it - this could also help you practice using accessibility standards like `aria-pressed` for toggle buttons.

For you speech buttons it would be nice to use an `aria-label` for your buttons which use icons rather than text. This will allow screen readers to give a description of what their clicking. [read more on aria-label here](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques/Using_the_aria-label_attribute)
For example it might be: `<button aria-label="play-audio-snippet"`
