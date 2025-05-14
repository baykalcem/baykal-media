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
  - url: /assets/images/landscapes/eastern-turkey/eastern-3.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-3.jpg
    title: "Lake Cildir"
  - url: /assets/images/landscapes/eastern-turkey/eastern-4.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-4.jpg
    title: "Mount Artos"
  - url: /assets/images/landscapes/eastern-turkey/eastern-5.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-5.jpg
    title: "Hosap Village"
  - url: /assets/images/landscapes/eastern-turkey/eastern-6.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-6.jpg
    title: "Ancient Church in Ani"
  - url: /assets/images/landscapes/eastern-turkey/eastern-7.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-7.jpg
    title: "Lake Van"
  - url: /assets/images/landscapes/eastern-turkey/eastern-8.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-8.jpg
    title: "Lake Cildir"
  - url: /assets/images/landscapes/eastern-turkey/eastern-9.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-9.jpg
    title: "Mount Artos"
  - url: /assets/images/landscapes/eastern-turkey/eastern-10.jpg
    image_path: /assets/images/landscapes/eastern-turkey/eastern-10.jpg
    title: "Hosap Village"
---

## Landscape Photography

My landscape photography focuses on capturing the raw beauty and emotional impact of natural environments. From dramatic mountain ranges to serene coastal scenes, I seek to create images that transport viewers and evoke a sense of wonder about our natural world.

---

## Collections

Explore the galleries below.

{% capture ezine_content %}
Landscapes from Ezine, capturing the Aegean light and rural scenery.

{% include gallery id="gallery_ezine" %}
{% endcapture %}

{% capture eastern_content %}
Dramatic scenery and historic textures from Eastern Turkey.

{% include gallery id="gallery_eastern" %}
{% endcapture %}

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Ezine</h3>
  <div class="accordion-content" markdown="1">
    {{ ezine_content | markdownify }}
  </div>
</div>

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Eastern Turkey</h3>
  <div class="accordion-content" markdown="1">
    {{ eastern_content | markdownify }}
  </div>
</div>

<script>
  document.addEventListener('DOMContentLoaded', function() {
    const accordions = document.querySelectorAll('.accordion-header');

    accordions.forEach(accordion => {
      accordion.addEventListener('click', function () {
        this.classList.toggle('active');
        const content = this.nextElementSibling;

        if (content.style.maxHeight) {
          content.style.maxHeight = null;
        } else {
          content.style.maxHeight = content.scrollHeight + "px";
        }

        setTimeout(function () {
          if (accordion.classList.contains('active')) {
            content.classList.add('active');
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
    /* Ensure this is large enough for varied height content.
       If you have very tall images, you might need to increase it or use JS to set it dynamically. */
    max-height: 5000px !important; /* Increased for potentially taller content */
  }

  /* ✅ Grid-Based Gallery Layout */
  .accordion-content .gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 1rem;
    align-items: start; /* ADDED: Prevents items in a row from stretching to tallest item's height */
  }

  .accordion-content .gallery a {
    display: block;
    overflow: hidden;
  }

  .accordion-content .gallery img {
    width: 100%;
    height: auto; /* CHANGED: Was 200px. Allows image to set its own height based on aspect ratio */
    display: block; /* ADDED: Good practice for images, removes potential bottom space */
    object-fit: cover; /* With height:auto, this has less effect but is harmless.
                          It ensures the image covers the area if 'a' tag had constraints. */
    border-radius: 4px;
    box-shadow: 0 2px 4px rgba(0,0,0,0.1);
    transition: transform 0.3s ease;
  }

  .accordion-content .gallery img:hover {
    transform: scale(1.03);
  }
</style>

---

For pricing information on prints or to discuss commissioned landscape work, please visit my [pricing page](/pricing/) or [contact me](/contact/) directly.
