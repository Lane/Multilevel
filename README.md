Multilevel
==========

jQuery plugin to build a multilevel navigation system out of a nested linked list.

* [Demo](http://www.laneolson.ca/sandbox/Multilevel/demo.html)

## Usage ##

### HTML ###

The navigation structure should be an unordered nested list wrapped in a nav or div tag:

    <nav>
      <ul>
        <li>
          <a href="#">Link One</a>
          <ul>
            <li><a href="#">Link One Sub Item</a></li>
            <li><a href="#">Link One Sub Item</a></li>
            <li><a href="#">Link One Sub Item</a></li>
            <li><a href="#">Link One Sub Item</a></li>
          </ul>
        </li>
        <li>
          <a href="#">Link Two</a>
          <ul>
            <li><a href="#">Link Two Sub Item</a></li>
            <li><a href="#">Link Two Sub Item</a></li>
            <li><a href="#">Link Two Sub Item</a></li>
            <li><a href="#">Link Two Sub Item</a></li>
          </ul>
        </li>
        <li>
          <a href="#">Link Three</a>
          <ul>
            <li><a href="#">Link Three Sub Item</a></li>
            <li><a href="#">Link Three Sub Item</a></li>
            <li><a href="#">Link Three Sub Item</a></li>
            <li><a href="#">Link Three Sub Item</a></li>
          </ul>
        </li>
      </ul>
    </nav>

### CSS ###

    nav { border: 2px solid #000; margin: 0px 20px;}
    nav ul { padding: 0; margin: 0; list-style: none; }
    nav ul li { display: inline-block; position: relative; }
    nav ul li a { display: block; padding: 10px; background: #fff; color: #000; text-decoration: none; }
    nav ul li a:hover { background: #000; color: #fff; }
    nav ul li a strong { float: right; font-size: 8px; margin-top: 5px; }
    nav ul li div { position: absolute; left: -2px; border: 2px solid #000; display: none; padding: 4px; background: #ccc; }
    nav ul li div:after { top: -7px; left: 40px; z-index:6; border-width: 0 7px 7px; border-color: #ccc transparent; content: ""; position:absolute; border-style:solid; display:block; width: 0; }
    nav ul li div:before { top: -10px; left: 38px; z-index:5; border-width: 0 9px 9px; border-color: #000 transparent; content: ""; position:absolute; border-style:solid; display:block; width: 0;  }
    nav ul li div ul { width: 300px; }
    nav ul li div ul li { display: block; }
    nav ul li div ul li ul { display: none; }

### JavaScript ###

Add jQuery and multilevel.js before the closing body tag in your html file:

    <script src="http://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    <script src="multilevel.js"></script>
    
After those two script tags, add the following javascript:

    <script type="text/javascript">
      $('document').ready(function()
      {
      	$('nav').multilevel();
      });
    </script>

## To Do: ##
* Add option to specify wrapper tag