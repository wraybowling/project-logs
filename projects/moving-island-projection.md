<iframe src="http://player.vimeo.com/video/21630800"></iframe>

<p><a href="http://movingisland.org">Moving Island</a> is a new building in downtown Raleigh that my friends Adam &amp; Chris are running. It's been featured in <a href="http://www.indyweek.com/indyweek/in-raleighs-moving-island-two-artists-try-to-make-the-space-local-governments-havent/Content?oid=1983442">Indy Weekly</a>, and <a href="http://www.newraleigh.com/articles/archive/moving-island-2011-buoyancy-benefit/">New Raleigh</a>. The atmosphere at Moving Island is one that encourages DIY, creative outlet, and technical innovation.  The Moving Island Projection (MIP) is a <a href="/tools#Processing">Processing</a> sketch I wrote as a light show for their "Buoyancy Benefit" and future events.</p>

<p>MIP implements three different elements. First, it is a VJ tool that plays back frame-by frame animations. Second it is a drawing tool for creating fthose frame-by-frame animations in realtime while it runs. Third, it is a system for managing those animations on 3D projected triangles to match the environment that's being projected on to.</p>

<img src="/img/moving-island-projection1.jpg">

<h2>Animation</h2>
<p>MIP's style is one that is loose and rough, but also fun and endearingly childish. Some compared it to "MS Paint." Most of the animations only hold three to five frames. There are 26 animation buffers available &mdash; one for each letter on the keyboard.</p>

<h2>Drawing</h2>
<p>I wrote the software to be more like an animation studio than a VJ setup. Any individual triangle can be selected (visualized by a yellow border). I can then draw on the current frame using my wacom tablet and keyboard shortcuts for color selection. Each frame is automatically stored to disk for later use on any other triangle.</p>

<h2>3D Projection</h2>
<p>The program uses nine triangular canvases &mdash; one for each key on the number row (zero deselects). Each triangle could be placed on to any surface in the room by stretching its corners individually which effectively keystoned each animation to the surface it lit. This method helped a lot with the fact that I wasn't sure where in the room they would put me, how widely the projector would throw on to the walls, or what walls the projector would be most effective on.</p>

<img src="/img/moving-island-projection3.jpg">

<h2>Performing</h2>
<p>Synchronizing animations on MIP involves holding down a letter, and pressing a number to assign the selected animation to a triangle. Occasionally, we would select a triangle of to the side and draw a new animation which temporarily disables its participation in the VJing so that both actions can be done at the same time.</p>

<h2>MIP's Future</h2>
<p>Reception for MIP was widely accepted as a success, and future adaptations and improvements are planned. MIP is planned to be part of future events at Moving Island, and is travelling with me to {Re}Happening 2011 in Black Mountain, NC.</p>
