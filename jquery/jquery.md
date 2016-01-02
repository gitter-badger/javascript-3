## jQuery [**Back**](./../README.md)

#### 1. Prefix `$`

- Prefix jQuery objects variables with `$`

```js
/**
 * bad
 */
const sidebar = $('.sidebar');

/**
 * good
 */
const $sidebar = $('.sidebar');
```

#### 2. Cache jQuery object

```js
/**
 * bad
 */
function setSidebar() {
    $('.sidebar').hide();
    
    /**
     * ...
     */
    
    $('.sidebar').css({
        'background-color': 'blue'
    });
}

/**
 * good
 */
function setSidebar() {
    const $sidebar = $('.sidebar');
    $sidebar.hide();
    
    /**
     * ...
     */
    
    $sidebar.css({
        'background-color': 'blue'
    });
}
```

#### 3. Use Cascading or parent > child

- To use Cascading `$('.sidebar ul')` or parent > child `$('.sidebar > ul')`, which named `non-context selector`
- The performance testing of 

```js
$('.sidebar ul').hide();

$('.sidebar > ul').hide();
```

<a href="http://aleen42.github.io/" target="_blank" ><img src="./../pic/tail.gif"></a>