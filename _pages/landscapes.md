---
title: "Landscape Photography"
layout: splash
permalink: /portfolio/landscapes/
header:
  overlay_image: /assets/images/landscapes-header.jpg
  overlay_filter: 0.3
  caption: "Photo credit: Baykal Media"
excerpt: "Capturing the breathtaking beauty of our natural world"

gallery_ezine:
  - url: /assets/images/landscapes/ezine/ezine-1.jpg
    image_path: /assets/images/landscapes/ezine/ezine-1.jpg
    title: "Hills overlooking Bozcaada"
  - url: /assets/images/landscapes/ezine/ezine-2.jpg
    image_path: /assets/images/landscapes/ezine/ezine-2.jpg
    title: "Ancient Granite Quarry"
  - url: /assets/images/landscapes/ezine/ezine-3.jpg
    image_path: /assets/images/landscapes/ezine/ezine-3.jpg
    title: "Rolling Hills of Ezine"
  - url: /assets/images/landscapes/ezine/ezine-4.jpg
    image_path: /assets/images/landscapes/ezine/ezine-4.jpg
    title: "Villages of Sakar Peak"
  - url: /assets/images/landscapes/ezine/ezine-5.jpg
    image_path: /assets/images/landscapes/ezine/ezine-5.jpg
    title: "Cigri Village Entrance"
  - url: /assets/images/landscapes/ezine/ezine-6.jpg
    image_path: /assets/images/landscapes/ezine/ezine-6.jpg
    title: "Cigri"

gallery_eastern:
  - url: /assets/images/landscapes/eastern-turkey/eastern-1.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-1.jpg
    title: "Ducks of Lake Van"
  - url: /assets/images/landscapes/eastern-turkey/eastern-2.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-2.jpg
    title: "Lake Van"
  - url: /assets/images/landscapes/eastern-turkey/eastern-4.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-4.jpg
    title: "Mount Artos"
  - url: /assets/images/landscapes/eastern-turkey/eastern-5.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-5.jpg
    title: "Hosap Village"
  - url: /assets/images/landscapes/eastern-turkey/eastern-7.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-7.jpg
    title: "Mount Ararat"
  - url: /assets/images/landscapes/eastern-turkey/eastern-8.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-8.jpg
    title: "Horse Ride in Cildir"
  - url: /assets/images/landscapes/eastern-turkey/eastern-9.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-9.jpg
    title: "Erzurum-Erzincan Train"
  - url: /assets/images/landscapes/eastern-turkey/eastern-6.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-6.jpg
    title: "Ancient Church in Ani"
  - url: /assets/images/landscapes/eastern-turkey/eastern-10.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-10.jpg
    title: "Ani Village"
  - url: /assets/images/landscapes/eastern-turkey/eastern-3.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-3.jpg
    title: "Lake Cildir"
  - url: /assets/images/landscapes/eastern-turkey/eastern-11.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-11.jpg
    title: "Erzurum"
  - url: /assets/images/landscapes/eastern-turkey/eastern-12.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-12.jpg
    title: "Hosap Castle"
  - url: /assets/images/landscapes/eastern-turkey/eastern-13.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-13.jpg
    title: "Horses of Cildir"
  - url: /assets/images/landscapes/eastern-turkey/eastern-14.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-14.jpg
    title: "Kars Bakkal"
  - url: /assets/images/landscapes/eastern-turkey/eastern-15.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-15.jpg
    title: "Woman in Erzurum"
  - url: /assets/images/landscapes/eastern-turkey/eastern-16.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-16.jpg
    title: "Caves of Ani"
  
---

## Landscape Photography

My landscape photography focuses on capturing the raw beauty and emotional impact of natural environments. From dramatic mountain ranges to serene coastal scenes, I seek to create images that transport viewers and evoke a sense of wonder about our natural world.

---

## Collections

Explore the galleries below.

{% capture ezine_content %}
Landscapes from Ezine, capturing the Aegean light and rural scenery.

<div class="masonry-gallery gallery_ezine">
  {% for img in page.gallery_ezine %}
    <div class="masonry-item">
      <a href="{{ img.url | relative_url }}" class="image-popup">
        <img src="{{ img.image_path | relative_url }}" alt="{{ img.title }}" title="{{ img.title }}">
      </a>
      <span class="caption">{{ img.title }}</span>
    </div>
  {% endfor %}
