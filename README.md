# React Progressive Web App (PWA) Example

For running command
Step 1: npm install
Step 2: npm audit fix --force
Step 3: npm run start
quit the terminal once you tested


Step 4:npm run build
After build complete

Step 5: npm install -g serve

Step 6:serve -s build


what is pwa in react side major difference 

1) inside the react app we need to focus on index.js file (registerServiceWorker();)
old react app
serviceWorker.unregister();

pwa react app
registerServiceWorker(); == follow and change this line


2) In public folder index.html file we need to add this line 
<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
  <meta name="theme-color" content="#000000">
  <!--
      manifest.json provides metadata used when your web app is added to the
      homescreen on Android. See https://developers.google.com/web/fundamentals/engage-and-retain/web-app-manifest/
    -->
  <link rel="shortcut icon" href="%PUBLIC_URL%/favicon.ico">
  <link rel="manifest" href="%PUBLIC_URL%/manifest.json">
  <!-- Tell the browser it's a PWA -->
  <meta name="mobile-web-app-capable" content="yes">
  <!-- Tell iOS it's a PWA -->
  <meta name="apple-mobile-web-app-capable" content="yes">
<div class="App">
      <p>
        Loading...
      </p>
    </div>

    <script>
      if ('serviceWorker' in navigator) {
        window.addEventListener('load', function () {
          navigator.serviceWorker.register('service-worker.js').then(function (registration) {
            console.log('ServiceWorker registration successful with scope: ', registration.scope);
          }, function (err) {
            console.log('ServiceWorker registration failed: ', err);
          }).catch(function (err) {
            console.log(err)
          });
        });
      } else {
        console.log('service worker is not supported');
      }
    </script>


How to checkout the PWA works 

in google chrome  install lighthouse extension  it will show the performance of pwa app.


we can store offline it self.
