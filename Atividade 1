///
Faça um programa que ao pressionar o botão verde
o LED deverá se acender, pressionando novamente o botão verde
o LED deverá apagar. 
///



void setup() {
  pinMode(25, INPUT);  // Configura o pino 25 como entrada para ler o estado do botão.
  pinMode(21, OUTPUT); // Configura o pino 21 como saída para controlar o LED.
}

int anterior = 0;  // Variável que armazena o estado anterior do botão (inicialmente 0, sem pressionamento).

void loop() {
  int nova = digitalRead(25);  // Lê o estado atual do botão (se foi pressionado ou não).

  if (anterior > nova){  // Verifica se o botão foi pressionado (detecção de borda descendente).
    int led = digitalRead(21);  // Lê o estado atual do LED.
    digitalWrite(21, !led);  // Inverte o estado do LED (se estava aceso, apaga; se estava apagado, acende).
  }
  anterior = nova;  // Atualiza o estado anterior para o estado atual do botão.
  delay(10);  // Atraso de 10 milissegundos para evitar leituras múltiplas indesejadas (debouncing).
}
