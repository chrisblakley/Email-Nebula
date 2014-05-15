#Email-Nebula

Starting point options for responsive HTML email campaigns.

##Documentation

In the fluid version, all rows should become tables themselves. This will segment any bugs to their own table (and speed up troubleshooting by isolating the bug).

When using a text link (or any date written out such as "June 30" or "6/30"), add the class "mobile_link" to its parent. If it's a date, you could just wrap it in a span with that class. This prevents iOS from hijacking the style of the link.

###Outlook Conditional Comments

For 3-column layouts in the stepped version, you'll need to use conditional comments to make it work in Outlook 2007, 2010, and 2013. To do so, use the condition of "gte mso 9". It will look something like this:
```html
<!--[if gte mso 9]>
  <table width="7" align="left" border="0" cellpadding="0" cellspacing="0" class="removeMobile">
<![endif]-->
                                                
<!--[if !mso]><!-- -->
  <table width="25" align="left" border="0" cellpadding="0" cellspacing="0" class="removeMobile">
<!--<![endif]-->
```
Depending on the width of the design, the above table widths will need to be adjusted (the above works for a 600px wide email with columns of 170px).
