<iframe src="http://www.youtube.com/embed/y_e-9q_KHpQ" class="fixed-aspect-ratio" data-width="2" data-height="1"></iframe>

<p class="intro">In 2009 I flew to Amsterdam, attended the Blender Conference, and gave a talk on puppets. Yes, puppets.</p>

<p>Puppets that use computer graphics as a means of entertaining audiences had been around since the mid-1980s. But even in the late 2000s when I gave the above presentation, they were still largely unexplored with only a few exceptions.</p>

<p>In my presentation I attempt to explain what digital puppets are, why they are important to keep exploring, and showcase my own experiments.</p>

<a href="https://docs.google.com/document/d/13-PpKKsVyA-Vnn072YpMcZdy7IZYBJfKnTzf5DFzb7g">Read the full research paper</a>

<p class="intro">Here are a few excerpts from my talk's notes:</p>

<h2>Where Did the Digital Puppet Come From, And Why is it a Big Deal?</h2>
<p>So here's the first topic: Where did this stuff come from? I think the simple answer is it came from the need for motion capture, and it came from videogames. Full body motion capture has been around for a while. Plenty of production studios use it for feature films and videogames use it a lot. I'm going to mostly ignore motion capture because it's nothing I (or most of the people in this room) have the capacity or budget for. There's another kind of digital puppetry however that involves something called a waldo. The term was coined by Jim Henson's company who came up with the first one for their show Fraggle Rock in the mid-80's. Traditionally speaking, it looked like a mitten but as time went on, "waldo" has become a generic term for any specialized controller that's used to remotely work a puppet.</p>

<h2>Introducing Raul</h2>
<p>A joystick controls the nodding and turning of his head. The second joystick controls the movements of his jaw. All of his facial expressions (which are shape keys) are being controlled by a directional pad. Up is happy, and down is unhappy. Left is confused, and right is surprised. The left joystick controls the nod  and turn on his head, and the right joystick controls the openning, closing, and shift of his jaw.</p>

<p>My choice of tools for Raul were as follows: 1, the blender game engine because you can control the progress of an Action with a variable, and a playstation 3 controller because of the high number of analog inputs it provides with a lot of variety, ergonomics, and portability, and its relative low cost compared to a professional input device.</p>

<p>The videogame controller is very often the starting point for a digital puppeteer. All that is required is finding some sort of way to hotwire the joysticks and buttons in to a 3D animation package, which can be the tricky part. In raul's case, absolutely everything going on is being first passed through GlovePIE to convert the controller's proprietary analog signals in to OSC, and then in Blender, python does the second half of the job to convert all the OSC signals to each respective variable.</p>

<h2>Connections With Blender</h2>
<p>So why all this talk about the cutting edge of the puppetry world? just as steve whitmire applied his muppet techniques to Waldo C Graphic, I believe that each production is born with a completely different set of needs. And the flexibility of input mapping that was once-upon-a-time a feature that would make it in to the Blender 2.5 series could make this high level of puppetry possible as a by-product of only a few small features. First, and foremost, the ability to have Blender communicate with OSC. This is something that might end up being handled with python since I've already proved that scriptlinks make that sort of functionality possible, but it would surely have a benefit to have midi controller binding happen with just as much ease as most music software handles it. Second, which is just as important as the first, is the ability to record input for an indiscriminate amount to IPO curves. Though not all of these features are immediately necessary, I think by next year Mango could greatly benefit from progress in these areas, and thus production studios mixing live action (be it digitized or not) with animation can begin to bridge the gap between keyframed movement, and the movement of the human body.</p>
