
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Graph</title>
    <script type="text/javascript" src="https://www.gstatic.com/charts/loader.js"></script>

</head>

<body>
    <div id="myChart" style="width:100%; max-width:600px; height:500px;">
    </div>

    <script>
        google.charts.load('current', {
            'packages': ['corechart']
        });
        google.charts.setOnLoadCallback(drawChart);

        function drawChart() {
            var data = google.visualization.arrayToDataTable([
                ['Programming', 'Mhl'],
                ['Python', 54.8],
                ['Html', 48.6],
                ['Css', 44.4],
                ['Java Script', 23.9],
                ['My Sql and Mongo Db', 14.5]
            ]);

            var options = {
                title: 'My Programming skill level',
                is3D: true
            };

            var chart = new google.visualization.PieChart(document.getElementById('myChart'));
            chart.draw(data, options);
        }
    </script>
</body>

</html>
