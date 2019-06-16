# SEi31 Final Project Marking

## GadBay
### Author: Ben
Repo: https://github.com/bennnym/gradbay
[Live Site](https://bennnym.github.io/gradbay/)

#### General comments


#### Code feedback
Good readme, very detailed, don't forget to also include a how to run the repo locally too.

Maybe consider using a linter in your next project to help with code formatting. This helps to keep lines readable and force good practices.
[ES Lint - good widely used](https://eslint.org/)

Consider turning large confusing rendering logic into small handler functions.
```
salePrice && !list ?
							<div>Sale Price: <span className='tab-small-headings'>${salePrice}</span>  </div> : list ? <div>Reserve Price: <span className='tab-small-headings'>${salePrice}</span>  </div> : <></>}
```

Consider breaking into down to something like this:
```
const renderSalePrice = () => {
  return (
    <div>
      Sale Price: <span className='tab-small-headings'>${salePrice}</span>
    </div>
  )
}

const renderReservePrice = () => {
  return (
    <div>Reserve Price: <span className='tab-small-headings'>${salePrice}</span>
  )
}

.....
....

return (
  <div>
      {salePrice && !list && renderSalePrice()}
      {salePrice && list && renderReservePrice()}
  </div>
)
```

This just helps with code structure and readability, which is very important.

It's cool to see you using Reacts latest update with `useState`, ofr your interviews and such it would be great to try implementing things using the older way `this.setState` and formulate why you like one over the other. (this is just for other ways to push your coding skills further - you've done an awesome job implementing react. Great work!!)


