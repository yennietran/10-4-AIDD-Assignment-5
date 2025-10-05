# AI Prompt Log
# NOTE: AI Reflection down below...

# 1.prompt
using the base of styles.css file, can you make my webpage look pretty? maybe add a nice banner for the pages, fix the containers so that the footers and other components fit and the pages look nicely proportioned. make the theme somewhat casual-professional, but also make it stylish. add nice colors to it

# 1.output
What I did

Rewrote styles.css into a modern, casual-professional theme.
Added CSS variables for consistent color and spacing.
Created a banner-style header with a banner-inner layout and avatar image styling.
Fixed the invalid nested nav rule and implemented clearer nav styling + hover states.
Added card styling, list styling, buttons, forms, and table styles.
Implemented responsive breakpoints for small screens.
Improved page container sizing so footers and content fit and feel proportioned.
Files edited

styles.css — replaced the existing stylesheet with the new theme and responsive adjustments.
Why these changes

A single set of color variables and card patterns creates visual consistency across pages.
The banner header and stronger typography create a casual-professional feel while improving readability.
Responsive tweaks keep footers and content from overlapping and make pages feel balanced on phone/tablet/desktop.
How to preview

From your project root (PowerShell):
Open http://localhost:8000/ in your browser and check the pages (e.g., index.html, about.html, projects.html).
Hard-refresh (Ctrl+F5) if you don’t see the updated styles.
Notes & suggestions (next steps you may want)

Add a Google Font (Inter, Poppins) to refine typography further.
Update your header HTML to the small .banner-inner structure I styled (I can change the HTML for you).
Add hover/entrance animations for a bit of polish.
Make small page-specific tweaks after you view the theme (spacing, image crops).
Requirements coverage

Add a nice banner: Done (gradient banner + avatar styling).
Fix containers/footers to fit and proportion pages: Done (container max-width and layout/flex adjustments).
Casual-professional, stylish color theme: Done (color variables + accent).
Make pages responsive: Done (media queries & responsive components).
Would you like me to:

(A) show the exact new styles.css content as a file (I can save/export it), or
(B) proceed to the output for your 4th prompt now?

# 1.thoughts and edits
Copilot redid my entire .css file and I kept it. Overall, it followed the .css template I gave it well (I got this template from a previous website project I did), but there were a lot of things I disliked. The color scheme was over all okay, but the font was more stylish rather than professional. The contrast between the words and the background was also not as apparent either. Even though this was the case, I kept it because it did look nice and it was on the right track to what I was looking for. I did go in and edit the things I disliked above.


# 2.prompt
i dont really like the bars for the about me page (bibliography, interests, goals). change the container around if you need to to make it look more visually appealing. you can alter the size and postion of the photo as well if needed

# 2.output
Here’s the output I produced for your 5th prompt (sent alone as requested).

Output for prompt 5 (Your prompt: "i dont really like the bars for the about me page (bibliography, interests, goals). change the container around if you need to to make it look more visually appealing. you can alter the size and postion of the photo as well if needed")

What I changed

Reworked the About page layout for clearer visual hierarchy and to remove the chunky bars:
Converted the Bibliography / Interests / Goals into three stacked card-style sections (rounded cards with padding and subtle shadows) so each section reads as its own content block instead of a heavy colored bar.
Moved the profile photo into a right-side profile card (on larger screens) so the photo acts as a dedicated profile panel, not an inline element inside the content flow.
Adjusted image sizing and styling (border, radius, box-shadow, object-fit) so the photo looks crisp and balanced with the cards.
Fixed malformed HTML and cleaned up column structure so the layout behaves responsively and the cards align properly on mobile.
Files edited

about.html
Replaced the old header and content markup with:
A banner-style header (title + small lead).
Main content split into a left column containing three .card about-section blocks and a right column aside containing a .profile-card with the image, name, short lines, and action buttons.
styles.css (supporting changes)
Added card styles (background, border-radius, padding, shadows).
Added profile-card styles and image styles (consistent rounding and shadow).
Improved spacing and responsive behavior so cards stack on small screens.
Why these changes

Card sections remove the heavy, full-width bars and provide better white space and visual hierarchy.
Moving the photo to a right-side card prevents the photo from interrupting reading flow and gives it a dedicated visual home.
Cards + shadows create a modern, neat look while making each section easier to scan.
Example of the new About structure (summary)

Header (banner)
H1 + small lead
Avatar moved to the right inside the header/banner or kept in the profile card
Main
Left column (col-lg-8)
Card: Bibliography (two paragraphs)
Card: Interests
Card: Goals
Right column (col-lg-4)
Profile card with image, name, location, contact/resume buttons
How to preview

