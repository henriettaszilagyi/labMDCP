<script> 
  
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
</script>
  <body>
  <button onclick="alertCookie()">Show cookies</button>
  <button onclick="alertCookieValue()">Show cookie value</button>
</body>
