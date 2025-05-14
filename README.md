# Nabbih
مشروع تطبيق نبّه لمراقبة استهلاك الكهرباء
<!DOCTYPE html>
<html lang="ar">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>نبّه - الصفحة الرئيسية</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      direction: rtl;
      text-align: right;
      background-color: #f9f9f9;
      color: #333;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #4CAF50;
      color: white;
      text-align: center;
      padding: 1rem 0;
    }

    #alert-bar {
      background-color: #ff9800;
      color: white;
      padding: 0.5rem;
      text-align: center;
      font-weight: bold;
    }

    main {
      padding: 1rem;
    }

    section {
      margin-bottom: 2rem;
    }

    canvas {
      max-width: 100%;
      margin: 0 auto;
      display: block;
    }

    footer {
      background-color: #4CAF50;
      color: white;
      text-align: center;
      padding: 1rem 0;
      position: fixed;
      bottom: 0;
      width: 100%;
    }
  </style>
  <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  <header>
    <div id="alert-bar">⚠️ استهلاكك الكلي مرتفع اليوم! حاول تقليل الاستهلاك.</div>
    <h1>نبّه - Nabbih</h1>
    <p>مراقبة ذكية لاستهلاك الكهرباء</p>
  </header>
  <main>
    <section id="summary">
      <h2>ملخص اليوم</h2>
      <p>🌟 <strong>أكثر جهاز استهلاكاً:</strong> المكيف</p>
      <p>🔋 <strong>مستوى الاستهلاك الكلي:</strong> 45 كيلو واط</p>
      <p>💡 <strong>نصيحة اليوم:</strong> افصل الأجهزة غير المستخدمة.</p>
    </section>
    <section id="chart">
      <h2>نسبة استهلاك الأجهزة</h2>
      <canvas id="consumptionPieChart"></canvas>
    </section>
  </main>
  <footer>
    <p>حقوق الطبع © 2025 - تطبيق نبّه</p>
  </footer>
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      const ctx = document.getElementById("consumptionPieChart").getContext("2d");
      
      // بيانات استهلاك الأجهزة
      const data = {
        labels: ["المكيف", "الثلاجة", "الإضاءة", "التلفزيون", "شاحن الجوال"],
        datasets: [{
          data: [40, 25, 15, 10, 10],
          backgroundColor: ["#FF5733", "#33FF57", "#3357FF", "#FFC300", "#DAF7A6"],
        }]
      };

      // تكوين الرسم البياني
      new Chart(ctx, {
        type: "pie",
        data: data,
        options: {
          responsive: true,
          plugins: {
            legend: {
              position: "top",
            },
          }
        }
      });
    });
  </script>
</body>
</html
