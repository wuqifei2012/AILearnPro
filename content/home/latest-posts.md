---
# An instantiation of the collection widget for blog posts
widget: collection
# Title
title: "Latest Posts"
# Description (show below title)
subtitle: ""
# Page type (post, publication, project, slide, or custom type)
page_type: post
# Number of items to list in this view (0 = show all)
count: 3
# Filter rows
filter_metadata:
  tags: ""
# Sort items (e.g., most recent, date descending)
sort_by: "date"
sort_desc: true
design:
  # Choose how many columns the grid uses, how wide the gap between columns is,
  # and the card hover style ('dark', 'light', or 'default')
  view: article-grid
  # Show the "Display an overlay with content on hover?" option?
  count: 3
  # Display a read preview, a thumbnail, or nothing for each widget_item?
  content:
    # Read more link ('excerpt', 'full', or '' to hide)
    read_more: excerpt
    # Available page types: < > date (Published date) | abstract (Abstract text) | links (Custom links) | signature (Author signature) | badge (Publication type badge)
    preview: ""
  # Show pagination?
  pagination:
    - ""
  # Hover over display types (brief, detail, or link)
  hover: brief
  # Show user-defined tags?
  tags_hide: ""
  # Size (xs, sm, md, lg)
  size: md
  # Animation effect (fade, zoom)
  animation: ""
  # Padding
  padding:
    - ""
---
