#incluir <Ultrassônico.h>
#incluir <Servo.h>
#incluir "notas_musicais.h"

#definir pinoServo 7
#definir Trigonometria 2
#definir Eco 3
#definir B1A 8
#definir B1B 9
#definir A1A 10
#definir A1B 11

inteirodistanciaD;
inteirodistanciaE;
inteiropino de campainha =6;

flutuadordistanciaObstáculo =35;

Ultrassônicoultrassônico(Trig, Eco);

Servo servo;

vazio configurar() {
Serial.começar(9600);

servo.anexar(pinoServo);
//pinos da ponte H
Modo pin(B1A, SAÍDA);
Modo pin(B1B, SAÍDA);
Modo pin(A1A, SAÍDA);
Modo pin(A1B, SAÍda);
Modo pin(buzzerPin, SAÍDA);

servo.escrever(90);
//Radar();
}

vazio laço() {

Serial.imprimir(ultrassônico.Alcance(

se(ultrassônico.Alcance(CM) <+distar
Andar(5);
Inteirostatus =Radar();
atraso(500);
se(estado ==1)  {
Andar(2);
atraso(600);
Andar(4);
atraso(400);
Andar(5);
}
se(estado ==0) {
Andar(2);
atraso(600);
Andar(3);
atraso(400);
Andar(5);
}
se(estado ==0) {
Andar(2);
atraso(500);
Andar(4);
atraso(300);
Andar(5);
}
atraso(1000);
}
outro{
Andar(1)
}
}

vazio Andar(Inteirodireção) {
se(direção ==1) {//anda pra frente
Escrita digital(B1A, ALTo);
Escrita digital(B1B, BAIXO);
Escrita digital(A1A, ALTO);
Escrita digital(A1B, BAIXO);
}

se(direção ==3) {//faz curva pra direita
Escrita digital(B1A, BAIXO);
Escrita digital(B1B, ALTO);
Escrita digital(A1A, BAIXO);
Escrita digital(A1B, ALTO);
}

se(direção ==4) {//faz curva pra esquerda
Escrita digital(B1A, ALTO);
Escrita digital(B1B, BAIXO);
Escrita digital(A1A, ALTO);
Escrita digital(A1B, BAIXO);
}

se(direção ==4) {//faz curva pra esquerda
Escrita digital(B1A, BAIXO);
Escrita digital(B1B, ALTO);
Escrita digital(A1A, ALTO);
Escrita digital(A1B, BAIXO);
