
# Responsive Email Template

Fully responsive email template with varying sections of column layouts.

For additional information, original article can be found [here](https://webdesign.tutsplus.com/tutorials/creating-a-future-proof-responsive-email-without-media-queries--cms-23919).

## Inlining Your Code

When using this responsive template solution, you **must** inline all CSS when finished editing.

Be sure to use Campaign Monitor’s inliner tool, [inliner.cm](http://inliner.cm), which also inlines styles onto conditional tables.

First, delete the link tag `<link rel="stylesheet" type="text/css" href="styles.css" />` in the `<head>` of your document and replace it with `<style type="text/css">`. Copy the contents of style.css and paste it underneath, then close the style tag with `</style>`. Finally, copy and paste the entire file into the box at [inliner.cm](http://inliner.cm) and wait for the results. Once processed, copy the contents out of the box and you’re ready to go!

## Handy & Important Tips: 

 - For a quick and easy buffer on mobile, without having to fiddle
   around with padding or media queries, change the width of your table
   from 100% to 95%.
 - Images need to be sized to the maximum size which they should be, nothing larger. For example, don't use a high resolution image for a 300x300 image slot. Outlook won't resize properly.
