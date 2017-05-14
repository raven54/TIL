## jQuery basics

### simple active class menu

jQuery
``` bash
$(document).ready(function(){
  $('ul li').click(function(){
    $('ul li').removeClass('active');
    $(this).addClass('active');
  });
});
```
ex : http://codepen.io/raven54/pen/vmjzVd
