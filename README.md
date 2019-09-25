<html>
<head>
  <html>
<head>
  <title>Form Validation</title>
  <script type="text/javascript">
    var divs = new Array();
    divs[0] = "errFirst";
    divs[1] = "errLast";
    divs[2] = "errEmail";
    divs[3] = "errUid";
    divs[4] = "errPassword";
    divs[5] = "errConfirm";
    function validate()
	{
      var inputs = new Array();
      inputs[0] = document.getElementById('first').value;
      inputs[1] = document.getElementById('last').value;
      inputs[2] = document.getElementById('email').value;
      inputs[3] = document.getElementById('uid').value;
      inputs[4] = document.getElementById('password').value;
      inputs[5] = document.getElementById('confirm').value;
      var errors = new Array();
      errors[0] = "<span style='color:red'>Please enter your first name!</span>";
      errors[1] = "<span style='color:red'>Please enter your last name!</span>";
      errors[2] = "<span style='color:red'>Please enter your email!</span>";
      errors[3] = "<span style='color:red'>Please enter your user id!</span>";
      errors[4] = "<span style='color:red'>Please enter your password!</span>";
      errors[5] = "<span style='color:red'>Please confirm your password!</span>";
      for (i in inputs)
      {
        var errMessage = errors[i];
        var div = divs[i];
        if (inputs[i] == "")
        	document.getElementById(div).innerHTML = errMessage;
        else if (i==2)
        {
          var atpos=inputs[i].indexOf("@");
          var dotpos=inputs[i].lastIndexOf(".");
          if (atpos<1 || dotpos<atpos+2 || dotpos+2>=inputs[i].length)
        	document.getElementById('errEmail').innerHTML = "<span style='color: red'>Enter a valid email address!</span>";
          else
        	document.getElementById(div).innerHTML = "OK!";
        }
        else if (i==5)
        {
          var first = document.getElementById('password').value;
          var second = document.getElementById('confirm').value;
          if (second != first)
        	document.getElementById('errConfirm').innerHTML = "<span style='color: red'>Your passwords don't match!</span>";
          else
       		document.getElementById(div).innerHTML = "OK!";
        }
        else
        	document.getElementById(div).innerHTML = "OK!";
       }
     }
        function finalValidate()
        {
          var count = 0;
          for(i=0;i<6;i++)
          {
            var div = divs[i];
            if(document.getElementById(div).innerHTML == "OK!")
            count = count + 1;
          }
          if(count == 6)
          	document.getElementById("errFinal").innerHTML = "All the data you entered is correct!!!";
        }
   </script>
</head>
<body>
	<table id="table1">
      <tr>
        <td>First Name:</td>
        <td><input type="text" id="first" onkeyup="validate();" /></td>
        <td><div id="errFirst"></div></td>
      </tr>
      <tr>
        <td>Last Name:</td>
        <td><input type="text" id="last" onkeyup="validate();"/></td>
        <td><div id="errLast"></div></td>
      </tr>
      <tr>
        <td>Email:</td>
        <td><input type="text" id="email" onkeyup="validate();"/></td>
        <td><div id="errEmail"></div></td>
      </tr>
      <tr>
        <td>User Id:</td>
        <td><input type="text" id="uid" onkeyup="validate();"/></td>
        <td><div id="errUid"></div></td>
      </tr>
      <tr>
        <td>Password:</td>
        <td><input type="password" id="password" onkeyup="validate();"/></td>
        <td><div id="errPassword"></div></td>
      </tr>
      <tr>
        <td>Confirm Password:</td>
        <td><input type="password" id="confirm" onkeyup="validate();"/></td>
        <td><div id="errConfirm"></div></td>
      </tr>
      <tr>
        <td><input type="button" id="create" value="Create" onclick="validate();finalValidate();"/></td>
        <td><div id="errFinal"></div></td>
      </tr>
	</table>
</body>
</head>
<body>
  <header>
      <h1>
          No fun No life
      </h1>
      <nav>
          <ul>
              <li>
                   <a href="https://ibrahim-hikari.github.io/entertainment/">
                       Home
                   </a>
               </li>
              <li>
                  <a href="https://omar7100.github.io/entertainment/
">
                      TV-shows
                  </a>
              </li>
              <li>
                  <a href="https://ahmadboxx.github.io/Entertainmentnew/">
                      Anime
                  </a>
              </li>
              <li>
                  <a href="https://obadeh.github.io/ENTERTAINMENT/">
                      Movies
                  </a>
              </li>
              <li>
                  <a href="https://www.facebook.com/ibrahim.ajarmeh.3">
                      Contact us
                  </a>
              </li>
          </ul>
      </nav>
  </header>
  <main>
  <article>
      <section>
      </section>
      <section>
      </section>
  </article>  <main>
       <img src="https://imgix.ranker.com/user_node_img/50084/1001673145/original/l-was-lying-to-the-orphans-about-his-motivations-photo-u1?w=650&q=50&fm=pjpg&fit=crop&crop=faces"/>

   <h3>
       L Lawliet known mononymously as L, is a fictional character and one of the primary protagonists in the manga series Death Note, created by Tsugumi Ohba and Takeshi Obata. He is an enigmatic, faceless, and highly-esteemed international consulting detective who communicates only through his equally inexplicable handler/assistant: Watari, who serves as his official liaison with the authorities. Though his entire past is shrouded in a void of mystery, he has gained a highly-esteemed reputation for solving numerous crime cases and perplexing homicidal mysteries around the globe and is considered to be one of the world's best detectives.
Throughout the series, he observes and spies on the activities of the series' main character, Light Yagami: a high school genius, in an effort to expose him as the infamous serial-killer: "Kira", who is responsible for massacring numerous high-profile criminals around the world, through apparent supernatural means. As the series progresses, the psychological mind-game of cat and mouse between L and Light intensifies, with each one of them being bent on uncovering their true identities, through a series of intricate ploys and schemes, before their cover is blown.
   </h3>
  <article>
      <section>
      </section>
      <section>
      </section>
  </article>
  </main>
  <footer>
      copyrights 2022
  </footer>
</body>
</html>
