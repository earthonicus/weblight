# Spotlight Focus Tool
<p><strong>Quick install:</strong> drag this button to your bookmarks bar, then click it on any webpage.</p>

<p>
  <a
    href="javascript:(function(){var ID='__spotlight_combo__';var s=document.getElementById(ID);if(s){window.removeEventListener('mousemove',s.__mv,true);window.removeEventListener('keydown',s.__kd,true);s.remove();var hh=document.getElementById(ID+'_help');if(hh)hh.remove();var ds=document.getElementById(ID+'_darkstyle');if(ds)ds.remove();return;}var mode='circle',r=200,lineH=200,dim=0.6,x=innerWidth/2,y=innerHeight/2,darkMode=false,spotlightOn=true;function place(){if(!spotlightOn){s.style.display='none';return;}s.style.display='block';if(mode==='circle'){s.style.width=(r*2)+'px';s.style.height=(r*2)+'px';s.style.left=(x-r)+'px';s.style.top=(y-r)+'px';s.style.borderRadius='50%';}else{s.style.width='100vw';s.style.height=lineH+'px';s.style.left='0px';s.style.top=(y-lineH/2)+'px';s.style.borderRadius='0';}s.style.boxShadow='0 0 0 9999px rgba(0,0,0,'+dim+')';}function toggleDark(){darkMode=!darkMode;var ds=document.getElementById(ID+'_darkstyle');if(darkMode){if(!ds){ds=document.createElement('style');ds.id=ID+'_darkstyle';ds.innerHTML='html,body{background:#111 !important; color:#eee !important;} *{color:#eee !important; border-color:#444 !important;} div,p,span,section,article,nav,header,footer,aside,main,table,td,th,ul,ol,li{background-color:transparent !important;}';document.head.appendChild(ds);}}else{if(ds)ds.remove();}}function toggleSpotlight(){spotlightOn=!spotlightOn;place();}function mv(e){if(mode==='circle'){x=e.clientX;y=e.clientY;}else{y=e.clientY;}if(spotlightOn)place();}function kd(e){var handled=true;if(e.key==='c'||e.key==='C'){mode='circle';if(spotlightOn)place();}else if(e.key==='l'||e.key==='L'){mode='line';if(spotlightOn)place();}else if(e.key==='ArrowRight'&&!e.shiftKey){if(mode==='circle'){r=Math.min(2000,r+20);}else{lineH=Math.min(innerHeight,lineH+20);}if(spotlightOn)place();}else if(e.key==='ArrowLeft'&&!e.shiftKey){if(mode==='circle'){r=Math.max(20,r-20);}else{lineH=Math.max(20,lineH-20);}if(spotlightOn)place();}else if(e.key==='ArrowRight'&&e.shiftKey){dim=Math.min(0.98,+(dim+0.05).toFixed(2));if(spotlightOn)place();}else if(e.key==='ArrowLeft'&&e.shiftKey){dim=Math.max(0,+(dim-0.05).toFixed(2));if(spotlightOn)place();}else if(e.key==='d'||e.key==='D'){toggleDark();}else if(e.key==='s'||e.key==='S'){toggleSpotlight();}else if(e.key==='Escape'){window.removeEventListener('mousemove',mv,true);window.removeEventListener('keydown',kd,true);s.remove();var hh=document.getElementById(ID+'_help');if(hh)hh.remove();var ds=document.getElementById(ID+'_darkstyle');if(ds)ds.remove();if(darkMode)toggleDark();}else{handled=false;}if(handled)e.preventDefault();}s=document.createElement('div');s.id=ID;var st=s.style;st.position='fixed';st.pointerEvents='none';st.zIndex='2147483647';st.background='transparent';st.transition='box-shadow 0.05s,width 0.05s,height 0.05s';document.body.appendChild(s);s.__mv=mv;s.__kd=kd;window.addEventListener('mousemove',mv,true);window.addEventListener('keydown',kd,true);place();var help=document.createElement('div');help.id=ID+'_help';help.innerHTML='<b>Spotlight Controls</b><br>C = Circle<br>L = Line<br>← / → = Resize<br>Shift+←/→ = Dimness<br>D = Dark Mode<br>S = Toggle Spotlight<br>Esc = Exit';help.style.position='fixed';help.style.right='10px';help.style.bottom='10px';help.style.background='rgba(0,0,0,0.7)';help.style.color='#fff';help.style.padding='8px 10px';help.style.font='12px sans-serif';help.style.borderRadius='6px';help.style.zIndex='2147483648';document.body.appendChild(help);})();"
    style="display:inline-block; padding:12px 20px; background:#0077cc; color:#ffffff; text-decoration:none; border-radius:6px; font-weight:bold;"
  >
    Spotlight
  </a>
