## 2 Day SASS Project - Responsive Webpage for a Record Label
Sailor Winkelman
12/8/17

1. Two-Day Project Thoughts and Feedback

Process:

* Before the two day project, I knew I wanted to make my own grid using SASS.

* I brought a big piece of paper with me to class on Wednesday to sketch designs on. In the first hours of the project day, I talked with Sam about what we wanted our page to do, and then sketched a mobile, tablet and desktop version of our first design on the big paper. Then, I sketched 2 more designs based on the same idea, on the same big paper.

* We jumped right into wireframing one of the designs using HTML and SCSS. We also created our SASS file structure at this time. Since we had a sketch, we could make a responsive wireframe without content. We worked on this for ~ 2.5 hours. During this process, we identified some of the SASS features we would need to make for our design to behave as planned, such as like a for loop to create the grid based on a column class, and importing partials to organize our code into modules, rather than putting it all in one giant SCSS file. We typed out a version of our 3 designs, and made a table of SASS features we were using or planned to use.

* During the first wireframing phase, determined that we needed to make a "hamburger menu," because we needed to collapse and expand ~3 lists of navigation links in the mobile view. We planned to not use a framework, but agreed we would need to pull in bootstrap if we couldn't find a way to make a collapsible navigation using SASS and CSS only.

* By the end of Wednesday, we had some content pulled in to our one responsive webpage that we wireframed. We also had probably the majority of our SASS functionality implemented, but not segmented out into partials. We had problems with our layout at this time, and we were not meeting our MVP because we could not collapse the navigation for mobile.

* On Thursday morning, we implemented bootstrap. I wish we didn't have to, because I feel my understanding of how the SCSS we were writing was clouded by all the bootstrap classes, negotiating what to use there, etc. It was also kind of sad to have our SASS grid be become unnecessary, because it does something we could have done with bootstrap classes. However, we also had already committed to our design, because our responsiveness assumed the nav could collapse and expand. We spent a lot of time finessing the page once we dropped in bootstrap, to try to get our layout functioning the way it should.

* That left about 3 hours of Thursday to try to get creative with SASS mixins and functions. I think we worked on the page too much already to be so creative, and unfortunately I don't think we made very good use of SASS features to make the code more organized, efficient, or modular and reusable. I didn't feel like I learned alot about SASS the way I did on Monday when we built the color swatch table, but it was an exercise in getting comfortable with a large project with partial files and imports, which feels important.

* I think I'm still figuring out how to efficiently handle planning a larger project, to allow for enough experimentation that I can feel confident moving forward and make good decisions, but not jump right into the work and never look back. I think the code being modular and reusable should be able to lead my design, rather than antagonize it - but that's sort of how this project felt.

* SASS Elements from Wed-Thur and How I Used Them:

<table class="tg">
  <tr>
    <th class="tg-yw4l">SASS Element</th>
    <th class="tg-yw4l">Definition</th>
    <th class="tg-yw4l">Implementation</th>
  </tr>
  <tr>
    <td class="tg-yw4l">for loop</td>
    <td class="tg-yw4l">Loops through index a set number of times, returning a result each time.</td>
    <td class="tg-yw4l">We used a for loop to assign column divs a width value. The value was determined by looping 1-12 times, and dividing the 100% width by the number of columns multiplied by the number of the index.</td>
  </tr>
  <tr>
    <td class="tg-yw4l">variable</td>
    <td class="tg-yw4l">Stores a value that can be changed in one place to impact every place it was referenced.</td>
    <td class="tg-yw4l">We made a _variables.scss partial to store our variables, and referenced them throughout the project. Our grid function used a set max-width variable, and we stored our media query breakpoints in variables to be easier to pull them in to our SCSS, and the same with color values.</td>
  </tr>
  <tr>
    <td class="tg-yw4l">@mixin push--auto</td>
    <td class="tg-yw4l">Mixins are called to an element in SCSS using @include.</td>
    <td class="tg-yw4l">We made a mixin called @push--auto, which applied a left and right margin of "auto" to an element. We used this mixin to center elements on the page.</td>
  </tr>
  <tr>
    <td class="tg-yw4l">@import and partials</td>
    <td class="tg-yw4l">Importing partials to your SCSS output file allows you to organize a directory of project components</td>
    <td class="tg-yw4l">We made directories like "base components  layout  pages vendor abstracts" and used @ import to place them all into our output SCSS file.</td>
  </tr>
  <tr>
    <td class="tg-yw4l">&amp;, nested selector</td>
    <td class="tg-yw4l">Nested selectors in SASS allow you to target the children within the parent element selector. The &amp; is used to reference the parent of the child you are targeting.</td>
    <td class="tg-yw4l">We used nested selectors to target children elements such as the h1 elements included inside the .main-blog-text class. We also used nesting to target elements with a display:none at media breakpoints, like when we took away the hero image's overlaid text when screen is small.</td>
  </tr>
</table>

3. Changing My Approach:
* Re-work design to be SCSS - only (no framework)
* Wireframe on paper using outside - in approach
* Think about the overall structure of the page before content. I'm going to try making a "grid" for all the content of the page and focusing on modular components inside it before I start adding any text, forms, etc.
