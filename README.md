# my_3_angular
<html ng-app="clockapp">
    <head>
        <title>clock app</title>
        
         <script src="angular.js"></script>
    </head>

    <body>
        <h1>Clock App</h1>
       
        <div ng-controller="timectrl">
            <!<p ng-bind="timestring"--><!insted of this we use next given function->
          
            <p>curret time is:{{timestring}} </p>
        </div>
         

        <script>
          var app = angular.module("clockapp",[]);
          app.controller("timectrl",caltime);
          
          function caltime($scope)
          {
              var currentdate=new Date();
              //var timestring=currentdate.toTimeString();//to get time use this method in javascript
              $scope.timestring =currentdate.toTimeString();//insted of variable we use proprty of scope as currenttime
             
          }
          
        </script>
    </body>
</html>
