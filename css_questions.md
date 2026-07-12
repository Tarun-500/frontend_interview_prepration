# CSS Interview Questions — Deduplicated & Organized

Cleaned from the original list: duplicates removed, questions grouped by topic, and missing but commonly-asked questions added (marked ✨ **New**).


## Fundamentals & Box Model

1. What are the different types of CSS?
2. What is the CSS Box Model?
3. What is Intrinsic Sizing?
4. What is CSS Painting Order?
5. How does box-sizing: border-box work internally?
6. Explain GPU Acceleration in CSS.
7. What are contain, content-visibility, and will-change?
8. What is min-content, max-content, and fit-content?
9. What is the difference between min-width, width, and max-width?
10. What is currentColor in CSS?
11. What is the difference between inherit, initial, unset, revert, and revert-layer?
12. Which CSS properties are inherited by default?
13. What is the difference between display: inline, inline-block, block, and contents?
14. Explain the CSS Painting Order.
15. What is the difference between filter, backdrop-filter, mix-blend-mode, and opacity?
16. What is the difference between clip-path and mask?
17. What is CSS Scroll Snap and how does it work?
18. How does the calc() function work?
19. How do you implement Dark Mode using only CSS?
20. How would you organize CSS for a project with 500+ components?
21. How does Shadow DOM affect CSS styling?
22. What is native CSS Nesting and how is it different from SCSS Nesting?
23. What is the difference between @import and <link rel="stylesheet">?
24. What are Safe Area Insets (env(safe-area-inset-*))?
25. How do you customize browser scrollbars using CSS?
26. How do you create visible focus states without affecting design?
27. How would you organize CSS for a project with 1000+ components?
28. How are percentage values calculated in nested layouts?
29. How does the browser resolve conflicting CSS rules?
30. What happens when CSS fails to load?
31. How does the browser recalculate styles after a CSS change?
32. How do browser rendering engines (Blink, Gecko, WebKit) differ?
33. How does translate3d() trigger GPU acceleration?
34. What is forced synchronous layout?
35. How do you reduce layout shifts caused by dynamic content?
36. How do you prevent CSS duplication across components?
37. How do you create reusable utility classes?
38. How would you build equal-height cards without JavaScript?
39. How would you implement a masonry layout using CSS?
40. How would you build a custom toggle switch using CSS?
41. How would you implement skeleton loading using CSS?
42. How would you create a shimmer loading effect using CSS?
43. How would you create a glassmorphism UI using CSS?
44. How would you create a neumorphism UI using CSS?
45. How would you build a print-friendly page using CSS?
46. If given a legacy CSS project with 20,000+ lines, how would you refactor it?
47. What happens when a CSS file contains invalid syntax?
48. Why are IDs considered more specific than classes?
49. Can CSS be considered blocking? Why?
50. Why do browsers block rendering while downloading CSS?
51. What is the difference between runtime theming and build-time theming?
52. How would you style third-party components without modifying their source code?
53. What are the biggest CSS challenges you've faced in production, and how did you solve them?
54. How does the browser calculate the final computed style of an element?
55. What is the difference between Specified, Computed, Used, and Actual values in CSS?
56. What are CSS Initial Values, and where are they defined?
57. How does the browser resolve percentage-based widths and heights?
58. How are percentage margins and paddings calculated?
59. What is Progressive Enhancement in CSS?
60. What is Graceful Degradation in CSS?
61. How do CSS Layers improve maintainability in enterprise applications?
62. What is the difference between place-items, place-content, and place-self?
63. What is the difference between align-items, align-content, and align-self?
64. What is the difference between justify-items, justify-content, and justify-self?
65. What is the difference between gap, row-gap, and column-gap?
66. What is the difference between ease, ease-in, ease-out, ease-in-out, linear, and cubic-bezier()?
67. What is the difference between translate(), translate3d(), and translateZ()?
68. What CSS features still have inconsistent browser support?
69. How do you debug browser-specific CSS issues?
70. How do you support users with reduced motion preferences?
71. What CSS techniques improve readability and usability?
72. If you were designing CSS from scratch today, what would you change and why?
73. How would you review another developer's CSS in a code review?
74. What CSS features released in the last 2–3 years have had the biggest impact on frontend development, and why?
75. If you had to design the next version of CSS, what limitations of the current specification would you solve, and how would you implement the solution?
76. How does the browser determine the optimal order for style calculation, layout, paint, and compositing when thousands of DOM nodes change simultaneously?
77. Difference between display: none, visibility: hidden, opacity: 0, and content-visibility: hidden.
78. How does vertical-align work?
79. How does all: unset work internally?
80. Difference between unset, revert, revert-layer, and initial.
81. What happens when the browser encounters unknown CSS properties?
82. Why is CSS considered a declarative language?
83. What happens when the browser encounters an invalid CSS value?
84. What is the Shrink-to-fit algorithm?
85. How does the browser resolve Auto Width?
86. How does the browser resolve Auto Height?
87. What is the Min-Max Content Contribution algorithm?
88. What is Fragmentation in CSS?
89. What is Multicolumn Layout?
90. What is CSS Regions? (Historical)
91. How does Writing Mode affect layout calculations?
92. What is FOIT?
93. What is FOUT?
94. What is FOFT?
95. Which CSS properties create new rendering layers?
96. What are CSS Anchor Functions?
97. How do browser engines parallelize rendering?
98. What is CSS Dead Code Elimination?
99. How would you build your own CSS preprocessor?
100. How would you implement CSS Hot Module Replacement (HMR)?
101. How would you migrate from SCSS to native CSS?
102. How would you design CSS for Web Components?
103. Which current CSS specification has the biggest limitation, and how would you improve it?
104. What is the difference between outline and border? ✨ **New**
105. What is the resize property and how does it work? ✨ **New**
106. What are CSS counters (counter-reset, counter-increment) used for? ✨ **New**
107. What is the difference between list-style and ::marker? ✨ **New**