</p>
  
A simple JavaScript bookmarklet that helps reduce visual clutter on any webpage by limiting what you see to a movable spotlight area.

It is designed to support people who may benefit from a narrower visual focus, including people with ADHD, dyslexia, autism, sensory processing differences, and other neurodivergent profiles. It can also be useful for reading fatigue, concentration, accessibility, and distraction reduction in general.

## What it does

Spotlight Focus Tool places a movable visual mask over the current webpage so you can focus on either:

- a circular spotlight around the cursor
- a horizontal reading line across the page

You can also:

- resize the focus area
- increase or decrease the dimming outside the focus area
- toggle a simple dark mode
- turn the spotlight on or off without leaving the page
- exit instantly with a keypress

## Why this exists

Many webpages are visually noisy. Sidebars, ads, popups, banners, animations, and dense layouts can make reading or concentrating harder than it needs to be.

This tool offers a lightweight way to create a more restricted focus of attention on top of any webpage, without needing a browser extension or account.

## Features

- Bookmarklet-based, no install package required
- Works on top of existing webpages
- Circle focus mode
- Line focus mode for reading
- Adjustable spotlight size
- Adjustable background dimness
- Optional dark mode
- Quick keyboard controls
- Easy to share and fork

## Installation

### Option 1: Use the installer page

Open the included `weblight.html` file in a browser.

Then:

1. Drag the **Spotlight** button to your bookmarks bar
2. Open any webpage
3. Click the bookmarklet to activate the tool

### Option 2: Use the JavaScript directly

Create a new browser bookmark and paste the bookmarklet code from `weblight.html` into the bookmark URL/location field.

## Controls

- **Mouse** → move the spotlight
- **C** → circle mode
- **L** → line mode
- **Left / Right Arrow** → smaller / bigger
- **Shift + Left / Right Arrow** → lighter / darker background dimming
- **D** → toggle dark mode
- **S** → toggle spotlight on/off
- **Esc** → exit

## Who it may help

This project may be useful for:

- ADHD
- Dyslexia
- Autism
- Sensory processing differences
- Visual overstimulation
- Reading fatigue
- Focus and concentration support
- Accessibility use cases
- Study support
- Deep reading on cluttered websites

This is not a medical device or therapeutic claim. It is a simple visual focus aid that some people may find helpful.

## Use cases

- Reading articles without distraction
- Following text line by line
- Reducing visual overwhelm on busy websites
- Supporting study sessions
- Helping keep attention on one part of the screen
- Demoing accessibility concepts quickly via a bookmarklet

## Project goals

- Keep it simple
- Keep it lightweight
- Make it easy for anyone to try
- Support accessibility and neurodivergent-friendly browsing
- Encourage community improvements

## Ideas for future improvements

- Adjustable colour overlays
- Reading ruler mode variations
- Remember saved settings
- Touchscreen support
- Browser extension version
- Accessibility presets
- Better mobile support
- High contrast themes

## Contributing

Contributions, improvements, and accessibility feedback are welcome.

Especially useful areas for support:

- accessibility testing
- neurodivergent user feedback
- browser compatibility fixes
- UI improvements
- better keyboard support
- packaging as an extension

## GitHub description

A simple bookmarklet that adds a movable spotlight or reading line to any webpage to reduce distraction and support focus, accessibility, ADHD, dyslexia, and neurodivergent browsing.

## Suggested GitHub topics

`accessibility` `adhd` `dyslexia` `neurodivergent` `autism` `focus-tool` `reading-tool` `bookmarklet` `javascript` `a11y` `sensory-friendly` `distraction-free` `assistive-technology` `inclusive-design` `visual-focus`

## Licence

Choose the licence that best matches your goal:

- **MIT** if you want maximum reuse and simplicity
- **Apache-2.0** if you want an explicit patent grant as well
- **GPL-3.0** if you want derivatives to stay open source

For a small accessibility utility intended to spread widely, **MIT** is usually the simplest choice.

## Support

If you find this useful, consider:

- starring the repo
- sharing it with accessibility communities
- suggesting improvements
- opening issues for bugs or ideas
