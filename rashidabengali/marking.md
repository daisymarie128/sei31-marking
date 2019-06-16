# SEi31 Final Project Marking

## Speed Type
### Author: Rashida
Repo: https://github.com/rashidabengali/speed_type
[Live Site](https://rashidabengali.github.io/speed_type/#/leaderboard)

#### General comments
I must say I'm very impressed with your final projects, you should be very proud of yourself for what you created in the week. Your project clearly demonstraights how much you've learnt in the course. 

Your presentation was good, you explained all of your features you created, I especially like that your app went the extra mile to not allow copy and pasting in the game, these small features are what truely make something feel finished and complete.
The play with friends feature as well was awesome and is something you should really demo at your meet and greet 🎉🎉🎉

#### Code Feedback
You have a very good readme, clearly explaining how to get your application up and running locally and this is what readmes are designed for so great job 👍

My only improvements for this would be to add one or two sentences explaining what the application does. Also you could consider adding a list of the frameworks and languages you've used for this project.

Consider removing old commented out code from the repo, it gets very hard to read in some places.

Also it's good practice to try and create variables that are descriptive and not short hand for words. This helps a new developer coming to code to be able to read the code without making assumptions about things.
Example in your code would be to rename this to what I assume must be something like Stop Watch? 
`sw.stop();` to `stopWatch.stop()`

Some small things you can do with your css is using short hand copy here:
instead of `margin: 20px 10px 10px 10px;` you could write `margin: 20px 10px 10px;`
Or instead of this `margin: 10px 10px 10px 10px;` write `margin: 10px;`

Try and delete unused methods in your templates with vue. In the Home.vue file there are a few mathods which return nothing
```js
  data() {
    return {
    }
  },
  methods: {

	```
