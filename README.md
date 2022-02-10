# index

<!DOCTYPE html>
<!--[if lt IE 7]>      <html class="no-js lt-ie9 lt-ie8 lt-ie7"> <![endif]-->
<!--[if IE 7]>         <html class="no-js lt-ie9 lt-ie8"> <![endif]-->
<!--[if IE 8]>         <html class="no-js lt-ie9"> <![endif]-->
<!--[if gt IE 8]>      <html class="no-js"> <!--<![endif]-->
<html>
    <head>
        <meta charset="utf-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <title>Authentication</title>
        <meta name="description" content="">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="stylesheet" href="">
    </head>
    <body>
            {% for message in messages  %}
            <div class = "alert alert- {{message.tags}} alert dismissable fade show" roles = "alert">
                <strong>Message:</strong>{{message}}
                <button type="button" class = "close" data-dismiss="alert" aria-label="Close">
                <span aria-hidden="true">&times;</span>
                </button>
            </div>
            {% endfor %}     

     <h3>Welcome to geekforGeeks</h3>
        {% if user.is_authenticated %}
        <h3>Hello {{ fname }} </h3>
        <h4>You are succesfully logged in.</h4>

      <button type = "submit"> <a href="/signup">SignUp</a>  </button>
      {% else %}


      <button type = "submit"><a href="/signin">SignIn</a></button>
      <button type = "submit"><a href="/signout">SignOut</a></button>
      {%endif%}
        <script src="" async defer></script>
    </body>
</html>
