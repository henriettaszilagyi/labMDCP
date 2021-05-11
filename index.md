<script> 
  allCookies = document.cookie;
  document.cookie = "session=laboratorul 10-11";
  document.cookie = "favorite_task=collect Data from you"; 
  function alertCookie() 
  { 
  alert(document.cookie); } 
</script>
  <body> Bine ai venit la lab <button onclick="alertCookie()">Show cookies</button> 
</body>
