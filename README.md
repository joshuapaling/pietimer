#Pietimer

Pietimer injects a canvas element into the page which has an ever reducing pie shaped timer. Once the timer is complete a callback function is performed.

Checkout <http://www.northfieldx.co.uk/pietimer> for a demo


##Usage

The pietimer canvas element will be injected *into* the specified element.

	$('#element').pietimer(); // Will place pietimer inside #element
	$('#element').pietimer('start');

At any point you can pause it:

	$('#element').pietimer('pause');

And restart it (ie, continue from when it was paused):

	$('#element').pietimer('start');

You can also reset it before it's finished:

	$('#element').pietimer('reset');

When the pie timer finishes, or is reset, you can start it again!

Don't forget to pass some options and a callback!


##Options

	$('#element').pietimer({
		seconds: 5,
		color: 'rgba(255, 255, 255, 0.8)',
		height: 40,
		width: 40,
		growingPie: false
	},
	function(){
		alert('boom');
	});


**height** and **width** will be inherited from the parent element and so are optional.

**color** will accept any value that the canvas element accepts including hex values like #ffffff

if **growingPie** is true, then the pie will start empty, and grow to full. If false, the pie will start full, and shrink to empty.