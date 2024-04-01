## How to trim a big sentence or paragraph and display where you need.   
 


### Use this snippet 

#### Make a Snippet called truncate-words.liquid

{% liquid <br/>
  assign words = content | split: ' ' <br/>
  assign truncated = words | slice: 0, limit | join: ' ' <br/>
  if words.size > limit <br/>
    assign truncated = truncated | append: '' <br/>
  endif <br/>
%} <br/>

{{ truncated }}


 
#### Use this code anywhere. To call the content change the product.title  and update the limit  

{% render 'truncate_words' with content: product.title limit: 10 %}
