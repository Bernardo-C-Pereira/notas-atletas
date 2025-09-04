let atletas = [
 {
   nome: "Cesar Abascal",
   notas: [10, 9.34, 8.42, 10, 7.88]
 },
 {
   nome: "Fernando Puntel",
   notas:  [8, 10, 10, 7, 9.33]
 },
 {
   nome: "Daiane Jelinsky",
   notas: [7, 10, 9.5, 9.5, 8]
 },
 {
   nome: "Bruno Castro",
   notas: [10, 10, 10, 9, 9.5]
 }
];

for (let i = 0; i < atletas.length; i++) {
  let notasComputadas = atletas[i].notas.slice();
  let maior = Math.max(...notasComputadas);
  let menor = Math.min(...notasComputadas);

  notasComputadas.splice(notasComputadas.indexOf(maior), 1);
  notasComputadas.splice(notasComputadas.indexOf(menor), 1);

  let soma = 0;

  notasComputadas.forEach(function(nota){
    soma = soma + nota;
    let media = soma / notasComputadas.length;
    atletas[i].media = media.toFixed(2);
  });
}

function exibeInformacoesAtletas(atleta){
  console.log(`Atleta: ${atleta.nome}
Notas Obtidas: ${atleta.notas.join(", ")}
Média Válida: ${atleta.media}
`);
}

atletas.forEach(exibeInformacoesAtletas);
