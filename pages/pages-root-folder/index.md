---
#
# Use the widgets beneath and the content will be
# inserted automagically in the webpage. To make
# this work, you have to use › layout: frontpage
#
layout: frontpage
header:
  image_fullwidth:
title: "CVLab @ USYD"

#slider:
#text_color: white
#shadow_color: black
#slides: 
#  - image: gallery-example-1.jpg
#    slide_html:
#  - image: gallery-example-2.jpg
#    slide_html: "<h2>Yes, this carousel supports html texting</h2>"
#  - image: gallery-example-3.jpg
#    slide_html: "<h2>Yes, this carousel supports html texting</h2>"

sidebar: right

widget1:
  title: "Pose Estimation"
  url: 'https://youtu.be/fSLmi166Mdk'
  video: '<iframe src="https://www.youtube.com/embed/fSLmi166Mdk" width="360" height="240" style="max-width: 100%; max-height: 150pt;"></iframe>'
  text: 'Check out our demo for multi-person <br/> pose estimation!'
widget2:
  title: "Video Detection"
  url: 'https://youtu.be/ZtbUcv_OIZg'
  text: 'We are also conducting reseaches about detecting objects in videos, check out our demo!'
  video: '<iframe src="https://www.youtube.com/embed/ZtbUcv_OIZg" width="360" height="240" style="max-width: 100%; max-height: 150pt;"></iframe>'
widget3:
  title: "Pose Tracking"
  url: 'https://youtu.be/CiKJuAH2U8I'
  video: '<iframe src="https://www.youtube.com/embed/AL-8XCzRFo0" width="360" height="240" style="max-width: 100%; max-height: 150pt;"></iframe>'
  text: 'Our team won the 2nd place in the pose-track challenge.'

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
#callforaction:
#  url: https://tinyletter.com/feeling-responsive
#  text: Inform me about new updates and features ›
#  style: alert
permalink: /index.html
#
# This is a nasty hack to make the navigation highlight
# this page as active in the topbar navigation
#
homepage: true

---


<div class="row main-content" style= " margin-top: 30px; max-height:540px">
  <div class="column small-9 pc">
    
    <!-- carrousel -->

    <div id="myCarousel" class="carousel slide" data-ride="carousel" style="">
        <!-- Indicators -->
        <ol class="carousel-indicators">
          <li data-target="#myCarousel" data-slide-to="0" class="active"></li>
          <li data-target="#myCarousel" data-slide-to="1"></li>
          <li data-target="#myCarousel" data-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner">
      		{% include carousel_item.html  active="true" url="https://wlouyang.github.io/projects/GBD/index.html" image="images/gbd-net.jpg" alt="GBD-Net for object detection" title="Object Detection" caption="We are conducting inspiring researches in general object detection. Our team won the 1st place of ILSVRC 2016. We are also working on the related topics including video detection and object tracking." %}

      		{% include carousel_item.html  url="http://cvboy.com/publication/cvpr2017_vip_cnn/" image="images/relation.jpg" alt="Visual Relationship Detection" title="Visual Relationship Detection" caption="Visual relationship detection involves detecting and localizing pairs of interacting objects in an image and also classifying the predicate or interaction between them. We are now working on this challenging problem. Click to see the detail!" %}

