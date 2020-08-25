---
layout: default
---
{% for post in site.posts limit:5 %}
<div class="container main-card-body">
  <hr>
  <div class="row">
    <div class="col-sm-3 col-xs-12 title-img-col">
      <img class="card-img-top" src="{{site.baseurl}}/assets/images/{{post.image}}" alt="{{post.title}}" />
    </div>
    <div class="col card-title-col">
      <h5 class="card-title"><a href="{{ post.url | prepend: site.baseurl }}">{{post.title}}</a></h5>
      <span class="card-date">{{post.date}}</span>
    </div>
  </div>
   <div class="card-body">
    <p class="card-text">{{post.meta}}</p>
    <a href="{{ post.url | prepend: site.baseurl }}" class="btn card-read-more">Read More</a>
  </div>
</div>
<div class="container">
  <hr />
  <div class="row text-right">
    <div class="col card-btn-bottom">
      <a href="#" class="btn card-btn-pro">{{post.category}}</a>
      
    </div>
  </div>
</div>
      
{% endfor %}