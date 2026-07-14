---
# An instantiation of the contact widget
widget: contact
# Automatically link email and github?
super_user: true
# Display a contact form?
form:
  name: contact
  # Form action — leave empty for default
  action: ""
  # Fields
  fields:
    name:
      label: "Name"
      type: "name"
    email:
      label: "Email"
      type: "email"
    subject:
      label: "Subject"
      type: "subject"
    message:
      label: "Message"
      type: "textarea"
  # Whether to show a captcha
  captcha: true
# Email address
email: "contact@airelearnpro.dev"
# Contact details displayed below the form
contact_links:
  - icon: github
    icon_pack: fab
    name: "⭐ Star Us on GitHub"
    link: "https://github.com/wuqifei2012"
  - icon: envelope
    icon_pack: fas
    name: "Email Us"
    link: "mailto:contact@airelearnpro.dev"
  - icon: linkedin
    icon_pack: fab
    name: "Connect on LinkedIn"
    link: "https://linkedin.com/in/wuqifei"
  - icon: scholar
    icon_pack: fas
    name: "Google Scholar"
    link: "https://scholar.google.com"
# Automatic links populated from social icons
automatic_link: true
design:
  # Column count (1/2/3)
  columns: "1"
  # Style theme option ('dark', 'light', or 'default')
  style: "light"
  # Animation
  animation: fade-in
---
