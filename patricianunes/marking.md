# SEi31 Final Project Marking

## Chrome Extension
### Author: Patricia
Repo: https://github.com/patricianunes/super-chrome-extension

#### General comments
Great presentation, you explained things well and I love your enthusiasm. You should be proud of what you created you did an excellent job. Also loveeeeee your rick and morty images 👏👏👏

#### Code feedback
It was great to see you adding `alt` tags to your images for accessability, though you could take this further by adding more detailed descriptions for the `alt` tag instead of logo. :) 

Becareful when setting heights for elements. Setting heights should generally be avoided unless it's absolutely necessary.

Also looking at your weather app you created you could consider breaking up your DOM elemnts into smaller functions to make things more readable.
is this: 
```
{props.city && props.country && (
      <p className="weather__key">
        Location:
        <span className="weather__value">
          {props.city}, {props.country}
        </span>
      </p>
    )}
```

Could be written like this:
```
renderLocation = () => {
 return (
      <p className="weather__key">
        Location:
        <span className="weather__value">
          {props.city}, {props.country}
        </span>
      </p>
		)


... 

{props.city && props.country ** renderLocation()}
```
