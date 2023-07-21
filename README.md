<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width,initial-scale=1.0, maximum-scale=1.0, minimum-scale=1.0">
    <title>Reloj despertador</title>
    <!-- UIkit CSS -->
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/uikit@3.6.17/dist/css/uikit.min.css"/>
    <link rel="stylesheet" href="css/estile.css">

    <link rel="shortcut icon" href="img/reloj.png" type="x-icon">
</head>
<body>
    <div class="contenedor">
        <div class="content-clock">
            <div id="date"></div>
            <div class="uk-flex-inline uk-flex-between">
                <div>
                    <button type="button" class="uk-button uk-button-primary btn-alarma" id="btnAlarm"
                        uk-tooltip="tile:Establecer alarma">Alarma</button>
                    <div class="uk-padding-small" uk-dropdown="mode:click">
                        <div class="uk-align-center uk-margin-remove-bottom">
                            <input type="time" value="00:00" id="inputTime">
                            <br>
                            <button type="button" class="uk-button uk-button-primary uk-margin-small"
                                onclick="programar()">
                                Programar
                            </button>
                        </div>
                    </div>
                    <br>
                    <div class="uk-flex-inline uk-flex-between">
                        <span id="show-alarma">Sin alarma</span>
                        <button type="button" class="uk-button-danger" id="btnStop"
                            uk-tooltip="title: Detener">x</button>
                    </div>
                </div>
                <div id="clock">
                    <div class="uk-flex-inline">
                        <div id="hour">00:00</div>
                        <div id="seconds">00</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <audio id="audioTag" src="audio/alarm-clock.mp3"></audio>

    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js"></script>
    <!-- UIkit JS -->

    <script src="https://cdn.jsdelivr.net/npm/uikit@3.6.17/dist/js/uikit.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/uikit@3.6.17/dist/js/uikit-icons.min.js"></script>
    <script type="text/javascript" src="js/app.js"></script>

    <script type="text/javascript">
        $(document).ready(function () {
            getToday()
            //nos queda iniciar el temporizardor en 1 segundo = 1000ms
            setInterval(updateTime, 1000);

    </script>
</body>

</html>