</div>
{% endcapture %}

{% capture eastern_content %}
Dramatic scenery and historic textures from Eastern Turkey.

<div class="masonry-gallery gallery_eastern">
  {% for img in page.gallery_eastern %}
    <div class="masonry-item">
      <a href="{{ img.url | relative_url }}" class="image-popup">
        <img src="{{ img.image_path | relative_url }}" alt="{{ img.title }}" title="{{ img.title }}">
      </a>
      <span class="caption">{{ img.title }}</span>
    </div>
  {% endfor %}
</div>
{% endcapture %}

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Ezine - January 2025</h3>
  <div class="accordion-content" markdown="1">
    {{ ezine_content | markdownify }}
  </div>
</div>

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Eastern Turkey - December 2024</h3>
  <div class="accordion-content" markdown="1">
    {{ eastern_content | markdownify }}
  </div>
</div>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script src="https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js"></script>
<script src="https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js"></script>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    // Initialize accordions
    const accordions = document.querySelectorAll('.accordion-header');

    accordions.forEach(accordion => {
      accordion.addEventListener('click', function() {
        this.classList.toggle('active');
        const content = this.nextElementSibling;

        if (content.style.maxHeight) {
          content.style.maxHeight = null;
        } else {
          content.style.maxHeight = content.scrollHeight + "px";
        }

        setTimeout(function() {
          if (accordion.classList.contains('active')) {
            content.classList.add('active');
            
            // Initialize Masonry after accordion is opened and images are loaded
            const gallery = content.querySelector('.masonry-gallery');
            if (gallery) {
              // Force three columns
              const containerWidth = gallery.offsetWidth;
              const itemWidth = (containerWidth / 3) - 20; // 3 columns with spacing
              
              const items = gallery.querySelectorAll('.masonry-item');
              items.forEach(item => {
                item.style.width = itemWidth + 'px';
              });
              
              imagesLoaded(gallery, function() {
                new Masonry(gallery, {
                  itemSelector: '.masonry-item',
                  gutter: 10,
                  fitWidth: true
                });
              });
            }
          } else {
            content.classList.remove('active');
          }
        }, 100);
      });
    });
  });
</script>

<style>
  .accordion {
    margin-bottom: 1rem;
    border-radius: 4px;
    overflow: hidden;
  }

  .accordion-header {
    cursor: pointer;
    padding: 0.75rem 1rem;
    margin: 0;
    font-size: 1.2em;
    font-weight: bold;
    transition: 0.3s;
  }

  .accordion-header:hover {
    background-color: rgba(0, 0, 0, 0.05);
  }

  .accordion-header:after {
    content: '\002B'; /* Plus sign */
    font-weight: bold;
    float: right;
    margin-left: 5px;
  }

  .accordion-header.active:after {
    content: "\2212"; /* Minus sign */
  }

  .accordion-content {
    padding: 0 1rem;
    max-height: 0;
    overflow: hidden;
    transition: max-height 0.3s ease-out;
  }

  .accordion-content.active {
    max-height: 8000px !important; /* Increased for taller masonry content */
  }

  /* Masonry Gallery Layout */
  .masonry-gallery {
    width: 100%;
    margin: 0 auto;
  }

  .masonry-item {
    box-sizing: border-box;
    margin-bottom: 10px;
    padding: 0 5px;
    /* Width will be set by JavaScript */
  }

  .masonry-item a {
    display: block;
    overflow: hidden;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .masonry-item a {
    display: block;
    overflow: hidden;
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
  }

  .masonry-item img {
    width: 100%;
    height: auto;
    display: block;
    transition: transform 0.3s ease;
  }

  .masonry-item img:hover {
    transform: scale(1.03);
  }

  .masonry-item .caption {
    display: block;
    padding: 3px 0;
    font-size: 0.75rem; /* Smaller font size */
    text-align: center;
    color: #666;
    line-height: 1.2; /* Tighter line height */
  }
</style>

---

For pricing information on prints or to discuss commissioned landscape work, please visit my [pricing page](/pricing/) or [contact me](/contact/) directly.