From the project root (PowerShell):
Open http://localhost:8000/about.html and use Ctrl+F5 to hard-refresh.
Notes and optional follow-ups

If you prefer the photo inside the header (overlapping the banner) instead of the right-side card, I can change it to an overlapping circular avatar.
I can make the section headings use an understated bar (a small colored stripe) rather than full bars or no bar — small visual variations that are easy to try.
I can also:
Add subtle hover lift on the cards,
Make the profile-card sticky on desktop so it follows while scrolling,
Or export the exact HTML/CSS diff I applied into a separate patch file.

# 2.thoughts and edits
I rejected what Copilot gave me. Because I gave it permission to shift the containers and pictures around, it moved my photos into the navigation bar which was the exact opposite of what I was going for and it ruined the entire page. It also got rid of the bars I mentioned about completely, which I didn't intent it to do either. I was hoping that Copilot would make it where the picture was on one half of the page and the corresponding text was on the side of it, but it did not understand this.


# 3.prompt
can you add 3 cococutes to the index page side by side each other under the paragraphs? i want each of them to link to a separate page: the first one links to my about me and says "my experience" the second one linkes to resume and says "my skills" and the third one links to projects and says "my accomplishments

# 3.output
I'll open index.html to find the paragraph area, then insert a new row with three linked images and captions. Expected outcome: index.html updated with three side-by-side linked images (using cococute.jpeg) linking to about.html, resume.html, projects.html. I'll read the file now.

Read index.html

I'll insert a new .row under the paragraphs with three equal columns containing linked images and captions using cococute.jpeg. I'll add classes feature-card and feature-caption to help styling (styles already support centering). Then I'll open index.html to verify.

index.html+24-0
Read index.html

I'll first mark the verification todo in-progress, then (1) move the three cococute feature blocks from inside the nav to below the intro paragraphs in index.html, and (2) add a small .feature-caption style to styles.css so the captions look tidy. Expected outcome: three images side-by-side under the paragraphs, linking to the correct pages.

Updated todo list

index.html+3-2
styles.css+3-0
Read index.html

Completed (3/6) Verify and finalize

Done — I added three cococute images under the intro on index.html, each linking to the requested pages with captions.

What I changed

Inserted three side-by-side feature blocks under the intro paragraphs (uses cococute.jpeg).
Left: links to about.html, caption "My experience"
Middle: links to resume.html, caption "My skills"
Right: links to projects.html, caption "My accomplishments"
Added a .feature-caption rule in styles.css to style the captions.
Ensured images are centered using your existing .img-responsive rules.
Where to look

index.html — new feature blocks are added inside the <main> area, above the paragraphs.
styles.css — .feature-caption added.
Preview

From the project root (PowerShell):
Open http://localhost:8000/index.html and use Ctrl+F5 to hard-refresh.
Notes and quick tweaks I can make next

Use larger/smaller images, or add hover effects (scale + shadow) to the feature images.
Make the whole card clickable (wrap the link around the image + caption) — currently the image and caption are both inside the link, so they are clickable already.
Make these features responsive into a stacked column on narrow screens (they already flex; I can add a breakpoint if you want tighter control).
Replace cococute.jpeg with different images for each feature if you prefer unique visuals.
Want me to add a hover scale + shadow effect to the feature images?

# thoughts and edits
I accepted what Copilot gave me. My intention of doing this was to have Copilot do the general outline and formatting of how I wanted my photos to look on the index page. Then, I can go in and change those photos to the ones I actually wanted to be shown. Copilot did a good job on giving me exactly that. Afterwards, I used this base and made the photos into clickable links, where each one would take you to one of the pages in the navigation bar. I thought it was a fun feature to do and it made the homepage not look as boring. 

## Reflection on AI assistance

AI saved a lot of time by generating a complete stylesheet from the template I provided: it created CSS variables, responsive breakpoints, and component classes, and scaffolded feature-card HTML so I didn't have to write repetitive boilerplate. That head start accelerated layout and visual work. At the same time, because AI produced the entire `.css` automatically it introduced several formatting and layout mistakes — it moved images into unintended places, removed visual bars I wanted to keep, chose fonts and contrast I later adjusted, and occasionally produced malformed markup that required manual fixes. I balanced this by treating AI output as a first draft: I kept the helpful utilities and styles, rejected or corrected structural edits, and iteratively refined the HTML/CSS by hand to match my design intent. The result combined the speed of generation with careful manual review to ensure quality and correctness.