<script> 
  
  document.cookie = "session=laboratorul 10-11";
  document.cookie = "favorite_task=collect Data from you"; 
  allCookies = document.cookie;
  function alertCookie() 
  { 
  alert(allCookies); } 
</script>
  <body> Bine ai venit la lab <button onclick="alertCookie()">Show cookies</button> 
</body>
