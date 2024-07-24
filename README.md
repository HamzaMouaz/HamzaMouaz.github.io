# hamzamouaz.github.graduateproject
<!DOCTYPE html>
{% load static %}
<!-- Created By CodingLab - www.codinglabweb.com -->
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Login Form | Joshyvibe</title> 
    <link rel="stylesheet" href="{% static 'css/styles.css' %}">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.2/css/all.min.css"/>
  </head>
  <body>
    <div class="container">
      <div class="wrapper">
        <div class="title"><span>Welcome Lets login</span></div>
        <form name="LoginForm" action="{% url 'login' %}" method="post"> <!-- Remplacez 'redirect_page' par le nom de votre vue de redirection -->
            {% csrf_token %}
          <div class="row">
            <i class="fas fa-user"></i>
            <input type="username" id="id_username" name="username" placeholder="Email or Phone" required>
          </div>
          <div class="row">
            <i class="fas fa-lock"></i>
            <input type="password" id="id_password" name="password" placeholder="Password" required>
          </div>
          <div class="pass"><a href="#">Forgot password?</a></div>
          <div class="row button">
            <input type="submit">
          </div>
          <div class="signup-link">Not a member? <a href="{% url 'signup' %}">Signup now</a></div>
        </form>
      </div>
    </div>

  </body>
</html>
