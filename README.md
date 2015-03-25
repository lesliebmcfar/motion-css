# Awesome-CSS3-animation
The library of CSS3 animation

<p>Awesome CSS3 animation is a library of animation for your web projects. It works very simply.
            All you need to do is connect the css file and use a specific class to an element that should be animated.
        </p>
<h2>USE</h2>
        
        <p>Connect stylesheet in <span style="color:#D9843E">&lt;head&gt;</span> tag on your site:</p>
        
        <pre>
            <code>
                &lt;link rel="stylesheet" href=<span style="color:#E93838">"awesome.min.css"</span>&gt;
            </code>
        </pre> 

        <p>Add class <span style="color:#E93838">"animation"</span> to an element that should be animated. Now select the kind of animation for your item and add the appropriate class. 
The name of the animation is the class that you have to add.
            For example, I want to add animation appearance to the left. It is called <span style="color:#E93838">"fade-in-left"</span>. Here's how it will look my element:
        </p>
        <pre>
            <code>
                &lt;div <span style="color:#FFCE53;">class</span>=<span style="color:#E93838">"animation fade-in-left"</span>&gt;...
            </code>
        </pre>

        <p>As you may have guessed, I added a <span style="color:#FFCE53;">class</span>=<span style="color:#E93838">"animation fade-in-left"</span>.</p>

        <h1>ADDITIONAL FEATURES</h1>

        <p>If you want to delay the animation, use one of the classes:</p>

<p>
    <span style="color:#E93838">"delay-05s"</span> - 0.5 sec delay,<br>
    <span style="color:#E93838">"delay-1s"</span> - 1 sec delay,<br>
    <span style="color:#E93838">"delay-1-5s"</span> - 1.5 second delay,<br>
    <span style="color:#E93838">"delay-2s"</span> - 2 seconds delay,<br>
    <span style="color:#E93838">"delay-3s"</span> - 3 seconds delay
        </p>

        <p>or add your own</p>
        <pre>
            <code>
<span style="color:#E93838">.delay-Xs</span>
{
    <span style="color:#D9843E">-webkit-animation-delay: Xs! important;<br>
    animation-delay: Xs! important;</span>
}
            </code>
        </pre>

        <p>For endlessly repeating of animation use class <span style="color:#E93838">"replay"</span>.</p>

<p>You can also combine this library with the jQuery, to fully control the animation on the site. For example, you can add the animation class to the element, 
    when it appears in the visible area of the screen.</p>

        <p>To do this, place the following code before the tag <span style="color:#D9843E">&lt;/body&gt;</span>:</p>
        <pre>
            <code>
&lt;script&gt;
	$ (window) .scroll (function () {
	$ (<span style="color:#48BD82">'#elementId'</span>). each (function () {
	var elPosition = $ (this) .offset (). top; 	// Position of the element
	var elHeight = $ (this) .height (); 		// Height of the element
	var windowTop = $ (window) .scrollTop (); 	// Top of the window
	var windowHeight = $ (window) .height (); 	// Height of the window
	if (elPosition < windowTop + windowHeight - elHeight) {
		$ (This) .addClass (<span style="color:#E93838">"animation fade-in"</span>);
	} 						                   // adds the class wheh the element is fully in the visible area of the window
	if (elPosition > windowTop + windowHeight) {
		$ (This) .removeClass (<span style="color:#E93838">"animation fade-in"</span>);
	} 						                   // removes the class when the element is not visible in the window
	if (elPosition + elHeight < windowTop) {
		$ (This) .removeClass (<span style="color:#E93838">"animation fade-in"</span>);
	} 						                   // removes the class when the element is not visible in the window
	});
	});
&lt;/script&gt;
            </code>
        </pre>

    <p>Instead <span style="color:#48BD82">#elementId</span> enter the ID or class of your element. Also replace the class <span style="color:#E93838">"fade-in"</span> to your animation class.</p>

    <p>Remember that for all kinds of entrance animation you need to add to your item <span style="color:#48BD82">id="animation"</span> or css rule <span style="color:#D9843E">"visibility: hidden;"</span>.<br>
    In turn, the class <span style="color:#E93838">"animation"</span> then makes your item is visible. 
        Adding class <span style="color:#E93838">"animation"</span> necessarily to any animation, because it contains <span style="color:#D9843E">"animation-fill-mode: both"</span>, 
which prohibit return your item to its original position after the end of the animation.</p>
