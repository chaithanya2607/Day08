Day08
# 1a] Solving problems using array functions on rest countries data.

----#html code
      <!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <script src = "guvitask.js"></script>
</body>
</html>
# 1b] Get all the countries from Asia continent /region using Filter function.

----   var request=new XMLHttpRequest();
       request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
       request.send();
       request.onload=function(){
       var result=JSON.parse(request.response);
       console.log(result);
       var country=result.filter((ele)=>ele.region==="Asia");
       console.log(country);
       }

# 1c] Get all the countries with a population of less than 2 lakhs using Filter function.

----  var request=new XMLHttpRequest();
      request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
      request.send();
      request.onload=function(){
      var result=JSON.parse(request.response);
      console.log(result);
      var country=result.filter((ele)=>ele.population < 200000);
      console.log(country);
      }

# 1d] Print the following details name, capital, flag using forEach function.

----  var request=new XMLHttpRequest();
      request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
      request.send();
      request.onload=function(){
      var result=JSON.parse(request.response);
      console.log(result);
      var country=result.forEach(element => {
      console.log(element.name+"----> "+element.capital+"----> "+element.flag);
      });
      }

# 1e] Print the total population of countries using reduce function.

----  var request=new XMLHttpRequest();
      request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
      request.send();
      request.onload=function(){
      var result=JSON.parse(request.response);
      console.log(result);
      var country=result.reduce((acc,ele)=>acc+ele.population);
      console.log(country);
     }

# 1f] Print the country which uses US Dollars as currency.

----  var request=new XMLHttpRequest();
      request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
      request.send();
      request.onload=function(){
      var result=JSON.parse(request.response);
      console.log(result);
      var country=result.filter((ele)=>ele.currencies[0].name==="United States dollar");
      console.log(country);
      }
