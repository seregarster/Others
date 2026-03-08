<!DOCTYPE html>
<html lang="ru">
<head>
<meta charset="utf-8">
<title>Please wait</title>

<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
    background: radial-gradient(circle at 30% 30%, #1f232a, #0e1014);
    font-family: "Segoe UI", system-ui, sans-serif;
    overflow: hidden;
}

/* Fluent окно */
.window {
    width: 640px;
    height: 480px;
    padding: 60px;
    border-radius: 24px;

    background: rgba(255,255,255,0.05);
    backdrop-filter: blur(25px);
    -webkit-backdrop-filter: blur(25px);

    border: 1px solid rgba(255,255,255,0.08);

    box-shadow:
        0 25px 80px rgba(0,0,0,0.6),
        inset 0 1px 0 rgba(255,255,255,0.08);

    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

/* Логотип Windows */
.logo {
    width: 64px;
    height: 64px;
    margin-bottom: 40px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 4px;
}

.logo div {
    background: #4cc2ff;
    animation: glow 4s infinite ease-in-out;
}

.logo div:nth-child(2) { animation-delay: .5s }
.logo div:nth-child(3) { animation-delay: 1s }
.logo div:nth-child(4) { animation-delay: 1.5s }

/* Текст */
.text {
    color: #e6e6e6;
    font-size: 22px;
    margin-bottom: 35px;
    text-align: center;
}

/* Прогресс бар */
.progress {
    width: 80%;
    height: 8px;
    background: rgba(255,255,255,0.08);
    border-radius: 10px;
    overflow: hidden;
}

.bar {
    height: 100%;
    width: 30%;
    background: linear-gradient(90deg, #4cc2ff, #7dd3ff);
    border-radius: 10px;
    animation: loading 3s infinite ease-in-out;
}

/* Подтекст */
.sub {
    margin-top: 25px;
    font-size: 16px;
    color: #9aa3ad;
    animation: fade 2s infinite ease-in-out;
}

/* Анимации */
@keyframes loading {
    0% { width: 10% }
    50% { width: 70% }
    100% { width: 10% }
}

@keyframes fade {
    0%,100% { opacity: 0.5 }
    50% { opacity: 1 }
}

@keyframes glow {
    0%,100% { opacity: 0.6 }
    50% { opacity: 1 }
}
</style>
</head>

<body>

<div class="window">

    <div class="logo">
        <div></div>
        <div></div>
        <div></div>
        <div></div>
    </div>

    <div class="text">ЗАГРУЗКА СИСТЕМЫ...<br>
                      ОСТАЛОСЬ 30 МИНУТ...</div>

    <div class="progress">
        <div class="bar"></div>
    </div>

    <div class="sub">Проверка доступности сервиса...</div>

</div>

</body>
</html>
