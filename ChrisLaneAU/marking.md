# SEi31 Final Project Marking

## Pocket Money
### Author: Chris
Repo: https://github.com/ChrisLaneAU/pocket-money-tracker-api
[Live Site](https://project3.chrislane.now.sh/)

#### General comments
You presented very well, and were confident in speaking about technical aspects of your application, this is great to see as it shows you put in the hardwork and learned quite a bit. It was impressive to see you learn Typescript for your final project, and you walked through your process and learnings wonderfully. You had a nice clean design to boot you should be stocked with what you accomplished throughout your 12 weeks! You also did a fantastci job talking through your test coverage and the table it outputs for you. 
🎉🎉🎉

#### Code feedback
Very well written readme, though also consider adding alink to the server repo as well, and vic-versa.

There are some places where your using conditional rendering where you write it like so:
```js
const progress: React.ReactNode =
	currentPage == "dashboard" ? (
      <></>
    ) : (
		 <>
      <h2 className="view-panel-progress-heading">
			...etc...

return (
    <section className="view-panel">
      {backButton}
      <MainImage image={image} description={name} currentPage={currentPage} />
      <ul className={listClasses}>{renderButtons()}</ul>
      <Name currentPage={currentPage} name={name} />
      {progress}
      {modalWindow}
    </section>
  );
```

You should write it instead with a the `&&` logical operator, instead of returning an emtpy div. something like this:
```
const renderProgress = () => {
	<>
        <h2 className="view-panel-progress-heading">
          <span className="view-panel-progress-heading-span">Progress:</span>
          {` $${progressVal} / $${currentGoal.price}`}
        </h2>
        <ul className="view-panel-progress-list">
          {Object.values(currentGoal).length ? (
            renderProgressIndicators()
          ) : (
            <></>
          )}
        </ul>
      </>
			}
....

return (
    <section className="view-panel">
      {backButton}
      <MainImage image={image} description={name} currentPage={currentPage} />
      <ul className={listClasses}>{renderButtons()}</ul>
      <Name currentPage={currentPage} name={name} />
      {currentPage === "dashboard" && renderProgress}
      {modalWindow}
    </section>
  );
```

The same goes for places where you've imported seperate components and are creating new functions to render them.
shorten this:
`const backButton: React.ReactNode =
    currentPage == "dashboard" ? <></> : <BackButton />;`

to just be this:
```
return (
   {currentPage === "dashboard" && <BackButton />}
	 )
```

Becareful using `z-index: 10000` no matter what the value is you've set. `z-index` can cause many bugs later with rendering and should be avoided as much as possible (but sometimes it must be used)

It's awesome to see you writting tests and what youve written is already a great start but to take it further in the future, consider writting tests which test the different functions you have in files and that the methods in side them are working.

Overall great job buddy!
