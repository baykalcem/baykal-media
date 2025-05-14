---
title: "Portrait Photography"
layout: splash
permalink: /portfolio/portraits/
header:
  overlay_image: /assets/images/portraits-header.jpg
  overlay_filter: 0.3
  caption: "Photo credit: Baykal Media"
excerpt: "Authentic moments and genuine emotions captured through a documentary lens"
gallery_lauren:
  - url: /assets/images/portraits/Baykal_Grad_Shoots-48-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-48-min.jpg
    alt: "Candid portrait of child playing"
  - url: /assets/images/portraits/Baykal_Grad_Shoots-382-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-382-min.jpg
  - url: /assets/images/portraits/Baykal_Grad_Shoots-463-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-463-min.jpg
gallery_hugh:
  - url: /assets/images/portraits/Baykal_Grad_Shoots-155-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-155-min.jpg
  - url: /assets/images/portraits/Baykal_Grad_Shoots-21-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-21-min.jpg
    alt: "Environmental portrait of artist in studio"
  - url: /assets/images/portraits/Baykal_Grad_Shoots-404-min.jpg
    image_path: assets/images/portraits/Baykal_Grad_Shoots-404-min.jpg
---

## Portrait Photography

My portrait photography explores the authentic character and genuine emotions of my subjects. Using a documentary approach with cinematic elements, I create portraits that reveal personality, tell stories, and capture meaningful moments.

{% include gallery caption="A selection of portrait work." %}

## Collections

Explore the galleries below.

### Graduation
{% capture lauren_content %}
Lauren's a 2025 Graduate from UNC-Chapel Hill.

{% include gallery id="gallery_lauren" %}
{% endcapture %}

{% capture hugh_content %}
Hugh's a 2025 Graduate from UNC-Chapel Hill.

{% include gallery id="gallery_hugh" %}
{% endcapture %}

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Lauren's Story</h3>
  <div class="accordion-content" markdown="1">
    {{ lauren_content | markdownify }}
  </div>
</div>

<div markdown="0" class="notice--primary accordion">
  <h3 class="accordion-header">Hugh's Story</h3>
  <div class="accordion-content" markdown="1">
    {{ hugh_content | markdownify }}
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

### My Approach to Portraits

When working with portrait subjects, I focus on:

- **Connection** - Building rapport and trust to capture authentic expressions
- **Environment** - Using meaningful locations that enhance the subject's story
- **Natural moments** - Allowing genuine interactions rather than stiff poses
- **Emotional depth** - Looking for the subtle expressions that reveal character
- **Storytelling** - Creating images that hint at the broader narrative of a person's life

### Portrait Sessions

I offer several types of portrait sessions:

- **Individual Portraits** - Capturing your unique personality and story
- **Family Sessions** - Documenting the connections and dynamics between family members
- **Environmental Portraits** - Photographing people in contexts meaningful to them (workplace, studio, home)
- **Documentary Day-in-the-Life** - Following subjects through their natural routines to capture authentic moments

For information about booking a portrait session, please visit my [pricing page](/pricing/) or [contact me](/contact/) directly.

