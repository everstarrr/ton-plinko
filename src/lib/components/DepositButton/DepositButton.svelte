<script>
    // Адрес вашего кошелька и сумма перевода
    const address = 'UQAayY0L5dpPaYWbhrHV9K58zYvUZNV272EZwFDnVZNhN7yX';  // Замените на реальный адрес
    const amount = '100000000'; // Сумма перевода в нанотонах (TON * 10^9)

    // Формируем ссылку для открытия в Tonkeeper
    const tonkeeperLink = `tonkeeper://transfer/${address}?amount=${amount}`

    // Функция для перенаправления
    const redirectToTonkeeper = () => {
        window.location.href = tonkeeperLink;
    };
</script>

<!-- HTML-код кнопки -->
<button on:click={redirectToTonkeeper} class="tonkeeper-button">
    Tonkeeper
</button>

<style>
    .tonkeeper-button {
        padding: 10px 20px;
        background-color: #0088cc;
        color: white;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }

    .tonkeeper-button:hover {
        background-color: #006699;
    }
</style>