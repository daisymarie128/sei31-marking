# SEi31 Final Project Marking

## TriTone
### Author: Hugh
Repo: https://github.com/hluscombe/TriTone
[Live Site](https://hluscombe.github.io/TriTone/)

#### General comments
LOVE ITTT!! 😍😍😍
Great idea, and am obviously bias that I love that you tried out Three.js.
You did a great job presenting and runing through trouble points and what you learned. I also really liked that your talked over some of the libraries you used and that you've formulated opinions about them, keep it up.


#### Code feedback
You had a very good readme that was descriptive and explained all your libraries and frameworks used good job, also don't forget to include a how to run the app locally as well.

For future reference always delete old unused code, it's not great to see in code bases and can make things very confusing and hard to follow.

React and Three.js have always been a pain to deal with together, but good job at getting it all working in the end, claps for you 👏

I saw you've got all the object that you needed to create, this can't be avoided sometimes but can be refactored into something a little more readable.
You could consider creating helper functions outside of the main scope which you just call when you need them.

Also consider moving some of these into seperate files to break down the complexity in the file. files getting longer than 250-350 are what start to get very bloated.

For example all of these objects you created could be made in a seperate file and exported.
```
		// object 5
    const coneGeometry = new THREE.ConeBufferGeometry( 1, 3, 30 );
    const coneMaterial = new THREE.MeshLambertMaterial( {color: '#147ACC', wireframe: false} );
    const cone = new THREE.Mesh( coneGeometry, coneMaterial );
    cone.rotation.x = -1.5
    cone.position.set(0,2,-4)

		export default cone;
```

Then in your `animation.js` file you can simply import it in and use it.
