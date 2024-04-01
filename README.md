## How to trim a big sentence or paragraph and display where you need.   
 


### Use this snippet 

{% liquid <br/>
  assign words = content | split: ' ' <br/>
  assign truncated = words | slice: 0, limit | join: ' ' <br/>
  if words.size > limit <br/>
    assign truncated = truncated | append: '' <br/>
  endif <br/>
%} <br/>

{{ truncated }}


### How to call 
{% render 'truncate_words' with content: product.title limit: 10 %}
