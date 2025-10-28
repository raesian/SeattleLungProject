---
layout: page
title: "Media"
description: "Videos and Images"
header-img: "img/home-bg.jpg"
nav_order: 2
---

<!-- Video Section -->
<div class="video-section">
  <h3>9/11 Transplant Surgery</h3>
  <p>Following the September 11th attacks, air space all across the country was shut down. So how did a flight carrying organs for critical surgeries reach its destination that day? With the help of the Armed Forces.</p>
  
  <div class="video-container">
    <video controls width="600" height="auto" preload="metadata">
      <source src="/img/Mulligan911Story.mp4" type="video/mp4">
      <source src="{{ site.baseurl }}/img/Mulligan911Story.mp4" type="video/mp4">
      <p>Video file not found. Please check the file path: {{ site.baseurl }}/img/Mulligan911Story.mp4</p>
      Your browser does not support the video tag.
    </video>
  </div>
  
  <div class="video-info">
    <p><strong>Source:</strong> CBS Sports Network (@CBSSportsNet)</p>
    <p><strong>Date:</strong> September 11, 2021</p>
  </div>
</div>

<style>
.video-section {
  max-width: 800px;
  margin: 0 auto;
  padding: 20px;
  text-align: center;
}

.video-section h3 {
  color: #333;
  margin-bottom: 15px;
  font-size: 1.5em;
}

.video-section p {
  color: #666;
  margin-bottom: 30px;
  font-size: 1.1em;
  line-height: 1.6;
}

.video-container {
  margin: 20px 0;
  text-align: center;
  max-width: 600px;
  margin-left: auto;
  margin-right: auto;
}

.video-container video {
  width: 100%;
  max-width: 600px;
  height: auto;
  border-radius: 10px;
  box-shadow: 0 10px 30px rgba(0,0,0,0.2);
  background: #000;
}

.video-info {
  margin-top: 30px;
  padding: 20px;
  background: #f8f9fa;
  border-radius: 10px;
  text-align: center;
}

.video-info p {
  margin: 5px 0;
  color: #666;
  font-size: 0.9em;
}
</style>
