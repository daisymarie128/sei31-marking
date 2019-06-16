# SEi31 Final Project Marking

## Fit
### Author: Luke Anton
Repo: 

#### General comments
You presented you project very well, you spoke clearly and articulated technical concepts effectively. Great to see you using tools such as Postman to test with. This is something that is used regularly in the industry and is great experience to have. You also explained what you learnt which was great and showed you did some hard work and have formed valid opinions about some of the tech used, like Reacts useState. Job well done! The looked great as well, big clasp for you 👏👏👏

#### Code feedback
You could improve your readme. It's great to see you have a detailed explanation of what the app was for and what it does this is great for people to get a good idea of what the repo does.

However adding build steps and how to get your application running locally is something that should always be added to every readme. Readme files are generally menat to give the new user cloning your repo a good idea of what it does and how to get it running. 

Things to include for next time would be:
- Link to the live site
- Languages and frameworks you might have used.
- Versions of these frameworks
- Setup process. i.e:
	```
	Download [Yarn](https://yarnpkg.com/en/)
	Run yarn install
	yarn start
	```
- You could also include a list of features which are still a work in process.

Becareful when using local urls as links. This can become increasingly hard to maintain and remove when you need to deploy your site.
```
href="http://127.0.0.1:50119/client/index.html"
```


Take a look at how to handle urls for development and production states. Or using framework to handle linking to other pages like Reacts Router and its `Link` method

Awesome to see you using Reacts `<Fragment>` component - keep up the good work 👏

Wonderful use of conditional rendering in the Profiles component 👍

Another thing you could do to improve your code would be to use the `required` attribute which is an out of the box attribute which comes with form elements. You can read more about it here [MDN Form - select  specs](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/select)

Example of what you could refactore. This:
```
<small>* = required field</small>
      <form className="form" onSubmit={e => onSubmit(e)}>
        <div className="form-group">
          <select
            type="text"
            name="location"
            value={location}
            onChange={e => onChange(e)}
          >
            <option value="0">* Location</option>
            <option value="Sydney">Sydney</option>
            <option value="Melbourne">Melbourne</option>
          </select>
        </div>
```

You could write this:
```
      <form className="form" onSubmit={e => onSubmit(e)}>
        <div className="form-group">
          <select
            type="text"
            name="location"
            value={location}
            onChange={e => onChange(e)}
						required
          >
            <option>Location</option>
            <option value="Sydney">Sydney</option>
            <option value="Melbourne">Melbourne</option>
          </select>
        </div>
```
