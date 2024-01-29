# Angular SQL

AngularJS databasedan ma'lumotlarni ko'rsatish uchun juda mos keladi. Faqat ma'lumotlar JSON formatida ekanligiga ishonch hosil qiling.

### MySQL bilan ishlaydigan PHP serveridan ma'lumotlarni olish

{% code title="AngularJSga misol:" %}
```
<div ng-app="myApp" ng-controller="customersCtrl">

<table>
  <tr ng-repeat="x in names">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $http) {
  $http.get("customers_mysql.php")
  .then(function (response) {$scope.names = response.data.records;});
});
</script>
```
{% endcode %}

### SQL bilan ishlaydigan ASP.NET serveridan ma'lumotlarni olish

{% code title="AngularJS misoli" %}
```
<div ng-app="myApp" ng-controller="customersCtrl">

<table>
  <tr ng-repeat="x in names">
    <td>{{ x.Name }}</td>
    <td>{{ x.Country }}</td>
  </tr>
</table>

</div>

<script>
var app = angular.module('myApp', []);
app.controller('customersCtrl', function($scope, $http) {
  $http.get("customers_sql.aspx")
  .then(function (response) {$scope.names = response.data.records;});
});
</script>
```
{% endcode %}

### Server kodiga misollar

Quyidagi bo'limda SQL ma'lumotlarini olish uchun ishlatiladigan server kodlari ro'yxati keltirilgan.

1. PHP va MySQL dan foydalanish. JSON qaytarilmoqda.
2. PHP va MS Access-dan foydalanish. JSON qaytarilmoqda.
3. ASP.NET, VB va MS Access-dan foydalanish. JSON qaytarilmoqda.
4. ASP.NET, Razor va SQL Lite-dan foydalanish. JSON qaytarilmoqda.

### Cross-Site HTTP Requestlar

Ma'lumotlarni boshqa serverdan so'rash (so'ralayotgan sahifadan tashqari) **saytlararo** **HTTP so'rovlar**i deb ataladi.

Saytlararo so'rovlar Internetda keng tarqalgan. Ko'pgina sahifalar turli serverlardan CSS, rasmlar va skriptlarni yuklaydi.

Zamonaviy brauzerlarda skriptlardan saytlararo HTTP so'rovlari xavfsizlik nuqtai nazaridan **same site** bilan cheklangan.

Quyidagi qator PHP kodimizga saytlararo accessga ruxsat berish uchun qo'shilgan.

```
header("Access-Control-Allow-Origin: *");
```

### 1. Server kodi PHP va MySQL

```
<?php
header("Access-Control-Allow-Origin: *");
header("Content-Type: application/json; charset=UTF-8");

$conn = new mysqli("myServer", "myUser", "myPassword", "Northwind");

$result = $conn->query("SELECT CompanyName, City, Country FROM Customers");

$outp = "";
while($rs = $result->fetch_array(MYSQLI_ASSOC)) {
  if ($outp != "") {$outp .= ",";}
  $outp .= '{"Name":"'  . $rs["CompanyName"] . '",';
  $outp .= '"City":"'   . $rs["City"]        . '",';
  $outp .= '"Country":"'. $rs["Country"]     . '"}';
}
$outp ='{"records":['.$outp.']}';
$conn->close();

echo($outp);
?>
```

### 2. Server kodi PHP va MS Access

```
<?php
header("Access-Control-Allow-Origin: *");
header("Content-Type: application/json; charset=ISO-8859-1");

$conn = new COM("ADODB.Connection");
$conn->open("PROVIDER=Microsoft.Jet.OLEDB.4.0;Data Source=Northwind.mdb");

$rs = $conn->execute("SELECT CompanyName, City, Country FROM Customers");

$outp = "";
while (!$rs->EOF) {
  if ($outp != "") {$outp .= ",";}
  $outp .= '{"Name":"'  . $rs["CompanyName"] . '",';
  $outp .= '"City":"'   . $rs["City"]        . '",';
  $outp .= '"Country":"'. $rs["Country"]     . '"}';
  $rs->MoveNext();
}
$outp ='{"records":['.$outp.']}';

$conn->close();

echo ($outp);
?>
```

### 3. Server kodi ASP.NET, VB va MS Access

```
<%@ Import Namespace="System.IO"%>
<%@ Import Namespace="System.Data"%>
<%@ Import Namespace="System.Data.OleDb"%>
<%
Response.AppendHeader("Access-Control-Allow-Origin", "*")
Response.AppendHeader("Content-type", "application/json")
Dim conn As OleDbConnection
Dim objAdapter As OleDbDataAdapter
Dim objTable As DataTable
Dim objRow As DataRow
Dim objDataSet As New DataSet()
Dim outp
Dim c
conn = New OledbConnection("Provider=Microsoft.Jet.OLEDB.4.0;data source=Northwind.mdb")
objAdapter = New OledbDataAdapter("SELECT CompanyName, City, Country FROM Customers", conn)
objAdapter.Fill(objDataSet, "myTable")
objTable=objDataSet.Tables("myTable")

outp = ""
c = chr(34)
for each x in objTable.Rows
if outp <> "" then outp = outp & ","
outp = outp & "{" & c & "Name"    & c & ":" & c & x("CompanyName") & c & ","
outp = outp &       c & "City"    & c & ":" & c & x("City")        & c & ","
outp = outp &       c & "Country" & c & ":" & c & x("Country")     & c & "}"
next

outp ="{" & c & "records" & c & ":[" & outp & "]}"
response.write(outp)
conn.close
%>
```

### 4. Server kodi ASP.NET, Razor C# va SQL Lite

```
@{
Response.AppendHeader("Access-Control-Allow-Origin", "*")
Response.AppendHeader("Content-type", "application/json")
var db = Database.Open("Northwind");
var query = db.Query("SELECT CompanyName, City, Country FROM Customers");
var outp =""
var c = chr(34)
}
@foreach(var row in query){
if (outp != "") {outp = outp + ","}
outp = outp + "{" + c + "Name"    + c + ":" + c + @row.CompanyName + c + ","
outp = outp +       c + "City"    + c + ":" + c + @row.City        + c + ","
outp = outp +       c + "Country" + c + ":" + c + @row.Country     + c + "}"
}
outp ="{" + c + "records" + c + ":[" + outp + "]}"
@outp
```
