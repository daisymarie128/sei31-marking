# SEi31 Final Project Marking

## mufflr
### Author: James
Repo: https://github.com/jamaspy/mufflr-cart
[Live Site](https://mufflr-apparel.netlify.com/)

#### General comments
Your final project looked awesome. Very nicely designed and you had great functionality, your project clearly showed you learnt alot in your time at GA so claps to you 👏👏👏

It was nice to see you explore frameworks like Gatsby and Contenful and you executed it very well, nice job.

#### Code feedback
It looks like you've got a good understanding of how React works and how this and bind works with functions. 
Too push yourself further you could try refactoring some components to not use this: `this.handleNameChange = this.handleNameChange.bind(this);` anymore and instead try and use `() => {}` arrow functions.

Be very careful using `dangerouslySetInnerHTML`. This can be harmful if a user hijacks this. An XSS attack is usually associated with this method. You can read more about it here [XSS info](https://www.owasp.org/index.php/Cross-site_Scripting_(XSS))

Was great to see you thining about SEO as well, good job.

Careful with uploading access tokens to github in future, im not sure which one you've used so it might be fine, but just for future reference always try to keep these seperate.


