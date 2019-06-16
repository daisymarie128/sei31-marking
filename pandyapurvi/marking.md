# SEi31 Final Project Marking

## Job Board
### Author: Purvi
Repo: https://github.com/pandyapurvi/client_job_board
[Live Site](https://pandyapurvi.github.io/deployment/#/)
#### General comments
Great work presenting you did an awesome job explaining over what you built and the technical aspects of the project. Big claps for you 👏👏👏

#### Code feedback
You had showed good understanding of using React and setting up an application. You should be proud of what you've acheived. 

It was great to seee you using `.map` functions and es6 features throughout your project. Great work.

To take your code further you could 

Make sure to remove old code and commented out things. Plus get rid of console logs. These arn't good things to have in production code.

Consider using String interpolation
instead of this:

`const URL = 'https://server-job-board.herokuapp.com/jobs/'+ job_id +'.json'`

You could write it like this:
```js
const URL = `https://server-job-board.herokuapp.com/jobs/${job_id}.json`
```

Use && logic rendering instead of ise else rendering
Instead of this: 
```js
{
  isEmployer
  ?  <button>Update</button>
  : ''
}
```

Should be this:
```js
{isEmployer && <button>Update</button>}
```
