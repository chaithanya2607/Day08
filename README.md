# Day08
# 1
# a] Solving problems using array functions on rest countries data.
----
# b] Get all the countries from Asia continent /region using Filter function.
----   var request=new XMLHttpRequest();
       request.open("GET","https://raw.githubusercontent.com/rvsp/restcountries-json-data/master/res-countries.json");
       request.send();
       request.onload=function(){
       var result=JSON.parse(request.response);
       console.log(result);
       console.log(result[0].name);
       var country=result.filter((ele)=>ele.region==="Asia");
       console.log(country);
       }

# c] Get all the countries with a population of less than 2 lakhs using Filter function.
----

# d] Print the following details name, capital, flag using forEach function.
----

# e] Print the total population of countries using reduce function.
----

# f] Print the country which uses US Dollars as currency.
----
