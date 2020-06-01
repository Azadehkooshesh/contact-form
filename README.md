# contact-form
HTML5 Css3

HTML Code:
<html lang="en">
<head>
    <title> Contact Us Form  </title>
    <meta charset="UTF-8"/>
    <link rel="stylesheet" href="styles.Css.css">


</head>
<body>
<div class="wrapper">
    <div class="contact-form">
        <div class="input-fields">
            <input type="text" class="input" placeholder="Name">
            <input type="text" class="input" placeholder="Email Address">
            <input type="text" class="input" placeholder="Phone">
            <input type="text" class="input" placeholder="subject">

        </div>
        <div class="msg">
            <textarea placeholder="Message"></textarea>
            <div class="btn">Send</div>
        </div>
        
    </div>
</div>

</body>
</html>

css Code:
@import url('https://fonts.googleapis.com/css?family=Ibarra+Real+Nova&display=swap');

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    outline: none;
    font-family: 'Ibarra Real Nova', serif;

}
body {
   background: url('aa.jpg') no-repeat top center;
    background-size: cover;
    height: 100vh;
}
.wrapper{
    position: absolute;
    top: 50%;
    transform: translateY(-50%);
    width: 100%;
    padding: 0 20px;
}
.contact-form{
    max-width: 550px;
    margin: 0 auto;
    background: rgba(0,0,0,0.8);
    padding: 30px;
    border-radius: 5px;
    display: flex;
    flex-direction: row;
    box-shadow: 0 0 10px rgba(0,0,0,0.13);
}
.input-fields{
    display: flex;
    flex-direction: column;
    margin-right: 4%;
}
.input-fields,
.msg{
    width: 48%;
}
.input-fields .input,
.msg textarea {
    margin: 10px 0;
    background: transparent;
    border: 0;
    border-bottom: 2px solid darkred;
    padding: 10px;
    color: darkred;
    width: 100%;
}
.msg textarea {
    height: 212px;
}
::-webkit-input-placeholder{
    color: darkred;
}
::-moz-input-placeholder{
    color: darkred;
}
::-ms-input-placeholder{
    color: darkred;
}
.btn{
    background: none;
    text-align: center;
    padding: 15px 20px;
    border-radius: 5px;
    color: #fff;
    text-transform: uppercase;
    border: 1px solid darkred;
    font-size: 20px;
    cursor: pointer;
    margin: 10px;
    transition: 0.8s;
    position: relative;
    overflow: hidden;

}
.btn:hover{
    color: darkred;
}
.btn::before{
    content:"";
    position: absolute;
    left: 0;
    width: 100%;
    height: 0%;
    background: darkred;
    z-index: -1;
    transition: 0.8s;

}
.btn::before{
    top: 0;
    border-radius: 0 0 50% 50% ;
}
.btn:hover::before{
    height: 180%;

}
@media  screen and (max-width: 600px){
    .contact-form {
        flex-direction: column;
    }
    .msg textarea{
        height: 80px;
    }
    .input-fields,
    .msg{
        width: 100%;
    }
}
