---
title: Tour
date: 2022-10-24

type: landing

sections:
  - block: slider
    content:
      slides:
      - title: 👋 Welcome
        content: Take a look at what we're working on...
        align: center
        background:
          image:
            filename: welcome.jpg
            filters:
              brightness: 0.35
          position: right
          color: '#666'
      - title: AI-Native EDA
        content: ' Opportunities and Challenges of Large Circuit Models'
        align: left
        background:
          image:
            filename: ai_native_eda.png
            filters:
              brightness: 0.35
          position: center
          color: '#555'
      - title: Time Series
        content: ' Prediction and Analysis of Events Ordered in Time'
        align: left
        background:
          image:
            filename: time_series.jpg
            filters:
              brightness: 0.35
          position: center
          color: '#555'
      - title: Generative AI
        content: ' Creating New and Original Content'
        align: left
        background:
          image:
            filename: generative_ai.jpg
            filters:
              brightness: 0.35
          position: center
          color: '#555'
      
    design:
      # Slide height is automatic unless you force a specific height (e.g. '400px')
      slide_height: ''
      is_fullscreen: true
      # Automatically transition through slides?
      loop: false
      # Duration of transition between slides (in ms)
      interval: 2000

  - block: markdown
    design:
      style: "min-height: 700px;"
      background:
        image:
          filename: ai_native_eda.png
          filters:
            brightness: 0.9
          # size: cover
          # position: center
          size: contain
          position: top
          parallax: true
          text_color_light: true
    content:
      # title: |
      #   <font size="9" style="color: rgba(255, 255, 255, 0.99);">
      #   CURE Lab Research Group
      #   </font>
      # image:
      #   filename: welcome.jpg
      text: |
        <div style="background-color: rgba(0, 0, 0, 0.65);">
        <p style="text-align: center">
        <font size=9px style="color: rgba(255, 255, 255, 1);">
        Large Circuit Model
        </font></p>
        <font size=4px style="color: rgba(255, 255, 255, 1);">
        We aim to explore opportunities and Challenges of Large Circuit Models in several espects:
        <br/>
        ✨ EDA Foundation Model
        <br/>
        ✨ AI-powered EDA Optimization
        <br/>
        ✨ Multi-modal EDA
        <br/>
        We are continue to work on ...
        </font> </div>
  
  - block: markdown
    design:
      style: "min-height: 700px;"
      background:
        image:
          filename: image_video.png
          filters:
            brightness: 0.9
          # size: cover
          # position: center
          size: contain
          position: top
          parallax: true
          text_color_light: true
    content:
      # title: |
      #   <font size="9" style="color: rgba(255, 255, 255, 0.99);">
      #   CURE Lab Research Group
      #   </font>
      # image:
      #   filename: welcome.jpg
      text: |
        <div style="background-color: rgba(0, 0, 0, 0.65);">
        <p style="text-align: center">
        <font size=9px style="color: rgba(255, 255, 255, 1);">
        Controllable Image&Video Generation
        </font></p>
        <font size=4px style="color: rgba(255, 255, 255, 1);">
        We aim to explore opportunities and Challenges of Controllable Image & Video Generation in several espects:
        <br/>
        ✨ Controllable Image Generation & Inpainting(Editing)
        <br/>
        ✨ High-quality Autonomous Driving Simulation
        <br/>
        ✨ Controllable Video Generation
        <br/>
        We are continue to work on ...
        </font> </div>

  - block: markdown
    design:
      style: "min-height: 700px;"
      background:
        image:
          filename: time_series.jpg
          filters:
            brightness: 0.9
          # size: cover
          # position: center
          size: contain
          position: top
          parallax: true
          text_color_light: true
    content:
      # title: |
      #   <font size="9" style="color: rgba(255, 255, 255, 0.99);">
      #   CURE Lab Research Group
      #   </font>
      # image:
      #   filename: welcome.jpg
      text: |
        <div style="background-color: rgba(0, 0, 0, 0.65);">
        <p style="text-align: center">
        <font size=9px style="color: rgba(255, 255, 255, 1);">
        Time Series Analysis
        </font></p>
        <font size=4px style="color: rgba(255, 255, 255, 1);">
        We aim to explore opportunities and Challenges of Time Series Analysis in several espects:
        <br/>
        ✨ Time Series Forecasting
        <br/>
        ✨ Time Series Anomaly Detection
        <br/>
        ✨ Time Series Representation Learning
        <br/>
        We are continue to work on ...
        </font> </div>
---
