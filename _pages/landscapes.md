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

---

### Ezine - January 2025
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

---

### Eastern Turkey - December 2024
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

<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
<script src="https://unpkg.com/imagesloaded@5/imagesloaded.pkgd.min.js"></script>
<script src="https://unpkg.com/masonry-layout@4/dist/masonry.pkgd.min.js"></script>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const galleries = document.querySelectorAll('.masonry-gallery');

    galleries.forEach(gallery => {
      // Force three columns
      const containerWidth = gallery.offsetWidth;
      // Ensure there's a fallback if offsetWidth is 0 (e.g., if gallery is hidden initially by other means)
      const itemWidth = containerWidth > 0 ? (containerWidth / 3) - 20 : (window.innerWidth / 3) - 20; // 3 columns with spacing
      
      const items = gallery.querySelectorAll('.masonry-item');
      items.forEach(item => {
        item.style.width = itemWidth + 'px';
      });
      
      imagesLoaded(gallery, function() {
        new Masonry(gallery, {
          itemSelector: '.masonry-item',
          gutter: 10,
          fitWidth: true // fitWidth might conflict with fixed column width, adjust as needed
                         // If you strictly want 3 columns, you might remove fitWidth and ensure container width is appropriate
                         // or calculate columnWidth based on a parent container.
        });
      });
    });
  });
</script>

<style>
  /* Masonry Gallery Layout */
  .masonry-gallery {
    width: 100%; /* Make sure it takes full width available */
    margin: 20px auto; /* Add some margin around galleries */
    /* If using fitWidth: true for Masonry, it will center itself if smaller than container.
       If not using fitWidth and setting columnWidth, ensure the total width of items + gutters
       fits within the gallery container or it might break layout.
    */
  }

  .masonry-item {
    box-sizing: border-box;
    margin-bottom: 10px;
    padding: 0 5px; /* Horizontal padding to create space between items, gutter handles vertical */
    /* Width will be set by JavaScript */
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

  /* Optional: Add some styling for the gallery titles if desired */
  h3 {
    margin-top: 2em;
    margin-bottom: 0.5em;
    padding-bottom: 0.3em;
    border-bottom: 1px solid #eee;
  }
</style>

---

For pricing information on prints or to discuss commissioned landscape work, please visit my [pricing page](/pricing/) or [contact me](/contact/) directly.