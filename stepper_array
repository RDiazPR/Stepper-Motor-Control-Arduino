// subrutinas para controlar el stepper motor 28BYJ-348 con su controlador 
// 
// Hay tres formas para usar esta rutina: 
//
// pasos(cantidad), vuelta completa = 512
//
// vueltas(cantidad), vuelta completa = 1
//
// grados(cantidad), vuelta completa = 360
//
// el signo en la cantidad es la direccion: + = CCW, - = CW
//
//

const char posArray[9] = { 0x08, 0x0C, 0x04, 0x06, 0x02, 0x03, 0x01, 0x09 };

void setup() {

DDRB = 0xFF; //The Port B Data Direction Register - read/write
}

void loop() {


//steps(-512);
//degrees(360);
revolutions(1);
delay(1000);


} //end main loop

void steps(int N){ 
for (int n = 0; n <= abs(N); n++){
  for (int s = 0; s < 8; s++) {
    if(N>=0) PORTB = posArray[s] ;
    else PORTB = posArray[7-s] ;
    delay(1); // must include this short delay!
     } // 8 total combinations
} // repeat N times
}// end function steps

void revolutions(float V) {steps(V*512);};
void degrees(float G) {steps(G/360*512);};