## Selectors & Specificity/Cascade

1. What is the difference between a pseudo-class and a pseudo-element?
2. What is the Universal Selector (*)?
3. What are the performance implications of complex CSS selectors?
4. Explain the CSS Cascade.
5. Explain CSS Specificity with examples.
6. What are Cascade Layers (@layer)? Why were they introduced?
7. What is the difference between :is(), :where(), :has(), and :not()?
8. Explain the :has() selector with practical examples.
9. How do browsers evaluate CSS selectors internally?
10. Are descendant selectors slower than class selectors?
11. What are ::part and ::slotted selectors?
12. How does the browser match CSS selectors?
13. Which selector matching algorithm do browsers use?
14. How do CSS specificity and the cascade work together?
15. How do CSS layers (@layer) help solve specificity wars?
16. What happens when multiple stylesheets define the same selector?
17. Can pseudo-elements (::before, ::after) be used on SVG elements?
18. Suppose a page contains 10,000 DOM elements. How does the browser efficiently match CSS selectors, and which selectors should be avoided?
19. Design a CSS strategy for an application with 5,000+ reusable components that ensures minimal bundle size, no specificity conflicts, excellent runtime performance, easy theming, high maintainability, strong accessibility, support for server-side rendering (SSR), and support for micro-frontends.
20. Suppose a page has 20 stylesheets, 5,000 CSS rules, and 100,000 DOM elements. How does the browser efficiently match selectors, and what are the biggest performance bottlenecks?
21. What is the difference between child (>), descendant ( ), adjacent sibling (+), and general sibling (~) selectors?
22. How does the :nth-child() algorithm work internally?
23. Difference between :nth-child() and :nth-of-type().
24. How does :scope work?
25. What is the :empty selector?
26. What is the origin order (User Agent → User → Author → !important)?
27. How many CSS selectors are considered too many?
28. How does CSS selector caching work?
29. What are CSS Scope (@scope) rules?
30. What are CSS Cascade Layers best practices?
31. Explain the CSS Origin Cascade (Author, User, User-Agent).
32. How do !important rules interact with Cascade Layers?
33. What is Selector Weight?
34. How do browsers resolve selector conflicts with equal specificity?
35. What is the difference between Cascade Order and Specificity?
36. How do Attribute Selectors work internally?
37. Which selectors are considered expensive and why?
38. How is specificity calculated numerically (inline, IDs, classes, elements)? ✨ **New**
39. What is the :dir() pseudo-class? ✨ **New**
40. What is the :target pseudo-class and when is it used? ✨ **New**
41. What is :focus-within and how does it differ from :focus-visible? ✨ **New**

## Layout — Positioning, Stacking & Formatting Contexts

