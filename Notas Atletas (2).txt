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

let notas = atletas[i].notas.slice();
let maior = Math.max(...notas);
let menor = Math.min(...notas);

notas.splice(notas.indexOf(maior), 1);
notas.splice(notas.indexOf(menor), 1);

atletas[i].notas = notas;
let soma = 0;

notas.forEach(function(nota){
soma = soma + nota
let media = soma / notas.length
atletas[i].media = media.toFixed(2)
})


}

console.log (atletas)
