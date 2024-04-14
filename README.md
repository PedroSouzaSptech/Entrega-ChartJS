# Entrega-ChartJS,

-- Exercicio 01
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exercicio ChartsJs</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>

<body>
  <div>
    <canvas id="myChart"></canvas>
  </div>

</body>

</html>
  <script>
    const DATA_COUNT = 7;
    const NUMBER_CFG = {
      count: DATA_COUNT,
      min: -100,
      max: 100
    };

    const labels = ['12:00', '13:00', '14:00', '15:00', '16:00', '17:00', ];
    const temperatura = [30, 29, 28, 25, 22, 23];
    const umidade = [80, 82, 80, 85, 80, 83];
    const data = {
      labels: labels,
      datasets: [{
          label: 'Temperatura',
          data: temperatura,
          borderColor: 'red',
          backgroundColor: 'rgba(255, 0, 0, 0.5)'
        },
        {
          label: 'Umidade',
          data: umidade,
          borderColor: 'blue',
          backgroundColor: 'rgba(0, 0, 255, 0.5)'
        }
      ]
    };

    const config = {
      type: 'line',
      data: data,
      options: {
        responsive: true,
        plugins: {
          legend: {
            position: 'top',
          },
          title: {
            display: true,
            text: 'Entrega grafico em Linha'
          }
        }
      },
    };

    const ctx = document.getElementById('myChart').getContext('2d');
    new Chart(ctx, config);
  </script>


-- Exercicio 02
<!DOCTYPE html>
<html lang="en">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exercicio ChartsJs</title>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>

<body>
  <div>
    <canvas id="myChart"></canvas>
  </div>


</body>

</html>
<script>
  const DATA_COUNT = 7;
  const NUMBER_CFG = { count: DATA_COUNT, min: 0, max: 100 };

  const labels = ['Janeiro', 'Fevereiro', 'Março', 'Abril', 'Maio', 'Junho'];
  const temperatura = [22, 24, 27, 23, 20, 18];
  const umidade = [90, 89, 93, 87, 88, 82];

  const data = {
    labels: labels,
    datasets: [
      {
        label: 'Temperatura 1',
        data: temperatura,
        backgroundColor: 'red',
      },
      {
        label: 'Umidade 2',
        data: umidade,
        backgroundColor: 'blue',
      },
    ]
  };

  const config = {
    type: 'bar',
    data: data,
    options: {
      responsive: true,
      plugins: {
        legend: {
          position: 'top',
        },
        title: {
          display: true,
        text: 'Entrega ChartJS'
        }
      }
    }
  };

  const ctx = document.getElementById('myChart').getContext('2d');
  new Chart(ctx, config);
</script>