#      		{% include carousel_item.html  url="http://mmlab.ie.cuhk.edu.hk/projects/project_salience_reid/index.html" image="images/re-id.png" alt="Re-Identification" title="Person Re-Identification (ReID)" caption="Given one query image of one specific person, a person ReID system is expected to provide all the images of the same person from a large gallery database. We have been focusing on person re-id problem over years." %}
        </div>

        <!-- Left and right controls -->
        <a class="left carousel-control" href="#myCarousel" data-slide="prev">
          <span class="glyphicon glyphicon-chevron-left"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="right carousel-control" href="#myCarousel" data-slide="next">
          <span class="glyphicon glyphicon-chevron-right"></span>
          <span class="sr-only">Next</span>
        </a>
    </div>
  </div>



  <!-- carrousel on mobile devices -->
  <div class="column small-12 mobile">
    
    <!-- carousel -->
    <div id="myCarousel-mobile" class="carousel slide" data-ride="carousel" style="">
        <!-- Indicators -->
        <ol class="carousel-indicators">
          <li data-target="#myCarousel-mobile" data-slide-to="0" class="active"></li>
          <li data-target="#myCarousel-mobile" data-slide-to="1"></li>
          <li data-target="#myCarousel-mobile" data-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner">
          {% include carousel_item.html  active="true" 
             url="https://wlouyang.github.io/projects/GBD/index.html" 
             image="images/gbd-net.jpg" 
             alt="GBD-Net for object detection" 
             title="Object Detection" 
             caption="We are conducting inspiring researches in general object detection. Our team won the 1st place of ILSVRC 2016. We are also working on the related topics including video detection and object tracking." %}

          {% include carousel_item.html  
             url="http://cvboy.com/publication/cvpr2017_vip_cnn/" 
             image="images/relation.jpg" 
             alt="Visual Relationship Detection" 
             title="Visual Relationship Detection" 
             caption="Visual relationship detection involves detecting and localizing pairs of interacting objects in an image and also classifying the predicate or interaction between them. We are now working on this challenging problem. Click to see the detail!" %}

          {% include carousel_item.html  
             url="http://cvboy.com/publication/cvpr2017_vip_cnn/" 
             image="images/re-id.png" alt="Re-Identification" 
             title="Person Re-Identification (ReID)" 
             caption="Given one query image of one specific person, a person ReID system is expected to provide all the images of the same person from a large gallery database. We have been focusing on person re-id problem over years." %}
        </div>

        <!-- Left and right controls -->
        <a class="left carousel-control" href="#myCarousel-mobile" data-slide="prev">
          <span class="glyphicon glyphicon-chevron-left"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="right carousel-control" href="#myCarousel-mobile" data-slide="next">
          <span class="glyphicon glyphicon-chevron-right"></span>
          <span class="sr-only">Next</span>
        </a>
    </div>
  </div>




  <div class="column small-3 pc" style="max-height: inherit">
  	<div><h3>News</h3></div>
    
    <div class="list-group" style="margin-left=0; max-height: inherit; overflow-y: auto;">
    {% include news_item.html 
        highlight="true" date="Always"
        content="We are hiring! Several Ph.D. positions are now available at USYD in computer vision. Candidates with strong academic background and/or solid programming skill are highly preferred." %}
    {% include news_item.html  date="20-Dec-2019" content="Congratulations to Weichen Zhang 's paper accepted by TPAMI" %}        
    
    {% include news_item.html  date="20-Nov-2019" content="Congratulations to Jinyang Guo 's paper accepted by AAAI 2020" %}

    {% include news_item.html  date="22-July-2019" content="Congratulations to Lingbo Liu 's paper accepted by ICCV 2019" %}

    {% include news_item.html  date="10-May-2019" content="Congratulations to Guo Lu 's paper accepted by CVPR 2019" %}

    {% include news_item.html  date="10-May-2019" content="Congratulations to Rui Su's paper accepted by CVPR 2019" %}

    {% include news_item.html  date="10-May-2019" content="Our lab homepage is now onine!" %}


    </div>
  </div>
</div>

<div class="column small-12 mobile">
    <br>
    <h3>News</h3>
    <div class="list-group" style="margin-left=0">
      {% include news_item.html 
        highlight="true" date="Always"
        content="We are hiring! Several Ph.D. positions are now available at USYD in computer vision. Candidates with strong academic background and/or solid programming skill are highly preferred." %}

    {% include news_item.html  date="10-May-2019" content="Congratulations to Rui Su's paper accepted by CVPR 2019" %}

      {% include news_item.html  date="10-May-2019" content="Our lab homepage is now onine!" %}

    </div>
    <h3 class="mobile"> Our Research </h3>
</div>


<div class="pc">
<br>
<h3> Our Research </h3> 
</div>

---
