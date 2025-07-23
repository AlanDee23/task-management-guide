<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Инфографика: Программа лояльности «Хмельницкий»</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;700;900&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #f8f9fa;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 600px;
            margin-left: auto;
            margin-right: auto;
            height: 300px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 350px;
            }
        }
        .gradient-text {
            background: linear-gradient(45deg, #FF6B6B, #FFD166);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            text-fill-color: transparent;
        }
        .flow-arrow {
            font-size: 2rem;
            color: #FFD166;
            line-height: 1;
        }
        .card {
            background-color: white;
            border-radius: 1rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            padding: 1.5rem;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
        }
    </style>
</head>
<body class="bg-[#073B4C] text-gray-800">

    <div class="container mx-auto p-4 md:p-8">

        <header class="text-center mb-12">
            <h1 class="text-4xl md:text-6xl font-black text-white mb-2">Программа лояльности «Хмельницкий»</h1>
            <p class="text-xl md:text-2xl text-[#FFD166]">Ваша выгода в каждой покупке!</p>
        </header>

        <main class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

            <div class="card md:col-span-2 lg:col-span-3 text-center bg-[#118AB2] text-white">
                <h2 class="text-2xl font-bold mb-2">Экономьте на каждой покупке!</h2>
                <p class="text-5xl md:text-7xl font-black gradient-text">до 10%</p>
                <p class="text-2xl font-bold">кэшбэк баллами</p>
            </div>

            <div class="card">
                <h3 class="text-xl font-bold mb-4 text-center">Как это работает? Просто!</h3>
                <div class="space-y-4">
                    <div class="flex items-center p-4 bg-gray-50 rounded-lg">
                        <span class="text-3xl font-bold text-[#06D6A0] mr-4">1</span>
                        <p class="font-bold">балл</p>
                        <span class="text-3xl font-bold text-gray-400 mx-2">=</span>
                        <span class="text-3xl font-bold text-[#06D6A0] mr-4">1</span>
                        <p class="font-bold">рубль</p>
                    </div>
                    <div class="flex items-center p-4 bg-gray-50 rounded-lg">
                         <span class="text-3xl mr-4">🍔+🍺</span>
                         <p class="font-bold">Специальные Комбо-наборы по выгодной цене</p>
                    </div>
                </div>
            </div>

            <div class="card">
                <h3 class="text-xl font-bold mb-4 text-center">Оплачивайте до 100% покупки</h3>
                <p class="text-center text-gray-600 mb-4">Накопленными баллами можно оплатить всю сумму чека.</p>
                <div class="chart-container h-48 md:h-64">
                    <canvas id="paymentDonutChart"></canvas>
                </div>
            </div>
            
            <div class="card">
                 <h3 class="text-xl font-bold mb-4 text-center">Чем больше покупок — тем выше кэшбэк</h3>
                 <p class="text-center text-gray-600 mb-4">Ваш уровень кэшбэка растет вместе с общей суммой ваших покупок.</p>
                 <div class="chart-container">
                    <canvas id="cashbackGrowthChart"></canvas>
                </div>
            </div>

            <div class="card md:col-span-2 lg:col-span-3">
                <h3 class="text-2xl font-bold text-center mb-6">Ваш путь к выгоде — всего 3 шага</h3>
                <div class="flex flex-col md:flex-row items-center justify-around text-center">
                    <div class="flex flex-col items-center p-4">
                        <div class="text-5xl mb-2">📱</div>
                        <h4 class="font-bold text-lg">1. Установите</h4>
                        <p class="text-gray-600">Найдите приложение «Хмельницкий» в App Store или Google Play.</p>
                    </div>
                    <div class="flow-arrow my-4 md:my-0 md:mx-8 transform md:rotate-0 rotate-90">→</div>
                    <div class="flex flex-col items-center p-4">
                        <div class="text-5xl mb-2">✍️</div>
                        <h4 class="font-bold text-lg">2. Зарегистрируйтесь</h4>
                        <p class="text-gray-600">Введите номер телефона и код из СМС. Это займет 1 минуту.</p>
                    </div>
                    <div class="flow-arrow my-4 md:my-0 md:mx-8 transform md:rotate-0 rotate-90">→</div>
                    <div class="flex flex-col items-center p-4">
                        <div class="text-5xl mb-2">💰</div>
                        <h4 class="font-bold text-lg">3. Экономьте!</h4>
                        <p class="text-gray-600">Покажите QR-код из приложения до оплаты и получайте баллы.</p>
                    </div>
                </div>
            </div>
            
            <div class="card lg:col-span-3">
                <h3 class="text-2xl font-bold text-center mb-6">Частые вопросы</h3>
                <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                    <div class="p-4 bg-gray-50 rounded-lg">
                        <p class="font-bold text-[#FF6B6B]">«У меня нет времени»</p>
                        <p class="text-gray-700 mt-1">«Это займёт всего 1-2 минуты, а выгода будет с каждой следующей покупки!»</p>
                    </div>
                    <div class="p-4 bg-gray-50 rounded-lg">
                        <p class="font-bold text-[#FF6B6B]">«Не хочу ничего скачивать»</p>
                        <p class="text-gray-700 mt-1">«Можно установить, сделать скриншот QR-кода и сразу удалить приложение.»</p>
                    </div>
                    <div class="p-4 bg-gray-50 rounded-lg">
                        <p class="font-bold text-[#FF6B6B]">«Я редко у вас бываю»</p>
                        <p class="text-gray-700 mt-1">«Даже небольшие покупки со временем накопят баллы для приятной скидки!»</p>
                    </div>
                    <div class="p-4 bg-gray-50 rounded-lg">
                        <p class="font-bold text-[#FF6B6B]">«Не разбираюсь в приложениях»</p>
                        <p class="text-gray-700 mt-1">«Я с радостью помогу вам пройти все шаги прямо сейчас!»</p>
                    </div>
                </div>
            </div>

            <div class="card md:col-span-2 lg:col-span-3 text-center bg-[#06D6A0]">
                <h3 class="text-2xl font-bold text-[#073B4C]">⚠️ Золотое правило</h3>
                <p class="text-lg text-white font-bold mt-2">Всегда показывайте QR-код кассиру <span class="underline">ДО</span> пробития чека!</p>
            </div>

        </main>

        <footer class="text-center mt-12">
            <p class="text-gray-400">Присоединяйтесь и экономьте с приложением "Хмельницкий"!</p>
        </footer>
    </div>

    <script>
        const tooltipTitleCallback = (tooltipItems) => {
            const item = tooltipItems[0];
            let label = item.chart.data.labels[item.dataIndex];
            if (Array.isArray(label)) {
                return label.join(' ');
            }
            return label;
        };

        const wrapLabel = (label) => {
            const maxLength = 16;
            if (label.length <= maxLength) {
                return label;
            }
            const words = label.split(' ');
            const lines = [];
            let currentLine = '';
            words.forEach(word => {
                if ((currentLine + word).length > maxLength) {
                    lines.push(currentLine.trim());
                    currentLine = '';
                }
                currentLine += word + ' ';
            });
            lines.push(currentLine.trim());
            return lines;
        };
        
        const paymentDonutCtx = document.getElementById('paymentDonutChart').getContext('2d');
        new Chart(paymentDonutCtx, {
            type: 'doughnut',
            data: {
                labels: ['Оплата баллами', 'Остаток'],
                datasets: [{
                    label: 'Оплата покупки',
                    data: [100, 0],
                    backgroundColor: ['#06D6A0', '#E5E7EB'],
                    borderColor: ['#FFFFFF'],
                    borderWidth: 4,
                    hoverOffset: 4
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                cutout: '70%',
                plugins: {
                    legend: {
                        display: false
                    },
                    tooltip: {
                        enabled: false
                    }
                }
            }
        });

        const cashbackGrowthCtx = document.getElementById('cashbackGrowthChart').getContext('2d');
        const originalLabels = ['Новичок (от 0₽)', 'Бывалый (от 3000₽)', 'Свой человек (от 10000₽)', 'Легенда (от 25000₽)'];
        new Chart(cashbackGrowthCtx, {
            type: 'bar',
            data: {
                labels: originalLabels.map(wrapLabel),
                datasets: [{
                    label: 'Процент кэшбэка',
                    data: [3, 5, 7, 10],
                    backgroundColor: ['#FFD166', '#FF6B6B', '#06D6A0', '#118AB2'],
                    borderRadius: 8,
                    barThickness: 25,
                }]
            },
            options: {
                responsive: true,
                maintainAspectRatio: false,
                scales: {
                    y: {
                        beginAtZero: true,
                        grid: {
                            display: false,
                            drawBorder: false,
                        },
                        ticks: {
                            callback: function(value) {
                                return value + '%'
                            },
                            color: '#4B5563'
                        }
                    },
                    x: {
                         grid: {
                            display: false,
                            drawBorder: false,
                        },
                        ticks: {
                           color: '#4B5563'
                        }
                    }
                },
                plugins: {
                    legend: {
                        display: false
                    },
                    tooltip: {
                        callbacks: {
                            title: tooltipTitleCallback,
                            label: function(context) {
                                let label = context.dataset.label || '';
                                if (label) {
                                    label += ': ';
                                }
                                if (context.parsed.y !== null) {
                                    label += context.parsed.y + '%';
                                }
                                return label;
                            }
                        },
                        backgroundColor: '#073B4C',
                        titleColor: '#FFFFFF',
                        bodyColor: '#FFFFFF',
                        padding: 10,
                        cornerRadius: 8,
                        displayColors: false
                    }
                }
            }
        });
    </script>
</body>
</html>
