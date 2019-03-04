---
{
  uri:'libya-voter-registration',
  collections:['front-end development'],
  hill:100,
  tools:['Django','HTML','CSS'],
  url:'https://libyavotes.ly/login/?next=/check_registration/',
  klout_sum:36,
  scope:'partial',
  freedom:1,
  clients['Caktus Group','High National Elections Commission'],
  references:[
    'https://www.caktusgroup.com/case-study/worlds-first-sms-voter-registration-system/'
  ]  
}
---

I created a new CSS boilerplate for Libya's voter registration web site with the goals of making something that was performant on low-end computers, as well as mobile devices, and had to look correct in English and Arabic without changing the markup. The result is called Sassless and it was successful in deploying as the stylesheet basis for a handfull of sites years after Libyavotes.ly launched.

## The Wildcard
Front-end developers loathe the wildcard, claiming that it has particularly bad performance hits. I chose to embrace the CSS wildcard because it has a specificity ranking of zero, and thus colissions with any kind of overriding selectors is impossible. It was clear to me for many years that this is the way that CSS was meant to be used, and somewhere along the way developers tried to sidestep it to gain a few milliseconds of page paint speed. Unfrotunately, at the time many of the codebases I was working with were being pre-compiled by LESS of SCSS, sometimes exploding into thousands of selectors, essentially cancelling out the savings while making the styles onerous to read manually.
```
* {
	position:relative;
	box-sizing:border-box;
	outline:none;
	margin:0;
	border:0;
	padding:0;
	color:inherit;
	font-size:inherit;
	font-family:inherit;
}
```



Later the project would be open sourced as <a href="https://www.caktusgroup.com/blog/2015/10/28/open-sourcing-smartelect-libyas-sms-voter-registration-system/">SmartElect</a>
