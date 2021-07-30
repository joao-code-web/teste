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
<script>function resetInput() {
    $('input[name=peso]').mask('99.9');
    $('input[name=altura]').mask('9.99');
    //aqui estamos formatando os inputs
}

function Imc() {
    $('input[type=submit]').click(()=> {
        var mac = window.document.getElementById('imcNumber');
        var indice = window.document.querySelector('h2');
        var peso = $('input[name=peso]').val();
        var altura = $('input[name=altura]').val();
        var imc = peso / ((altura * altura));

        function veriImc() {
            const pesoBaixo = 18.5;
            const pesoNormal = 24.9;
            const sobrePeso = 29.9;
            const obesidade = 34.9;
            const obesidadeSevera = 39.9;    
        
            //Essa variaveis são para fazer a verificação da saúde//
            
            if(imc < pesoBaixo) {
                mac.innerHTML = 'Abaixo do peso ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4); 
            } else if(imc < pesoNormal) {
                mac.innerHTML = 'Peso adequado ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4);
            } else if(imc < sobrePeso) {
                mac.innerHTML = 'Sobrepeso ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4); // toPrecision esta formatando a variavel imc
            } else if(imc < obesidade) {
                mac.textContent = 'obesidade ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4);
            } else if(imc < obesidadeSevera) {
                mac.innerHTML = 'obesidade Severa ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4);
            } else {
                mac.innerHTML = 'obesidade Morbida ';
                indice.innerHTML = 'Seu IMC é: ' + imc.toPrecision(4);
            }
        }

    veriImc();
    return false; // se não coloca o 'return false' o site vai atualizar quando o usuario clicar no botão
    }); 
}

function openwindow() {
    $('form span').click(function(e){
        e.stopPropagation();
        $('.infor-imc').show(1000);
    });
}

openwindow();

function fecharJanela(e){
    var element1 = $('body');

    element1.click(function(){
        $('.infor-imc').hide(1000);
    });

    $('form span').click(function(e){
        e.stopPropagation();
    });
}

fecharJanela();


// chamando as funções
resetInput();
Imc();
</script>
</body>
</html>
