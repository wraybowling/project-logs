<iframe src="http://player.vimeo.com/video/67390928" class="fixed-aspect-ratio" data-width="16" data-height="9"></iframe>

<p class="intro">What if your webcam captured depth? The Kinect already does. Occlusion Video Chat tickles the question "If we used such a technology to share the same space virtually, what would happen?"<br>The answer: lots of slow motion fist fights.</p>

<h2>Download the Source</h2>
<p><em>Occlusion Video Chat</em> is available as a public repository on Bitbucket:</p>
<a style="repository" href="http://bitbucket.org/wraybowling/occlusion-video-chat/">Occlusion Video Chat on Bitbucket</a>

<h2>Photos</h2>
<img src="img/occlusion-video-chat-11.jpg" alt="Watercolored posters on the wall">
<p>A couple of dancers. (Photo credit: <a href="http://www.flickr.com/photos/bphillipsmith/sets/72157634254691561/">Phil Smith</a>)</p>
<img src="img/occlusion-video-chat-3.jpg" alt="Watercolored posters on the wall">
<p>Watercolored posters on the wall</p>
<img src="img/occlusion-video-chat-4.jpg" alt="Two bros posing together.">
<p>Two bros posing together.</p>
<img src="img/occlusion-video-chat-9.jpg" alt="My dad and Zach in a fist fight. (there were a lot of fist fights!)">
<p>My dad and Zach in a fist fight. (there were a lot of fist fights!)</p>
<img src="img/occlusion-video-chat-6.jpg" alt="The first time <em>Occlusion Video Chat</em> compiled with all of the features operating correctly.">
<p>The first time <em>Occlusion Video Chat</em> compiled with all of the features operating correctly.</p>
<img src="img/occlusion-video-chat-7.jpg" alt="Both cameras pointed at me from opposite directions.">
<p>Both cameras pointed at me from opposite directions.</p>

<h2>An Homage to Z-sorting</h2>
<p>The overall goal of <em>Occlusion Video Chat</em> was to make something that was personal, intimate, and inspiring to the imaginations of adults and children alike. The project was also subtly an homage to one of Computer Graphics' first major accomplishments: The solving of the "visibility problem" with <a href="https://en.wikipedia.org/wiki/Hidden_surface_determination">Z-sorting</a>. The Kinect has single-handedly made depth data accessible to the masses and therefore bridges one of the remaining gaps in the world of special effects. Special effects teams combine live footage with animated objects on a regular basis, painstakingly rotoscoping subjects because of the lack of depth information in their images. <em>Occlusion Video Chat</em> is a lo-fi example of how we may be approaching the end of an era.</p>

<h2>Calibrating the Depth Map</h2>
<iframe src="http://player.vimeo.com/video/49272017" class="fixed-aspect-ratio" data-width="2" data-height="1"></iframe>
<p>Since <em>Occlusion Video Chat</em> takes advantage of both the color and the depth cameras on the Kinect, the two images needed to be synthetically aligned. Most applications blur the depth data slightly to achieve better results. I wanted nice sharp masks and to achieve the above level of detail. Using a technique similar to paralax mapping, the depth image was broken up into slices. Those slices were shifted to match the angle of the color camera, and then layered back ontop of one another. To fill in holes, I used a background plate which is currently captured manually but could also be derived from the farthest recorded points on-screen.</p>
<img src="img/occlusion-video-chat-2.jpg" alt="holes versus no holes">
<p>a depth map with holes still present and my filtered depth map without holes.</p>

<h2>Depth -> Alpha conversion</h2>
<iframe src="http://player.vimeo.com/video/49262732" class="fixed-aspect-ratio" data-width="2" data-height="1"></iframe>
<p>The above video shows two example video feeds A and B. Depth from feed A is converted into transparency before being sent over the network. This was because some streaming video protocols implement alpha support with MPEG.</p>

<h2>Stability</h2>
<p>For SPARKcon, for any other future gallery spaces, or for home use, stability was very important. I wanted to be able to leave <em>Occlusion Video Chat</em> to operate autonomously. The original concept was written in Processing in about three days but it ran very slowly. Refactoring in C++ took sixteen weeks. Instead of relying on the computers' CPUs, OpenFrameworks was picked as the best candidate for its ability to use the GPU. The remaining slowdowns are the result of problems I found with transmitting video over a network. <a href="http://evanosaurus.com/">Evan Kinney</a> attempted to help me understand MPEG encoding but we have so far been unsuccessful. If you can help, please get in touch via Github.</p>
<img src="img/occlusion-video-chat-10.png" alt="">
<img src="img/occlusion-video-chat-5.jpg" alt="">
<p>On rare occasions when <em>Occlusion Video Chat</em> would break, it was because of network latency. We would usually take these opportunities to make clone photos.</p>

<h2>Comparisons to Occlusion Photo Booth</h2>
<p><em>Occlusion Video Chat</em> is the second piece in the <a href="/serial-projects">Occlusion Series</a>. It was done entirely in my free time, and unlike the first installment Occlusion Photo Booth (OPB), <em>Occlusion Video Chat</em> received no grant funding. OCV was very successful in getting across the core concept without the need for explanation, whereas OPB had to be explained to patrons repeatedly. OCV drew from OPB thematically, but shared no other connection in its technology stack or its core concept.</p>
