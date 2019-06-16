# SEi31 Final Project Marking

## spectrify
### Author: Thomas
Repo: https://github.com/thomashexton/spectrify

#### General comments
Well done with graduating and finishing your final project, you presented well and clearly explained the pain points in the projects and what you learnt. Well done! 👏👏👏 Also loved your simplistic design and great color choices!!

#### Code feedback
You have a great detailed readme, which is awesome.
But don't forget to add key things a readme needs like Languages/Frameworks used and the versions of them. One sentences explaining what the repo is. How to run your project locally.

Good job on using `async` and `await` functions in your javascript code, this is a good thing to know when entering the job market.

Consider using sting interpolation instead of stings.
ie this: `createAuthorizedRequest( "GET", "https://api.spotify.com/v1/artists/" + artistId, `

Could be re-written as
```js
createAuthorizedRequest( "GET", `https://api.spotify.com/v1/artists/${artistId}`,
```

Consider cleaning up the repo and removing usued code and comment out lines or console logs - these arn't great to have in production code.

You had a good set up of controllers and your Ruby code looks great, well done.
