---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: hero
    content:
      title: |
        CURELab
      image:
        filename: welcome.jpg
      text: |
        <p style="line-height:1em">
          <font size="4"> 
            At the <u>CU</u>HK <u>RE</u>liable Computing laboratory (CURE Lab.), our core research methodology is rooted in creating innovative solutions that directly tackle the limitations of state-of-the-art computing technologies. Currently, we are passionately committed to the exploration and advancement of artificial intelligence across a variety of cutting-edge directions:
            <br/>
            ✨ AI-Native EDA
            ✨ Time Series
            ✨ Generative AI
            <br/>
            We are continue to work on the safety and security aspects of AI, developing robust AI models that can withstand adversarial attacks and operate reliably even under uncertain or volatile conditions.
            <br />
          </font> 
        </p>
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