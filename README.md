# angular_lab

I. ANGULAR.js MVC
  - VIEWS are in charge on almost everything
  - on page first load Angular expects html to see which controllers it should load
  - controllers render the templates which update html
    - can setup data-binding, can fire up AJAX requests
  - cycle repeats
```html
<!DOCTYPE html>
<html>
<head>
  <script src="https://code.angularjs.org/1.5.8/angular.min.js"></script>
  <script>
    var gameApp = angular.module("gameApp", []);
    var games = [
      { name: "Quake", rating: 5 },
      { name: "Bioshock", rating: 3 },
      { name: "Basement Crawl", rating: 1 }];

    gameApp.controller("GameListController", function ($scope) {
      $scope.games = games;
    });
  </script>
</head>

<body ng-app="gameApp">
  <ul ng-controller="GameListController">
    <li ng-repeat="item in games">
      {{ item.name }}: {{ item.rating }} stars
    </li>
  </ul>
</body>
</html>
```




