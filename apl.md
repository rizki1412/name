<!DOCTYPE html>
<html>
<head>
   <meta charset="UTF-8">
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   <title>Data dengan Jquery 01</title>

   <!-- harus tehubung dengan internet agar Jquery berfungsi, krn CDN -->
   <script src="https://code.jquery.com/jquery-3.5.1.min.js" 
   integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" 
   crossorigin="anonymous"></script>

   <style type="text/css">
      input, button{
         padding:10px;
         margin: 5px
      }
   </style>
</head>
<body>
   <h1>Akses API dengan Jquery ajax</h1>
   <button id="tombol">Load</button><img id="load" src="load.gif">
   <table border="1"></table>
   <script>      
      $().ready(function(){
         $("#load").hide();

         $("#load").click(function(){
            //ajax
            $.ajax({
               dataType: "json",
               url: "https://ibnux.github.io/BMKG-importer/cuaca/wilayah.json", 
               beforeSend: function(){ //proses sebelum ajax berjalan
                  $("#load").show();
               },
               success: function(result){ //berhasil
                  console.log(result);
                  
                  
                  //masukkan kedalam table
                  
                     
                  $("table").append();

                  $("#load").hide();
               }
            });
         });
      });
   </script>
</body>
</html>
