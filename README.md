<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Te Quiero Cascada Ordenada</title>
  <style>
    body {
      margin: 0;
      overflow: hidden;
      background: #000;
      font-family: Arial, sans-serif;
    }

    .fall {
      position: absolute;
      top: -20px;
      font-size: 15px;
      color: hsl(50%, 10%, 60%);
      opacity: 1;
      white-space: nowrap;
      pointer-events: none;
      animation: fall 6s linear forwards, colorChange 6s linear forwards;
    }

    @keyframes fall {
      0% {
        transform: translateY(0);
        opacity: 1;
      }
      80% {
        opacity: 0.6;
      }
      100% {
        transform: translateY(110vh);
        opacity: 0;
      }
    }

    @keyframes colorChange {
      0% { color: hsl(0, 100%, 70%); }
      25% { color: hsl(60, 100%, 70%); }
      50% { color: hsl(120, 100%, 70%); }
      75% { color: hsl(180, 100%, 70%); }
      100% { color: hsl(240, 100%, 70%); }
    }
  </style>
</head>
<body>
  <script>
    const screenWidth = window.innerWidth;
    const spacing = 45; // espacio entre columnas
    const columnCount = Math.floor(screenWidth / spacing);
