---
# An instantiation of the contact widget
widget: contact
# Automatically link email and github?
super_user: true
# Display a contact form?
form:
  name: contact
  # Form action (HTTP endpoint) — leave empty for a default Netlify form
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
# Email address (if using super_user=false)
email: "contact@airesearch.lab"
# Contact details displayed below the form (leave blank to hide)
contact_links:
  - icon: github
    icon_pack: fab
    name: "Follow Us on GitHub"
    link: "https://github.com/wuqifei2012"
  - icon: envelope
    icon_pack: fas
    name: "Email Us"
    link: "mailto:contact@airesearch.lab"
  - icon: linkedin
    icon_pack: fab
    name: "LinkedIn"
    link: "https://linkedin.com/company/ai-research-lab"
# Automatic links populated from social icons
automatic_link: true
design:
  # Column count (1/2/3)
  columns: "1"
  # Style theme option ('dark', 'light', or 'default')
  style: "default"
  # Animation
  animation: ""
  # Significance/weight of the experience (1-5)
  significance: "0"
  # Spacer between experiences (empty, small, medium, large)
  spacer: ""
---
