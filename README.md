# arduino-stepper
control stepper motor 28BYJ-348

Initial code based on:
http://www.instructables.com/id/BYJ48-Stepper-Motor/?ALLSTEPS

User 'urkraft' on this same page greatly simplified the code in the comment section. My contribution uses the same idea and simplifies the application with one of three possible commands:

pasos(N)
vueltas(N)
grados(N)

'N' is the quantity; its sign will indicate the direction (CW or CCW). For reference: 1 Turn = 360 degrees = 512 steps.  
