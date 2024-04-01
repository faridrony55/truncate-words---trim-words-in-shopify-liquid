## How to trim a big sentence or paragraph and display where you need.   
## I am using for product title


### Use this snippet 

{% liquid
  assign words = content | split: ' '
  assign truncated = words | slice: 0, limit | join: ' '
  if words.size > limit
    assign truncated = truncated | append: ''
  endif
%}
{{ truncated }}



### How to call 
{% render 'truncate_words' with content: product.title limit: 10 %}
