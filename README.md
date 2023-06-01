# graficas_2d
para subir los archivos 

from tkinter import*

 from tkinter import *
import random

#--------------------
#variables globales
#--------------------
BASE = 460
ALTURA = 220

#--------------------
#ventana principal
#--------------------
ventana_principal = Tk()
ventana_principal.title("graficas 2D")
ventana_principal.resizable(False, False)
ventana_principal.geometry("900x900")
ventana_principal.config(bg= "white")

#----------------------
#frame de graficacion
#----------------------
frame_graficacion = Frame(ventana_principal)
frame_graficacion.config(bg="black", width=480, height=240)
frame_graficacion.place(x=10, y=10)

# funcion para modificar arco 
def modificar_arco(angulo):
    c.intemconfig(arco, exten=angulo)


#creacion canvas 
c = Canvas(frame_graficacion, width=BASE, height=ALTURA)
c.config(bg="yellow")
c.place(x=10, y=10)


# #dibujar una linea recta
# linea_1 = c.create_line(BASE/2, ALTURA/2, BASE,0, fill="red", width=2)
# linea_2 = c.create_line(BASE, ALTURA, BASE/2, ALTURA/2, fill="yellow", width=2)
# linea_3 = c.create_line(0, ALTURA, BASE/2, ALTURA/2, fill="blue", width=2)
# linea_4 = c.create_line(0, 0, BASE/2, ALTURA/2, fill="green", width=2)

# linea_1 = c.create_line(BASE/2, ALTURA/2, BASE/2, 0, fill="pink", width=2)
# linea_2 = c.create_line(BASE/2, ALTURA/2, BASE/2, ALTURA, fill="white", width=2)
# linea_3 = c.create_line(BASE/2, ALTURA/2, 0, ALTURA/2, fill="orange", width=2)
# linea_4 = c.create_line(BASE/2, ALTURA/2, BASE, ALTURA/2, fill="purple", width=2)

#dibujar texto
# texto_1 = c.create_text(BASE/4, ALTURA/2, anchor="center", text="sistemas!!", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
# texto_2 = c.create_text(3*BASE/4, ALTURA/2, anchor="center", text="colegio", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
# texto_3 = c.create_text(BASE/2, ALTURA/4, anchor="center", text="especialidad", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
# texto_2 = c.create_text(BASE/2, 3*ALTURA/4, anchor="center", text="guanenta", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")

#---------------------
#frame de controles
#  dibujar rectangulo
# rect_1 = c.create_rectangle(BASE/2,ALTURA/2,BASE,ALTURA,fill="pink",outline="orange")
# rect_2 = c.create_rectangle(0,0,BASE/2,ALTURA/2, fill="orange")
 
# dibujar circulos
# circ_1 = c.create_oval(BASE/2,0,BASE,ALTURA/2, fill="blue")
# circ_2 = c.create_oval(0,ALTURA/2,BASE/4,ALTURA, fill="yellow")
# circ_3 = c.create_oval(BASE/4,ALTURA/2,BASE/2,ALTURA, fill = "red")

# # dibujar  poligonos
# polig_1 = c.create_polygon(3*BASE/4,ALTURA/2,BASE,ALTURA, BASE/2, ALTURA, fill="red")
# polig_2= c.create_polygon(BASE/4,0,BASE/2,ALTURA/4,BASE/4,ALTURA/2,0,ALTURA/4, fill="white",outline="black")
# cruz = c.create_polygon(BASE/2-25,ALTURA/2-75,BASE/2+25,ALTURA/2-25, BASE/2+75,ALTURA/2-25,BASE/2+75,ALTURA/2+25, BASE/2+25, ALTURA/2+75,BASE/2-25,ALTURA/2+75, BASE/2-25 ,ALTURA/2+25, BASE/2-25,ALTURA/2+25, BASE/2-25, ALTURA/2-25, fill="red")

# tren = c.create_rectangle(BASE/2-30,ALTURA/2-30,BASE/2+30,ALTURA/2+30)
# tren_1 = c.create_rectangle(BASE/2-50,ALTURA/2-50,BASE/2+50,ALTURA/2+50)
# tren_2 = c.create_oval((BASE/2+20,ALTURA/2-20,BASE/2-20,ALTURA/2+20))
# tren_3 = c.create_rectangle(BASE/2+60,ALTURA/2-50,BASE/2-60,ALTURA/2-60)
# tren_4 = c.create_rectangle(BASE/2+40,ALTURA/2-80,BASE/2-45,ALTURA/2-60)


# generar 100 circulos de radio = 10 , y color y posicion aleatoria si salirse del canvas.
for i in range(100):
    # generar color aleatorio  
    color ="#"
    for i in range(6):
        color = color + random.choice("123456789ABCDEF")
    # genera valor de x e y aleatorio
    radio = random.randint(5,25)
    x = random.randint(0, BASE-2*radio)
    y = random.randint(0, ALTURA-2*radio)

    # dibujamos el circulo 
    circulo = c.create_oval(x,y,x+2*radio,y+2*radio, fill=color)

# agregar una imagen canva:
img_nave = PhotoImage(file="img/nave2.png")
nave = c.create_image(BASE/2,ALTURA/2, image=img_nave)

# # frame de graficacion 
frame_graficacion = frame_graficacion =Frame(ventana_principal)
frame_graficacion.config(bg= "green" , width=400, height=240)
frame_graficacion.place(x=10,y=10)

# craeacion canvas 
c = Canvas(frame_graficacion, width= BASE, height=ALTURA)
c.config(bg="black")
c.place(x=18,y=10)

# arco 
arco = c.create_arc(BASE/2-radio,ALTURA/2-radio,BASE/2+radio,ALTURA/2+radio, start=3,extent=0, fill="blue")
#---------------------
frame_controles = Frame(ventana_principal)
frame_controles.config(bg="pink2", width=480, height=230)
frame_controles.place(x=10, y=260)




ventana_principal.mainloop()