---
widget: contact
super_user: true
form:
  name: contact
  action: ""
  fields:
    name:
      label: "姓名"
      type: "name"
    email:
      label: "邮箱"
      type: "email"
    subject:
      label: "主题"
      type: "subject"
    message:
      label: "留言"
      type: "textarea"
  captcha: true
email: "contact@airesearch.lab"
contact_links:
  - icon: github
    icon_pack: fab
    name: "关注GitHub"
    link: "https://github.com/wuqifei2012"
  - icon: envelope
    icon_pack: fas
    name: "发送邮件"
    link: "mailto:contact@airesearch.lab"
automatic_link: true
design:
  columns: "1"
  style: "default"
  animation: ""
  significance: "0"
  spacer: ""
---
