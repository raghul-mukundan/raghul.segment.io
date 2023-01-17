<!-- <!DOCTYPE html> -->
 
<html>
<head>
<title>Sneakerhead Signup<span id="selection-marker-1" class="redactor-selection-marker"></span></title>
 <script>
  !function(){var analytics=window.analytics=window.analytics||[];if(!analytics.initialize)if(analytics.invoked)window.console&&console.error&&console.error("Segment snippet included twice.");else{analytics.invoked=!0;analytics.methods=["trackSubmit","trackClick","trackLink","trackForm","pageview","identify","reset","group","track","ready","alias","debug","page","once","off","on","addSourceMiddleware","addIntegrationMiddleware","setAnonymousId","addDestinationMiddleware"];analytics.factory=function(e){return function(){var t=Array.prototype.slice.call(arguments);t.unshift(e);analytics.push(t);return analytics}};for(var e=0;e<analytics.methods.length;e++){var key=analytics.methods[e];analytics[key]=analytics.factory(key)}analytics.load=function(key,e){var t=document.createElement("script");t.type="text/javascript";t.async=!0;t.src="https://cdn.segment.com/analytics.js/v1/" + key + "/analytics.min.js";var n=document.getElementsByTagName("script")[0];n.parentNode.insertBefore(t,n);analytics._loadOptions=e};analytics._writeKey="LwTBOvunP3AUDjZzRexJGMaO6MuAFVU9";;analytics.SNIPPET_VERSION="4.15.3";
  analytics.load("LwTBOvunP3AUDjZzRexJGMaO6MuAFVU9");
  analytics.page();
  }}();
</script>
</head> 
 
<body>
<h1>Sign up for the latest information on sneaker drops!</h1>
<p>Enter your contact information if you would like to receive alerts about the best sneakers as soon as they drop.</p>
<!--Location for users to enter their information to receive the sneakerhead newsletter-->
<form name="sneakersignup" onsubmit="identify(event)">
<br> <br>
Name: <input name="fullname" required="" size="60" type="text"/>
<br> <br>
Email: <input name="email" required="" size="60" type="email"/>
<br> <br>
<label for="shoeType">Preferred Shoe</label>
 <select id="shoeType" name="shoeType">
   <option value="Running">Running</option>
   <option value="Cross Trainers">Cross Trainers</option>
   <option value="Sports">Sports</option>
 </select>
<br> <br>
 <input name="submit" type="submit" value="submit"/> </form>
<br>
 
<script type="text/javascript">
 function identify(e){
 
   e.preventDefault();
   var form = e.target;
   var email = form["email"].value;
   var fullname = form["fullname"].value;
   var shoeType = form["shoeType"].value;
   var user = {
     email: email,
     name: fullname
   };
 // Identify call
   analytics.identify('12345', {
       email: email,
       name: fullname,
       shoeType: shoeType
    });
  //  Sign-up Track call
     analytics.track('user signed up', user, function() {
       window.location.href = "";
     });
 // Ecommerce Events
    analytics.track('Products Searched', {
     query: 'kith air force 1'
    });
 
    analytics.track('Product List Viewed', {
      list_id: 'hot_sneakers_2021',
      category: 'Trendy',
      products: [ {
        product_id: '507f1f77bcf86cd799439011',
        sku: '45790-32',
        name: 'Air Jordan 4 - White / Military Blue - Fire Red',
        price: 500.00,
        position: 1,
        category: 'Jordan',
        url: 'https://www.example.com/product/path',
        image_url: 'https://www.example.com/product/path.jpg'
      }, {
        product_id: '505bd76785ebb509fc183733',
        sku: '46493-32',
        name: 'Kith x Nike Air Force 1 “NYC”',
        price: 1000.00,
        position: 2,
        category: 'Air Force 1'
    } ] });
 
    analytics.track('Product Viewed', {
      product_id: '507f1f77bcf86cd799439011',
      sku: 'G-32',
      category: 'Jordan',
      name: 'Air Jordan 4 - White / Military Blue - Fire Red',
      brand: 'Nike',
      variant: 'November 2019',
      price: 500.00,
      quantity: 1,
      coupon: 'First_Purchase',
      currency: 'usd',
      position: 2,
      value: 500,
      last_name: 'Bowerman',
      url: 'https://www.example.com/product/path',
      image_url: 'https://www.example.com/product/path.jpg'
    });
 
    analytics.track('Product Added', {
      cart_id: 'skdjsidjsdkdj29j',
      product_id: '507f1f77bcf86cd799439011',
      sku: 'G-32',
      category: 'Jordan',
      name: 'Air Jordan 4 - White / Military Blue - Fire Red',
      brand: 'Nike',
      variant: 'November 2019',
      price: 500.00,
      quantity: 1,
      coupon: 'First_Purchase',
      position: 2,
      url: 'https://www.example.com/product/path',
      image_url: 'https://www.example.com/product/path.jpg'
    });
 
    analytics.track('Order Completed', {
      checkout_id: 'fksdjfsdjfisjf9sdfjsd9f',
      order_id: '50314b8e9bcf000000000000',
      affiliation: 'Google Store',
      total: 555.00,
      subtotal: 500.00,
      revenue: 525.00,
      shipping: 35.00,
      tax: 20.00,
      discount: 30.00,
      coupon: 'First_Purchase',
      currency: 'USD',
      products: [
        {
          product_id: '507f1f77bcf86cd799439011',
          sku: 'G-32',
          name: 'Air Jordan 4 - White / Military Blue - Fire Red',
          price: 500.00,
          quantity: 1,
          category: 'Jordan',
          url: 'https://www.example.com/product/path',
          image_url: 'https:///www.example.com/product/path.jpg'
 
       }
      ]
    });
 }
 
</script>
 
</body>
</html>
