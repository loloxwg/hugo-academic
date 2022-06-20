---
# An instance of the Contact widget.
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle:

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: loloxwg@gmail.com
#  phone: +86 159 xxxx xxxx
#  address:
#    city: Shanghai
#    country: China
#    country_code: CN
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: Twitter
      link: https://twitter.com/loloxwg
    - icon: reddit
      icon_pack: fas
      name: Reddit
      link: https://www.reddit.com/
    - icon: github
      icon_pack: fab
      name: Github
      link: https://github.com/loloxwg

design:
  columns: '2'
---