1. What creates a new Stacking Context?
2. Why doesn't z-index work sometimes?
3. Explain Block Formatting Context (BFC).
4. Explain Inline Formatting Context (IFC).
5. Explain Flex Formatting Context (FFC).
6. Why doesn't position: sticky work? Explain all possible reasons.
7. What is the difference between overflow: hidden, overflow: clip, overflow: auto, and overflow: scroll?
8. Why doesn't overflow: hidden clip an absolutely positioned child in some cases?
9. Why does position: fixed behave differently inside a transformed parent?
10. Why doesn't position: absolute position relative to the expected parent?
11. Why do images overflow their containers even with width: 100%?
12. How do you debug stacking context and z-index issues in DevTools?
13. A modal has z-index: 99999 but still appears behind the navbar. Why?
14. position: sticky is not working. List every possible reason.
15. Why is a child element overflowing its parent despite overflow: hidden?
16. Why does text-overflow: ellipsis sometimes fail?
17. How do CSS transforms affect stacking contexts?
18. Why does transform create a containing block for position: fixed?
19. Difference between overflow-wrap, word-break, and white-space.
20. Difference between table-layout: auto and fixed.
21. How does Overflow Propagation work?

## Layout — Flexbox

1. How does the browser calculate flex-basis?
2. Explain how Flexbox calculates item sizes internally.
3. Why does a Flex item overflow even when flex: 1 is applied?
4. Why does min-width: auto cause Flexbox overflow?
5. A Flexbox layout is overflowing. How would you debug it?
6. Why is an image stretching inside a Flexbox container?
7. Why are Flexbox items not shrinking?
8. When should you choose Grid over Flexbox?
9. When should you combine Grid and Flexbox in the same layout?
10. How does the browser calculate available space in Flexbox?
11. What is the difference between flex-basis: auto and flex-basis: 0?
12. Why does flex: 1 sometimes produce unexpected layouts?
13. How do min-width and max-width interact with Flexbox?
14. How do nested Flexbox and Grid layouts affect performance?
15. How do you inspect Flexbox layouts in DevTools?
16. How would you redesign Flexbox if you could start from scratch?

## Layout — Grid

1. Explain the CSS Grid Auto-placement Algorithm.
2. What is the difference between auto-fit and auto-fill?
3. What is subgrid and when should it be used?
4. Why does a Grid item overflow its container?
5. A Grid layout works on desktop but breaks on mobile. How would you debug it?
6. How do browsers calculate fr units in CSS Grid?
7. What is the difference between Explicit Grid and Implicit Grid?
8. What is the purpose of grid-auto-flow?
9. How does grid-template-areas work internally?
10. How do you inspect CSS Grid layouts in DevTools?
11. How does Auto Layout work in CSS Grid?
12. How would you redesign CSS Grid?

## Responsive Design & Units

