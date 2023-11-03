function calcularBayes() {
    var probA = parseFloat(document.getElementById("probA").value);
    var probBA = parseFloat(document.getElementById("probBA").value);
    var probB = parseFloat(document.getElementById("probB").value);

    var resultado = (probBA * probA) / probB;
    document.getElementById("resultadoBayes").textContent = resultado;
}

function calcularBernoulli() {
    var probExito = parseFloat(document.getElementById("probExito").value);
    var numIntentos = parseInt(document.getElementById("numIntentos").value);

    var resultado = Math.pow(probExito, numIntentos) * Math.pow(1 - probExito, 1 - numIntentos);
    document.getElementById("resultadoBernoulli").textContent = resultado;
}

function calcularBinomial() {
    var probExito = parseFloat(document.getElementById("probExitoBinomial").value);
    var numIntentos = parseInt(document.getElementById("numIntentosBinomial").value);
    var numExitos = parseInt(document.getElementById("numExitosBinomial").value);

    var combinacion = calcularCombinacion(numIntentos, numExitos);
    var resultado = combinacion * Math.pow(probExito, numExitos) * Math.pow(1 - probExito, numIntentos - numExitos);
    document.getElementById("resultadoBinomial").textContent = resultado;
}

function calcularCombinacion(n, k) {
    function factorial(num) {
        if (num === 0 || num === 1)
            return 1;
        for (var i = num - 1; i >= 1; i--) {
            num *= i;
        }
        return num;
    }
    return factorial(n) / (factorial(k) * factorial(n - k));
}

function calcularPoisson() {
    var lambda = parseFloat(document.getElementById("lambda").value);
    var k = parseInt(document.getElementById("k").value);

    var resultado = (Math.pow(lambda, k) * Math.exp(-lambda)) / factorial(k);
    document.getElementById("resultadoPoisson").textContent = resultado.toFixed(4);
}

function factorial(num) {
    if (num === 0 || num === 1) {
        return 1;
    }
    for (var i = num - 1; i >= 1; i--) {
        num *= i;
    }
    return num;
}
