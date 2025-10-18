<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Железнодорожная система</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        
        .container {
            background: white;
            border-radius: 20px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.1);
            overflow: hidden;
            width: 100%;
            max-width: 1000px;
        }
        
        .header {
            background: linear-gradient(135deg, #2c3e50, #34495e);
            color: white;
            padding: 40px;
            text-align: center;
        }
        
        .header h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .header p {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .apps-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 0;
            height: 500px;
        }
        
        .app-card {
            padding: 40px;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            text-align: center;
            cursor: pointer;
            transition: all 0.3s ease;
            border: none;
            background: white;
        }
        
        .app-card:hover {
            background: #f8f9fa;
            transform: scale(1.02);
        }
        
        .app-card:first-child {
            border-right: 2px solid #e9ecef;
        }
        
        .app-icon {
            width: 80px;
            height: 80px;
            background: linear-gradient(135deg, #3498db, #2980b9);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin-bottom: 20px;
            font-size: 2rem;
            color: white;
        }
        
        .app-title {
            font-size: 1.5rem;
            font-weight: bold;
            color: #2c3e50;
            margin-bottom: 10px;
        }
        
        .app-description {
            color: #7f8c8d;
            line-height: 1.5;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            background: #f8f9fa;
            color: #6c757d;
            border-top: 1px solid #e9ecef;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🚆 Система управления железнодорожными операциями</h1>
            <p>Выберите приложение для работы</p>
        </div>
        
        <div class="apps-grid">
            <button class="app-card" onclick="openApp('park_management.html')">
                <div class="app-icon">🏢</div>
                <div class="app-title">Управление вагонным парком</div>
                <div class="app-description">
                    Управление расположением вагонов,<br>
                    отслеживание занятости путей
                </div>
            </button>
            
            <button class="app-card" onclick="openApp('schedule_control.html')">
                <div class="app-icon">📊</div>
                <div class="app-title">Контроль плана-графика</div>
                <div class="app-description">
                    Мониторинг технологических операций,<br>
                    анализ нарушений и отчетность
                </div>
            </button>
        </div>
        
        <div class="footer">
            <p>Железнодорожная система управления © 2024</p>
        </div>
    </div>

    <script>
        function openApp(filename) {
            window.open(filename, '_blank');
        }
    </script>
</body>
</html>
