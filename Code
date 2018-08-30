# -*- coding: utf-8 -*-

from random import randint

def generarApuesta(minima,maxima):
    return ((randint((minima/100),(maxima/100)))*100)

def apuestaMinima():
    return (randint(1,10)*100)

def girarDado():
    return  (randint(1,6))

def decision():
    return (randint(0,1))


def turno(dado, apuestaM , apuestaT, dado2):
    
        print("Dado[", dado ,"]")
        print("Apuesta minima: ",apuestaM)
        print("Apuesta turno: " ,apuestaT)
                                                     
        if dado !=6 and dado!=1 :

            if decision() == 0 :
                    print("->NO apuesta a : Dado[", dado ,"]")
                    return 0   
                       
            else:
                                       
                if dado2 <= dado :                        
                    print("Apostando a : Dado[", dado ,"]")
                    print("Segundo Dado[", dado2 ,"]")
                    print("->Apuesta Fallida: ", 0-apuestaT)
                    return 0-apuestaT
                    
                else:
                    print("Apostando a : Dado[", dado ,"]")
                    print("Segundo Dado[", dado2 ,"]")
                    print("->Apuesta Ganada: ", apuestaT)
                    return apuestaT    
        
        else:
            
            if dado == 6:
                print("->Dado[6]...Gana : " , apuestaM)
                return apuestaM
                
            else:
                print("->Dado[1]...Pierde : " , 0-apuestaM)   
                return 0-apuestaM                
                


def juego(mesa, jugador1, jugador2, apuestaM, jugador, dado, dadoN, resultado):
           
    print("___________________________________")
    print("Mesa:$ ",mesa+(resultado*-1))  
    
    
    
    if mesa+(resultado*-1)<=0 or jugador1 <=0 or jugador2 <=0 :
        print("JUGADOR 1: $ ",jugador1) 
        print("JUGADOR 2: $ ",jugador2) 
        print("FIN DEL JUEGO")   
                     
        
    else:    
        
        if jugador == 1:
            print("*JUGADOR 1: $", jugador1)
            juego((mesa+(resultado*-1)),  jugador1 ,(jugador2+resultado) , apuestaM,2,girarDado(),girarDado(),(turno(dado,apuestaM, generarApuesta(apuestaM,mesa),dadoN)))
            
        else:
            print("*JUGADOR 2: $", jugador2)
            juego((mesa+(resultado*-1)), (jugador1+resultado), jugador2 , apuestaM,1,girarDado(),girarDado(),(turno(dado,apuestaM, generarApuesta(apuestaM,mesa),dadoN)))



              
juego (1000, 1000, 1000, 500,1,girarDado(),girarDado(),0)
