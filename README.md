# Nabbih
مشروع تطبيق نبّه لمراقبة استهلاك الكهرباء
<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>نبّه - Nabbih</title>
    <link rel="stylesheet" href="styles.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
  body {
  font-family: Arial, sans-serif;
  direction: rtl;
  margin: 0;
  padding: 0;
  background-color: #f4f4f4;
  color: #333;
}

header {
  background-color: #f44336;
  color: white;
  text-align: center;
  padding: 1rem;
}

.alert-bar {
  font-weight: bold;
}

main {
  padding: 2rem;
}

.summary {
  background: #fff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  margin-bottom: 2rem;
}

.summary .stats p {
  margin: 0.5rem 0;
}

.chart {
  background: #fff;
  padding: 1.5rem;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}
    <header>
        <h1>نبّه - Nabbih</h1>
        <nav>
            <a href="index.html" class="active">الرئيسية</a>
            <a href="devices.html">تفاصيل الأجهزة</a>
        </nav>
        <div id="alert-bar">⚠️ استهلاكك مرتفع اليوم! حاول تقليل استخدام الأجهزة.</div>
    </header>
    <main>
        <section id="summary">
            <h2>ملخص اليوم</h2>
            <p>أكثر جهاز استهلاكاً: <strong>المكيف</strong></p>
            <p>مستوى الاستهلاك الكلي: <strong>15 كيلو واط</strong></p>
            <p>نصيحة اليوم: <em>استخدم الغسالة في ساعات الليل لتقليل التكلفة.</em></p>
        </section>
        <section id="chart">
            <h2>نسبة استهلاك الأجهزة</h2>
            <canvas id="consumptionChart"></canvas>
        </section>
    </main>
    <footer>
        <p>© 2025 - نبّه</p>
    </footer>
    <script src="script.js"></script>
</body>
</html>
