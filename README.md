<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>

    <form action="">
        
    <input type="number" name="peso" id="peso" required placeholder="Digite seu peso:">
    <input type="text" name="altura" id="altura" required placeholder="Digite sua altura:">
    <input type="submit" value="Calcular">  
    <span>O que é IMC?</span>
    <div class="clear"></div>

    <h1 id="imcNumber"></h1>
    <h2></h2>
    </form>

    <div class="infor-imc">
        <p>IMC é a sigla para Índice de Massa Corporal,que é um cálculo que serve para avaliar se a pessoa está dentro do seu peso ideal em relação à altura. Assim, de acordo com o valor do resultado de IMC, a pessoa pode saber se está dentro do peso ideal, acima ou abaixo do peso desejado.Estar dentro do peso certo é importante porque estar acima ou abaixo desse peso pode influenciar bastante a saúde, aumentando o risco de doenças como desnutrição quando se está abaixo do peso, e AVC ou infarto, quando se está acima do peso. Assim, é comum os médicos, enfermeiros e nutricionistas avaliem o IMC da pessoa nas consultas de rotina para verificar a possibilidade de doenças que a pessoa pode estar pre-disposta.</p>
    </div><!--infor-imc-->
<script src=" https://code.jquery.com/jquery-3.6.0.min.js"></script>
<script src="js/jquery.mask.js"></script>
<script src="js/script.js"></script>
</body>
</html>
