# Accessibility Interview Questions  
These questions try to stay away from asking people to recite specifications, or rattle off screen reader hot keys. Those can easily be looked up on the job. Instead these questions try to act as conversation starters, to gain insight into how someone solves problems, and interprets accessible, inclusive user experiences.

Questions are grouped into three buckets: [General](#general), [Technical](#technical), and [Design](#design). These categories may be a mistake, but we're going with it for now. If you have ideas for categories, and questions in general, please [let us know](https://github.com/scottaohara/accessibility_interview_questions/issues)! Ideally a candidate would be able to answer questions from each category.


## General
- Who benefits from accessibility?
  - All users, customers and stakeholders in a web application's life are 
  benefactors of the work in achieving accessibility requirements and goals, 
  each for different reasons which converge on the description, explanation, 
  development and interpretation of purposeful and successful web application 
  features. The properties of an accessible web application are perceivability,
  operosity or operability, usability and robustness. Historically, however, 
  users of assistive technologies have been excluded from participation in 
  web applications, primarily, due to undertheoretization and lack of research 
  regarding the technologies as well as their ability circumstances, cognitive,
  neurological and physiological, whether it involves blindness, color 
  interpretation, tactile capabilities, as well as cultural constraints involving 
  linguistic and ethnic norms which appeal to the majority at the cost of minority 
  populations who might encounter or use web applications.
- How would you define inclusive and/or universal design?
  - Inclusive design involves consideration of both vertical and lateral thinking 
  as well as circumstance-based thinking, insofar as these modes of interaction 
  with web applications may be realized at the cost of others if they are designed 
  in a certain way. Lateral thinking styles involve analogical reasoning whereas 
  vertical thinking generally involves deductive reasoning and perceiving. 
    + Can you provide an example? (does not need to be web related)
    + Circumstances may compromise fundamental experience with a web application, such 
    as using a web application in an urgent crisis that may cause a user not to perceive 
    web page elements as clearly or use them as effectively. Lateral thinking involves 
    enhancing or encouraging analogical reasoning to discover and draw inferences about 
    the state of the web application based on visual and feedback web page elements. 
    Vertical thinking involves encouraging patterns that reflect deductive reasoning 
    patterns like linear flow sequences, user interface wizards and modal windows.
- How has your approach to accessibility changed over time?
  - I began only focused on semantic HTML but eventually realized that data 
  itself must be augmented with accessibility requirements involving 
  hypermedia as the engine of application state (HATEOAS), beyond merely 
  developing DOM-based solutions that may be subject to cross-browser 
  compatibility constraints.
- Name some ways responsive/mobile first design can affect accessibility.
  - In terms of perceivability and operability mobile-first designs can create 
  accidental side-effects where web page elements are not visually presented 
  or they become unusable (since mobile clients or devices may not support 
  various ARIA features available in dominant browsers). In some cases, modal 
  windows, e.g., may not render as effectively or performatively as they would 
  in a desktop setting, since performance requirements are different under the 
  mobile context; this is also a matter of robustness. If semantic HTML is 
  used, the negative consequences for perceivability and usability can be 
  reduced, but this may not guarantee that operability is at parity with a 
  desktop experience.
- What are some user experience (UX) concerns to be aware of when using iconography in user interfaces (UI)?
  - Iconography can sometimes affect perceivability if they orient the user 
  visually in the wrong way; other times they can be treated as "user 
  interface imagery" by the developer and go undescribed using ARIA labels, 
  which effectively turns them into blackholes for blind users of assistive 
  technologies like screen readers or users who have low-vision who may also 
  use such technologies. Users with cognitive disabilities may not, depending 
  on the icon chosen, adequately interpret those icons so as to act in the 
  expected manner that the developer builds or the designer plans.
- What assistive technologies (ATs) are you familiar with (desktop + mobile)?
    + What do you feel is your skill level with these AT(s)? 
- What are skip links?
    + What benefit(s) do they provide? 
    + What are some of their limitations?
- What are some of the tools available to test the accessibility of a website or web application?
- What is WCAG?
    + What are the differences between A, AA, and AAA compliance?
- How can using plain language benefit the accessibility of a project?
- Describe appropriate instances to use a link, vs a generic button, vs a submit button.
- Describe ways to indicate an element or component's state that aren't entirely reliant on visuals.
- How can carousels be problematic for users with disabilities?
- How would you convince your Manager to allocate some funds to do an accessibility external audit?
- Describe a situation where a coworker may have been resistant to accessibility or inclusive design best practices.
    + How were you able to work with them to mitigate such issues?
    + What sort of strategies do you use in situations like these to help educate coworkers?


## Technical
- What methods would you use to find an element's accessible name?
- What is the accessibility tree?
- Why are rems or ems preferable to pixels for setting type size?
- Why is it important to allow the viewport to be resized, and/or zoomed?
- How is the `title` attribute exposed to assistive technologies?
    + What kind of elements can `title` attributes be used on?
    + What sort of information is appropriate for use with the `title` attribute?
- Describe a scenario where you might need to use `aria-describedby`.
- What is a focus trap, or focus trapping? Describe an instance of when you'd need focus trapping, and how it can be an accessibility failure if not used appropriately.
- Describe a situation where one might need to add or modify the focusability of an element by using the `tabindex` attribute.
- What are landmark regions and how can they be useful?
- In what situations might you use a toggle button, vs a switch control, vs a checkbox?
- Describe methods to hide content:
    + From all users.
    + From only screen reader users.
    + From sighted users, but not screen reader users.
    + And why you might do so.
- Describe an instance of inappropriately using ARIA attributes.
- Aside from screen readers, what other assistive technologies can be affected by use of ARIA? How?
- What is the difference between `hidden`, `aria-hidden="true"` and `role="presentation"` or `role="none"`?
- Describe instances where you might need to use `aria-live`.
    + What values (such as `assertive` or `polite`) might you give the attribute in different situations?
- How would you mark-up an icon font or SVG that was for decorative purposes?
- How is CSS pseudo content treated by screen readers?
- What is the purpose of the `alt` attribute for images? 
    + Can you describe the effect of an empty `alt`, and/or the lack of the attribute, on an image?  
    + In what instances might an empty `alt` or no `alt` be appropriate?
    + How might alternative text for an image vary, depending on the context the image is used in?
    + Since `svg`s don't accept the `alt` attribute, how can one provide alternative text for these graphics?
    + Do you need to supply an image an `alt` attribute if used witin a `figure` with a `figcaption`?
- Describe the steps you take in reviewing or auditing a website or application for accessibility?
- Describe an instance where an automated test would not flag a blatant accessibility error?
- When should you use or recommend <abbr>ARIA</abbr> roles or attributes to solve an accessibility issue?
- Describe your process for figuring out if an accessibility bug is due to a developer, browser, or assistive technology error?
- What is the difference between `legend`, `caption` and `label` elements?  
     + What are their similarities?
- Describe the purpose of heading and header elements, and how they are useful in websites and applications. 
- Describe how you'd handle a single page web app should and managing focus when changing routes.
- Name an ARIA attribute that requires either a child/parent relationship or a pairing role.
- What is your understanding of "accessible name computation" and how it affects modifying the way screen readers announce certain content?
- What are some issues with modifying normal scrolling behavior? For example: infinite scrolling or scrolljacking.
- Some ARIA widgets are presently best supported on devices with physical keyboard, rather than mobile/touch interfaces.  Are you aware of any widgets that would be described this way, and why?


## Design
- Talk about the pros and cons of flat and [skeuomorphic design](http://whatis.techtarget.com/definition/skeuomorphism) trends in regards to accessibility.
- Explain the importance of color contrast in designing for inclusion.
- Besides `:hover`, name other states an actionable element (links, buttons, form controls, etc.) could have styles for, and why providing them is important?
- When might it be appropriate to remove the visual outline from a focused element?
- If a form or form field were to return an error message, where might you want those error messages to be located?
- How can utilizing animation in an interface affect the user experience?
- Explain how you could make an infographic accessible for screen reader users.
- Why is color alone insufficient to draw attention to actionable elements, or to convey state?
- What are some of the inclusive UX problems that need to be solved when content (static or actionable) is revealed on `:hover`, and how would you propose solving for them?


## Have a question to add?
[Create an issue](https://github.com/scottaohara/accessibility_interview_questions/issues), or [submit a pull request](https://github.com/scottaohara/accessibility_interview_questions/pulls) for consideration.


## Thank you
Thank you to [all contributors](https://github.com/scottaohara/accessibility_interview_questions/graphs/contributors).  
Special shoutout to [Eric Bailey](https://github.com/ericwbailey) and [Ashley Bischoff](https://github.com/handcoding) for many contributions not recorded by GitHub.
