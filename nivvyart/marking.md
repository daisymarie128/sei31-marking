# SEi31 Final Project Marking

## GitHost
### Author: Adrian
Repo: https://github.com/nivvyart/gitghost
[Live Site]()

#### General comments
I loved your project, the graphs were great and you presented very well. You spoke clearly and explained technical details superbly. Your final project showed you learnt a lot with your time at GA and you should be very proud of yourself. You also shared some very good resources while presenting which was great.


#### Code feedback
Really great readme explaining how to get the application running locally this is one of the main reasons for a readme so good job. Don't forget to also include a live link to the site and perhaps a one sentence description of what the repo does.

You could consider breaking down your components into smaller chunks as well. `Project.js` seems to start getting abit unreadable with the large DOM structure which is being create din there

Also consider reading up on es6 deconstruction methods. This can help with writting less code and helping making things more readable.
instead or writting this out all the time.
```
username={this.props.match.params.username}
repository={this.props.match.params.repository}
startDate={this.props.match.params.startDate}
```

You could deconstruct the props object like so.
```
const { username, repository, startDate } = this.state.match.params;

username={username}
repository={repository}
startDate={startDate}
```

It looks like your code consistency changes through out the component. 
It would be a good idea to get comfortable with learning what javascripts `this` does and what it means in relation to binding things.
i.e some places you write:
```
this._handleUserChange = this._handleUserChange.bind(this);
```

other places you use modern `() => {}` arrow functions instead. Both are fine. but try to stay consistant. And when you get further into your carer you might start seeing more arrow functions being used :)

When using `a` tags that open in a new tag, it's good practice to also add `rel="noopener noreferrer"` for security reasons. You can read more about it [here](https://mathiasbynens.github.io/rel-noopener/)

Overall great work! I loved the graphs!!
