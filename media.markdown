---
layout: page
title: "Media"
description: "Videos and Images"
header-img: "img/home-bg.jpg"
nav_order: 2
---

<!-- Page Header -->
<div class="media-page-header">
  <h2>Lab Media Gallery</h2>
</div>

<!-- Spotlight Story Title -->
<h2 class="section-title">Spotlight Story</h2>

<!-- Featured Video Section -->
<div class="featured-section">
  <div class="featured-video-card">
    <div class="featured-video-wrapper">
      <video controls preload="metadata" poster="{{ site.baseurl }}/img/SpotlightThumbnail.jpg">
        <source src="/img/Mulligan911Story.mp4" type="video/mp4">
        <source src="{{ site.baseurl }}/img/Mulligan911Story.mp4" type="video/mp4">
        Your browser does not support the video tag.
      </video>
    </div>
    <div class="featured-video-content">
      <h3>9/11 Transplant Surgery</h3>
      <p>Following the September 11th attacks, air space all across the country was shut down. So how did a flight carrying organs for critical surgeries reach its destination that day? With the help of the Armed Forces.</p>
      <div class="video-meta">
        <span class="meta-item"><strong>Source:</strong> CBS Sports Network</span>
        <span class="meta-item"><strong>Date:</strong> September 11, 2021</span>
      </div>
    </div>
  </div>
</div>

<!-- Day in the Life Title -->
<h2 class="section-title">Day in the Life Series</h2>

<!-- Day in the Life Section -->
<div class="video-section-container">
  <div class="video-grid">
    
    <!-- Day in the Life: Hesham -->
    <div class="video-card">
      <div class="video-wrapper">
        <iframe width="100%" height="100%" src="https://www.youtube.com/embed/j_sQ130GSbo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="video-content">
        <h3>Day in the Life: Hesham</h3>
        <p>Follow Hesham for 48 hours on summer break through adventures and lab.</p>
        <div class="video-meta">
          <span class="meta-item"><strong>Series:</strong> Day in the Life</span>
        </div>
      </div>
    </div>

    <!-- Day in the Life: Jonny -->
    <div class="video-card">
      <div class="video-wrapper">
        <video controls preload="metadata" poster="{{ site.baseurl }}/img/MichaelMulliganLoadingScreen.jpg">
          <source src="{{ site.baseurl }}/img/DayInTheLife.v2_Jonny.mov" type="video/mp4">
          <source src="{{ site.baseurl }}/img/DayInTheLife.v2_Jonny.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>
      <div class="video-content">
        <h3>Day in the Life: Jonny</h3>
        <p>Experience a day in the life with Jonny, a neuroscience undergraduate student balancing school and lab. Walk through blood processing with him!</p>
        <div class="video-meta">
          <span class="meta-item"><strong>Series:</strong> Day in the Life</span>
        </div>
      </div>
    </div>

  </div>
</div>

<style>
/* Page Header */
.media-page-header {
  text-align: center;
  max-width: 800px;
  margin: 0 auto 20px auto;
  padding: 20px;
}

.media-page-header h2 {
  font-size: 2.5rem;
  color: var(--color-primary, #2c3e50);
  margin-bottom: 15px;
  font-weight: 700;
}

.media-page-header p {
  font-size: 1.2rem;
  color: var(--color-text-muted, #666);
  line-height: 1.6;
}

/* Section Titles */
.section-title {
  font-size: 2rem;
  color: #2c3e50 !important;
  text-align: center;
  margin-bottom: 40px;
  margin-top: 20px;
  font-weight: 700;
  position: relative;
  padding-bottom: 15px;
  display: block;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 4px;
  background: #3498db;
  border-radius: 2px;
}

/* Featured Section */
.featured-section {
  max-width: 1200px;
  margin: 0 auto 80px auto;
  padding: 20px;
}

.featured-video-card {
  background: white;
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 8px 30px rgba(0, 0, 0, 0.12);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.featured-video-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 16px 50px rgba(0, 0, 0, 0.18);
}

.featured-video-wrapper {
  position: relative;
  width: 100%;
  background: #000;
  aspect-ratio: 16 / 9;
}

.featured-video-wrapper video {
  width: 100%;
  height: 100%;
  object-fit: cover;
  display: block;
}

.featured-video-content {
  padding: 40px;
}

.featured-video-content h3 {
  font-size: 2rem;
  color: var(--color-text, #333);
  margin: 0 0 20px 0;
  font-weight: 700;
  line-height: 1.3;
}

.featured-video-content p {
  color: var(--color-text-muted, #666);
  font-size: 1.1rem;
  line-height: 1.8;
  margin-bottom: 30px;
}

/* Video Section Container */
.video-section-container {
  max-width: 1400px;
  margin: 0 auto 60px auto;
  padding: 20px;
}

/* Video Grid */
.video-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
  gap: 40px;
}

/* Video Card */
.video-card {
  background: white;
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.08);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  flex-direction: column;
}

.video-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 40px rgba(0, 0, 0, 0.15);
}

/* Video Wrapper */
.video-wrapper {
  position: relative;
  width: 100%;
  background: #000;
  aspect-ratio: 16 / 9;
  max-width: 600px;
  margin: 0 auto;
}

.video-wrapper video,
.video-wrapper iframe {
  width: 100%;
  height: 100%;
  object-fit: contain;
  display: block;
  border: none;
}

/* Video Content */
.video-content {
  padding: 24px;
  flex: 1;
  display: flex;
  flex-direction: column;
}

.video-content h3 {
  font-size: 1.5rem;
  color: var(--color-text, #333);
  margin: 0 0 12px 0;
  font-weight: 600;
  line-height: 1.3;
}

.video-content p {
  color: var(--color-text-muted, #666);
  font-size: 1rem;
  line-height: 1.6;
  margin-bottom: 20px;
  flex: 1;
}

/* Video Meta */
.video-meta {
  display: flex;
  flex-direction: column;
  gap: 8px;
  padding-top: 16px;
  border-top: 1px solid #e0e0e0;
}

.meta-item {
  font-size: 0.9rem;
  color: var(--color-text-muted, #666);
}

.meta-item strong {
  color: var(--color-text, #333);
  font-weight: 600;
}

/* Responsive Design */
@media (max-width: 768px) {
  .video-grid {
    grid-template-columns: 1fr;
    gap: 30px;
  }

  .media-page-header h2 {
    font-size: 2rem;
  }

  .media-page-header p {
    font-size: 1.1rem;
  }

  .section-title {
    font-size: 1.75rem;
  }

  .featured-video-content {
    padding: 24px;
  }

  .featured-video-content h3 {
    font-size: 1.6rem;
  }

  .video-content {
    padding: 20px;
  }

  .video-content h3 {
    font-size: 1.3rem;
  }
}

@media (min-width: 769px) and (max-width: 1200px) {
  .video-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1201px) {
  .video-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* Loading State */
video:not([src]) {
  background: linear-gradient(90deg, #f0f0f0 25%, #e0e0e0 50%, #f0f0f0 75%);
  background-size: 200% 100%;
  animation: loading 1.5s infinite;
}

@keyframes loading {
  0% { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}
</style>
