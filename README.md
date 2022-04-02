
# Responsive Email Template

Fully responsive email template (fluid-hybrid) with varying sections of column layouts.

For additional information, original article can be found [here](https://webdesign.tutsplus.com/tutorials/creating-a-future-proof-responsive-email-without-media-queries--cms-23919).

These columns can be tweaked to suit your needs. For example, if a you need a 2 column with a 60/40 split. Just adjust max-width on the column but also make sure to adjust the `conditional comments` for Outlook (there are table column widths hardcoded in the template set-up).

## Inlining Your Code

When using this responsive template solution, you **must** inline all CSS when finished editing.

Be sure to use an inliner tool which also inlines styles onto conditional tables.

- [MailChimp's Inliner](https://templates.mailchimp.com/resources/inline-css/)
- [Campaign Monitor's Inliner: inliner.cm](http://inliner.cm)

First, delete the link tag `<link rel="stylesheet" type="text/css" href="styles.css" />` and any other styles in the `<head>` of your document and replace it with `<style type="text/css">`. Copy the contents of style.css and paste it underneath, then close the style tag with `</style>`. Finally, copy and paste the entire file into the box at [inliner.cm](http://inliner.cm) and wait for the results. Once processed, copy the contents out of the box paste back into your file between the `<style>` tags.

## General Development Process

- Clone this repo and build out your template locally. Your initial HTML file should have some type of indicator that it is not the inlined version. I like to use `--index` at the end of the file name.
- Check that things are looking OK in the browser and all your HTML and CSS is clean. Make sure you have `align` tags on table columns where needed (mostly for centering).
- Once you have the base HTML file looking good and working, save it and then `save as` to create a new file. Remove the indicator from the filename (in this case, `--index`). This will be your "final" file moving forward.
- Follow the steps above to inline your code. You'll have to reference back to your original file for some pieces like the Dark Mode styles, some conditional comment/setup stuff. You'll also have to take any media queries you've defined in your `styles.css` file and add those into a `style` tag in the `head`.

## Handy & Important Tips: 

- Bulletproof Email Buttons:
https://buttons.cm/

- Bulletproof Background Images:
https://backgrounds.cm/

- Make sure all `table` elements use `role="presentation"`. This will remove any semantic meaning from the element and prevent screen readers from presenting the content as if it's tabular data.

 - Images should be double their display size so they display in high res (resize to actual size which fits email layout). Only set the `width` on images inline as this will help with regular display and the responsive styles. Always use helpful `alt` info! Use surrounding content to determine what `alt` into should be. If no `alt` declaration needs to be made, leave it empty! (`alt=""`).

- When checking and editing for responsive views, base your breakpoints on your content and not on devices sizes. Make sure your content looks good where/when you'd like.

- For a quick and easy buffer on mobile, without having to fiddle around with padding or media queries, change the width of your table from 100% to 75%, 50%, etc.

### Potential "Gotchas"

#### Outlook.com
- Outlook.com will strip `<a>` tags with empty or invaled `href` attributes.
  https://github.com/hteumeuleu/email-bugs/issues/10

- Outlook.com only prefixes first selector in a chain of selectors.
https://github.com/hteumeuleu/email-bugs/issues/61

#### Gmail
- Gmail removes styles that include special characters.
https://github.com/hteumeuleu/email-bugs/issues/19

- Gmail strips emails after 102KB. Will get  `[Message clipped] View entire message`.
https://github.com/hteumeuleu/email-bugs/issues/41

- Gmail removes `<style>` tags in non clipped view.

#### Yahoo
- Yahoo Android removes the first `head` tag (this is why we have duplicate `head` tags, with the first one empty).
https://github.com/hteumeuleu/email-bugs/issues/28

- Yahoo will ignore embedded styles preceded by a comment.
https://github.com/hteumeuleu/email-bugs/issues/25

### Some resources to minimize/condense code

- Email Comb
https://emailcomb.com/light

- HTML Crush
https://htmlcrush.com/light

- Alter.Email
https://alter.email/

### Smashing Magazine HTML Email Workshop Info

- Building Modern HTML emails
https://workshop.hteumeuleu.com/