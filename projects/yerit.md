<img src="../img/yerit-1.jpg">
<p class="intro"><em>YERIT</em> is a 3-player game about hillbillies that want to eat Doritos.</p>

<a href="https://github.com/wraybowling/YERIT">View YERIT on Github</a>

<h2>Design &amp; User Testing Intertwined</h2>

<p>Game design of <em>YERIT</em> was about removing everything that wasn't benefitting gameplay the same way simple board games tend to be made of simple shapes and a good set of rules.</p>

<p><em>YERIT</em> was designed to be small enough that it could take advantage of the fact that it was presented in a public space where players were coming and going with a high frequency. New versions were pushed roughly every ten minutes over the course of an afternoon while simply observing players struggle with bugs that would become apparent through gameplay. The result was a game that transformed from being mildly fun to extremely fun within a single day.</p>

<img src="../img/yerit-2.jpg">

<h2>Built with SVG and Javascript</h2>
<p>Scalable Vector Graphics (SVG) are a largely underutilized web technology, and so YERIT was built with SVG as an exercise in its use. The application kept memory usage static by never creating or destroying any elements in the DOM &mdash; they are only ever repositioned. The aforementioned technique seemed to work quite well. The game never dropped below 60fps on the meager computer it was running on.</p>

<img src="../img/yerit-4.jpg">
<img src="../img/yerit-3.jpg">
