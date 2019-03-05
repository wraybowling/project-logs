---
layout: default
description: Access Freely. Ebooks, movies, music, and events free for cardholders.
priority: 1.0
---

<section class="search text-center">
  <div class="cushion">
    <form>
    <select>
      <option>Catalog</option>
      <option>Events</option>
      <option>richlandlibrary.com</option>
    </select>
    <input type="text" placeholder="e.g. 'nikola tesla' or 'ghost towns'">
    <button>Search</button>
    </form>

    <h3>Top Authors</h3>
    <ul>
      <li>Martel, Yann</li>
      <li>Rowling, J.K.</li>
      <li>Vonegut, Kurt</li>
    </ul>
  </div>
</section>

<h3>Events</h3>
<ul>
{% for event in site.events %}
  {% include event.html %}
{% endfor %}
</ul>

<section class="newsletter cushion">
  <form>
  <p>Subscribe to the Richland Library Newsletter and enjoy written wonders delivered straight to your inbox.</p>
  <input type="email" placeholder="Your Email">
  <button>Subscribe</button>
  </form>
</section>
