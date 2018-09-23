---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth: texture1.png
widget1:
  title: "Outreach"
  url: 'http://kpolsen.github.io/outreach/'
  image: outreach_3884_2800.jpg
  text: 'Talks and presentations from different events.'
widget2:
  title: "Volunteer work"
  url: 'https://kpolsen.github.io/volun/'
  image: volun_3884_2800.jpg
  text: 'Projects I have worked/work on and the people I meet there.'
widget3:
  title: "Blog"
  url: 'https://kpolsen.github.io/more/blog/'
  image: blog_3884_2800.jpg
  text: 'Random adventures and discoveries.'
#
# Use the call for action to show a button on the frontpage
#
# To make internal links, just use a permalink like this
# url: /getting-started/
#
# To style the button in different colors, use no value
# to use the main color or success, alert or secondary.
# To change colors see sass/_01_settings_colors.scss
#
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true
---