1. What is the difference between em, rem, %, vh, and vw?
2. What are Container Queries?
3. What is the difference between Media Queries and Container Queries?
4. What are CSS Logical Properties?
5. How would you build a responsive dashboard without using Media Queries?
6. Explain the aspect-ratio property.
7. What is the difference between object-fit, background-size, and aspect-ratio?
8. Can calc() combine different units like %, px, rem, and vw?
9. How do you implement responsive typography?
10. What is the difference between px, rem, em, and clamp() for font sizing?
11. Explain CSS Architecture (BEM, SMACSS, OOCSS, ITCSS, Atomic CSS).
12. How do you remove unused CSS in production?
13. What is the difference between 100vh, 100svh, 100lvh, and 100dvh?
14. What is the prefers-reduced-motion media query?
15. What is the prefers-color-scheme media query?
16. What is the difference between the Layout Viewport and the Visual Viewport?
17. What is the writing-mode property?
18. How do CSS Logical Properties work with RTL and vertical layouts?
19. What is the difference between physical properties (margin-left) and logical properties (margin-inline-start)?
20. How would you build a responsive layout without media queries?
21. How would you create a responsive table using only CSS?
22. How would you build a fully responsive navbar using only CSS?
23. How would you implement RTL support using CSS Logical Properties?
24. How do media queries affect CSS loading performance?
25. How does PurgeCSS (or Tailwind's content scanning) remove unused styles?
26. How do CSS logical properties improve accessibility?
27. How do you support RTL (Right-to-Left) layouts using CSS?
28. How would you build a responsive design system for multiple brands?
29. How would you build a theme engine supporting Light, Dark, RTL, and custom brand themes?
30. How would you build a fully responsive layout that supports LTR, RTL, vertical writing modes, dynamic themes, and accessibility without duplicating CSS?
31. What is fluid typography?
32. How does clamp() improve responsive design?
33. What are fluid spacing systems?
34. How does incremental rendering work?
35. How does Incremental Layout work?
36. How does Incremental Paint work?
37. If you had to remove one CSS feature forever, which one would it be and why?
38. What is the light-dark() CSS function? ✨ **New**
39. What are modern CSS color functions (hsl(), lab(), lch(), oklch(), oklab()) and why were they introduced? ✨ **New**
40. What is the color-mix() function? ✨ **New**

## Typography & Fonts

1. What is font-display: swap?
2. How do you create scalable spacing and typography systems?
3. How does line-height actually work?
4. How does font fallback work?
5. How do browsers choose fallback fonts?
6. How does browser font rendering work?
7. What is font hinting?
8. What is font subsetting?
9. What is text-wrap: balance and what problem does it solve? ✨ **New**
10. What does the hyphens property do? ✨ **New**
11. What is the difference between letter-spacing and word-spacing? ✨ **New**

## Animations & Transforms

1. Why is transform: translate() faster than top/left?
2. Which CSS animations are GPU accelerated?
3. Why is box-shadow more expensive than transform?
4. Why do we use transform: translate(-50%, -50%) for centering?
5. What is the View Transitions API?
6. How does CSS integrate with the View Transitions API?
7. Which CSS properties are most expensive to animate?
8. Why should you avoid animating width and height?
9. Why is animating transform and opacity recommended?
10. What is compositor-only animation?
11. A CSS animation causes the page to lag. How would you optimize it?
12. How do CSS keyframe animations work internally?
13. What is the difference between CSS Transitions and CSS Animations?
14. How does the browser interpolate animation values?
15. Which CSS properties can be animated and which cannot?
16. What is animation compositing?
17. What is the difference between animation-fill-mode values?
18. What is the difference between animation-play-state and animation-delay?
19. How do multiple animations run on the same element?
20. What is steps() in CSS animation?
21. What is the order of multiple transforms (translate, rotate, scale)?
22. What is the difference between 2D and 3D transforms?
23. How does perspective work?
24. What is transform-style: preserve-3d?
25. How does backface-visibility work?
26. What is the transform origin and how does it affect animations?
27. How does CSS calculate transformation matrices?
28. How do CSS animations work with SVG paths?
29. How do you debug CSS animations using DevTools?
30. How do you make CSS animations accessible?
31. How would you optimize the CSS rendering performance of a dashboard containing hundreds of cards, charts, tables, animations, and virtualized lists?
32. What is FLIP Animation?
33. How do browsers optimize animations?
34. How do registered custom properties improve animations?
35. What is Scroll-driven Animations (animation-timeline)?
36. How does requestAnimationFrame differ from CSS Animations?
37. How do CSS animations synchronize with the rendering pipeline?
38. How does animation throttling work in inactive tabs?
39. What are Scroll-linked Animations?
40. What is the difference between mask-image and clip-path for animating reveals? ✨ **New**

## CSS Variables, Theming & Design Systems

1. Explain CSS Variables in depth.
2. What is the difference between CSS Variables and SCSS Variables?
3. What are Design Tokens?
4. How do CSS Variables work in a Design System?
5. What are Custom Properties and how are they resolved by the browser?
6. How would you build a fully themeable design system using CSS Variables?
7. How do you structure CSS in a Design System?
8. How do you manage themes using CSS Variables?
9. How do you implement Light and Dark themes efficiently?
10. How would you build a CSS design token system from scratch?
11. How do CSS custom properties improve maintainability?
12. How would you implement multiple brand themes (white-label applications) using CSS?
13. How would you implement a multi-brand design system (e.g., Uber Eats, Uber, Uber Freight) using only CSS Variables and Design Tokens?
14. How would you implement instant theme switching (Light, Dark, Brand themes) without causing Flash of Unstyled Content (FOUC) or layout shifts?
15. What is @property and why is it useful?
16. How would you design a scalable Design Token architecture?
17. How would you implement versioning for Design Tokens?
18. Design a scalable Design System for 100+ products.
19. What is the accent-color property? ✨ **New**
20. What is the appearance property used for? ✨ **New**

## Architecture (BEM, CSS-in-JS, Modules, Tailwind, etc.)

1. What is the difference between Tailwind CSS and traditional CSS?
2. What are CSS Modules and how do they prevent style conflicts?
3. What is the difference between CSS Modules, Styled Components, Emotion, and Tailwind CSS?
4. What are the advantages and disadvantages of Utility-first CSS?
5. What are the advantages and disadvantages of CSS-in-JS?
6. How would you migrate a large CSS codebase to Tailwind CSS?
7. How would you design a scalable CSS architecture for a project with 1000+ components?
8. How does Tailwind CSS generate utility classes during build time?
9. What are the trade-offs between atomic CSS and semantic CSS?
10. How do you prevent CSS leakage in micro-frontend architectures?
11. What are the advantages and disadvantages of BEM?
12. What are the advantages and disadvantages of CSS Modules?
13. How would you build a CSS framework like Tailwind CSS?
14. How would you migrate a legacy CSS codebase (50,000+ lines) to a scalable architecture?
15. How would you architect CSS for a micro-frontend application?
16. How would you design a CSS architecture that supports 100+ developers working on the same codebase without style conflicts?
17. How would you build a component library that guarantees zero CSS conflicts across multiple micro-frontends loaded from different teams?
18. How would you build your own CSS Modules implementation?
19. How would you build a utility-first CSS framework like Tailwind?
20. How would you implement Atomic CSS from scratch?
21. Design a CSS architecture for a micro-frontend platform.

## Rendering Pipeline & Browser Internals

1. What is the Render Tree?
2. What is the CSSOM?
3. What causes Reflow?
4. What causes Repaint?
5. What causes Composite?
6. Explain the Browser Rendering Pipeline.
7. What is the difference between Reflow, Repaint, and Composite?
8. Which CSS properties trigger Layout, Paint, and Composite?
9. How is the Render Tree different from the DOM Tree?
10. Why are some DOM elements missing from the Render Tree?
11. What is Style Recalculation?
12. What is layer promotion in browsers?
13. How does the CSS parser work internally?
14. How is the CSSOM constructed by the browser?
15. How do browsers recover from CSS parsing errors?
16. How do you identify unnecessary repaints?
17. How do you identify unnecessary reflows?
18. How does the browser perform style recalculation, and what strategies would you use to minimize its cost in a large application?
19. Explain the complete lifecycle of a CSS property from parsing to rendering.
20. How would you implement your own CSS engine? Explain the architecture from parsing CSS to rendering pixels on the screen.
21. How does the browser invalidate styles after a DOM mutation?
22. What is style invalidation?
23. How does the CSS tokenizer work?
24. How does CSS parsing differ from HTML parsing?
25. How does the CSS Lexer work?
26. How does the CSS Parser build the CSSOM?
27. How do browsers optimize Style Recalculation?
28. How does Layer Promotion work?
29. What is Rasterization?
30. What is Tile-based Rendering?
31. How do browsers Composite GPU Layers?
32. Explain the entire browser rendering pipeline from HTML download to pixels appearing on the screen.
33. How would you implement Dark Mode across millions of pages without repainting?

## Performance & Optimization

1. How do you optimize CSS for a website with millions of users?
2. What is Critical CSS?
3. How does Critical CSS improve Core Web Vitals?
4. How do browsers cache CSS files?
5. What causes Cumulative Layout Shift (CLS)?
6. How can CSS help reduce CLS?
7. How does CSS affect Core Web Vitals?
8. How do you identify layout thrashing?
9. What are the best CSS practices for performance optimization?
10. How do you optimize CSS for a large enterprise application?
11. How do you optimize CSS bundle size?
12. How would you optimize CSS for SEO and performance?
13. How would you audit CSS performance in Lighthouse?
14. How does CSS loading affect First Contentful Paint (FCP)?
15. How does CSS loading affect Largest Contentful Paint (LCP)?
16. How do you preload critical CSS?
17. What is the difference between inline CSS and external CSS in terms of performance?
18. What is render-blocking CSS, and how do you eliminate it?
19. How do browser developer tools detect unused CSS?
20. How do you optimize SVG performance with CSS?
21. How do you profile CSS rendering performance?
22. How do you find unused CSS in Chrome DevTools?
23. How would you reduce CSS bundle size in a very large application?
24. Design a CSS architecture for an application with 1 million daily active users. What would you optimize first and why?
25. How would you identify whether a performance issue is caused by CSS, JavaScript, Layout, Paint, or the Compositor? Explain your debugging process.
26. How would you optimize CSS delivery to achieve a Lighthouse Performance score above 95 while maintaining maintainable styles?
27. Explain how browser compositing layers are created automatically. Which CSS properties trigger new compositor layers, and when can this hurt performance?
28. Why can will-change hurt performance?
29. What are Paint Holding optimizations?
30. How does CSS Memory Management work?
31. How do browsers optimize CSS matching?
32. How does HTTP/2 affect CSS delivery?
33. How does HTTP/3 affect CSS loading?
34. How would you optimize CSS for Server Components in Next.js?
35. How would you optimize CSS for a website with 100 million users?
36. If you were a browser engineer, how would you improve CSS performance?
37. What is contain-intrinsic-size and how does it pair with content-visibility? ✨ **New**

## Accessibility

1. How do you build accessible UI using CSS?
2. How do you ensure proper color contrast in CSS?
3. How do you visually hide an element while keeping it accessible to screen readers?
4. How would you build an accessible custom checkbox using CSS?
5. What is the difference between visual hiding and accessibility hiding?
6. How do you style focus states accessibly?
7. What is :focus-visible, and why is it preferred over :focus?
8. How do you design for high-contrast mode?
9. What are the most common CSS accessibility mistakes developers make?
10. How do you create an accessible modal using only CSS?
11. How do forced colors mode and Windows High Contrast affect CSS?
12. What is Forced Colors Mode?
13. How does High Contrast Mode affect CSS?
14. What is prefers-contrast?
15. How do you support keyboard-only navigation using CSS?
16. How do you create an accessible Tooltip using CSS?
17. What is the difference between aria-hidden and CSS visually-hidden techniques? ✨ **New**
18. How does pointer-events: none affect accessibility and interaction? ✨ **New**

## Modern CSS Features (Houdini, Anchor, Scroll-timeline, etc.)

1. What is CSS Houdini?
2. What is the CSS Typed Object Model (Typed OM)?
3. What are Paint Worklets in CSS Houdini?
4. What is the CSS Layout API?
5. What is CSS Anchor Positioning?
6. What is CSS Typed OM Level 2?
7. What is view-timeline?
8. What is scroll-timeline?
9. What are Style Queries?
10. What is :state()?
11. What is the @font-face rule and how does unicode-range optimize font loading? ✨ **New**
12. What is the initial-letter property? ✨ **New**

## SVG & CSS

1. How do SVG elements inherit CSS?
2. What is the difference between styling SVG with CSS and SVG attributes?
3. What is the difference between inline SVG and external SVG?
4. How does currentColor work inside SVG?
5. How do CSS filters affect SVG elements?
6. What is the difference between fill, stroke, and color in SVG?
7. What are the best practices for styling icons using SVG and CSS?

## Cross-browser & DevTools Debugging

1. How do you debug CSS layout issues using Chrome DevTools?
2. What is paint flashing in Chrome DevTools?
3. How would you debug a CSS issue using Chrome DevTools?
4. How would you debug a CSS issue that only occurs in Safari?
5. How does @supports work, and when should it be used?
6. What is Feature Detection in CSS?
7. Why does CSS behave differently in Chrome, Firefox, Safari, and Edge?
8. What are the most common Safari-specific CSS bugs?
9. How do you write cross-browser compatible CSS?
10. What is feature detection, and how is it different from browser detection?
11. How do @supports rules help with progressive enhancement?
12. How do you handle vendor prefixes today?
13. What tools automatically add vendor prefixes?
14. How do you debug layout issues using Chrome DevTools?
15. What is the Layers panel in Chrome DevTools?
16. How would you debug a production CSS issue that occurs only on iOS Safari and cannot be reproduced locally?

## Real-world Debugging Scenarios

1. Why doesn't height: 100% work in some cases?
2. Why doesn't left: 50%; top: 50% perfectly center an element?
3. Why doesn't border-radius clip child elements sometimes?
4. A tooltip is hidden behind another component. How would you debug it?
5. height: 100% is not working. Why?
6. How would you debug a rendering issue inside the browser engine?

## System Design / Staff-level / FAANG Scenarios

1. If you were creating a CSS framework from scratch, what features would you include and why?
2. If you had to redesign CSS today from scratch, what problems would you solve differently?
3. If you were interviewing a Senior Frontend Engineer for a FAANG company, what are the top 10 CSS topics you would test, and why?
4. Design a CSS engine from scratch.
5. How would you build the next generation of CSS?

---
**Total questions: 463** (removed 5 exact duplicates from the original list of 446; added 22 missing questions on commonly-asked topics not previously covered.)
