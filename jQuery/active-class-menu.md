## jQuery basics

### simple active class menu

``` bash
$(document).ready(function(){
  $('ul li').click(function(){
    $('ul li').removeClass('active');
    $(this).addClass('active');
  });
});
```
ex : http://codepen.io/raven54/pen/vmjzVd
