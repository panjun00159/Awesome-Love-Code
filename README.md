<canvas id="captcha"></canvas>
<input type="text" id="captcha-input" />
<button onclick="verifyCaptcha()">Submit</button>

<script src="https://cdn.jsdelivr.net/npm/captcha.js"></script>
<script>
  var captcha = new Captcha();
  captcha.draw(document.getElementById("captcha"));
  
  function verifyCaptcha() {
      var userInput = document.getElementById("captcha-input").value;
      if (captcha.verify(userInput)) {
          alert("Captcha verified!");
      } else {
          alert("Invalid captcha!");
      }
  }
</script>
