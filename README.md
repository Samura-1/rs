# rs
	background: -webkit-linear-gradient(134.8deg, rgb(93, 79, 212) 48%, rgb(69, 20, 154) 46%);
  
  
  
@font-face {
font-family: Montserrat; /* Имя шрифта */
src: url(../fonts/Montserrat-Black.ttf); /* Путь к файлу со шрифтом */
}


$(window).on('scroll', function(){
if ( $(window).scrollTop() > 70 ) {
  $('.site-navigation,  .header').addClass('navbar-fixed');
  $("#logo").attr("src","../includes/img/logo2.png");
} else {
  $('.site-navigation,  .header').removeClass('navbar-fixed');
  $("#logo").attr("src","../includes/img/logo.png");
}
});


$(document).ready(function(){
 $(".nav-link,.skroll").on("click", function (event) {
    event.preventDefault();
    var id  = $(this).attr('href'),
      top = $(id).offset().top;
    $('body,html').animate({scrollTop: top}, 900);
  });
});	


@media (min-width: 1200px) {
  .container{
    padding-left: 15px;
    padding-right: 15px;
    margin-right: auto;
    margin-left: auto;
    max-width: 1140px;
    width: 100%;

  }
}
  function select() {
    $.ajax({
      url: 'http://56732123.ffox.site/response.php',
      method: 'GET',
      dataType: 'json',
      success: function(data){
        // Object.values(data);
        let response = data;
        console.log(response);
        response.forEach((item)=>{
          document.querySelector('.post').innerHTML +=``
        });
      },
    });
  };
  
  header('Content-type: application/json; charset=utf8');
