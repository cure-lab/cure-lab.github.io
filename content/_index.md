---
# Leave the homepage title empty to use the site title
title:
date: 2024-05-25
type: landing

sections:
  - block: markdown
    design:
      background:
        image:
          filename: welcome.jpg
          filters:
            brightness: 0.9
          # size: cover
          # position: center
          size: contain
          position: top
          parallax: true
          text_color_light: true
    content:
      text: |
        <div style="background-color: rgba(0, 0, 0, 0.65);">
        <p style="text-align: center">
        <font size=9px style="color: rgba(255, 255, 255, 1);">
        CURE Lab Research Group
        </font></p>
        <font size=4px style="color: rgba(255, 255, 255, 1);">
        At the <u>CU</u>HK <u>RE</u>liable Computing laboratory (CURE Lab.), our core research methodology is rooted in creating innovative solutions that directly tackle the limitations of state-of-the-art computing technologies. Currently, we are passionately committed to the exploration and advancement of artificial intelligence across a variety of cutting-edge directions:
        <br/>
        ✨ AI-Native EDA
        <br/>
        ✨ Image&Video Generation 
        <br/>
        ✨ Time Series
        <br/>
        We are continue to work on the safety and security aspects of AI, developing robust AI models that can withstand adversarial attacks and operate reliably even under uncertain or volatile conditions.
        </font> </div>
  
  - block: collection
    content:
      title: Latest News
      subtitle:
      text:
      count: 5
      filters:
        author: ''
        category: ''
        exclude_featured: false
        publication_type: ''
        tag: ''
      offset: 0
      order: desc
      page_type: post
    design:
      view: card
      columns: '1'
  
  - block: collection
    content:
      title: Latest Preprints
      text: ""
      count: 5
      filters:
        folders:
          - publication
        publication_type: 'article'
    design:
      view: citation
      columns: '1'

  - block: people
    content:
      title: People
      user_groups:
          - Professor
          - Ph.D. Student
          - Research Assistant
          - Visitors
      sort_by: Params.year
      sort_ascending: false
    design:
      show_interests: false
      show_role: true
      show_social: true


---
