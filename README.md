# graficas_2d
para subir los archivos 

from tkinter import*

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
ventana_principal.geometry("500x500")
ventana_principal.config(bg= "white")

#----------------------
#frame de graficacion
#----------------------
frame_graficacion = Frame(ventana_principal)
frame_graficacion.config(bg="green", width=480, height=240)
frame_graficacion.place(x=10, y=10)

#creacion canvas 
c = Canvas(frame_graficacion, width=BASE, height=ALTURA)
c.config(bg="black")
c.place(x=10, y=10)

#dibujar una linea recta
linea_1 = c.create_line(BASE/2, ALTURA/2, BASE,0, fill="red", width=2)
linea_2 = c.create_line(BASE, ALTURA, BASE/2, ALTURA/2, fill="yellow", width=2)
linea_3 = c.create_line(0, ALTURA, BASE/2, ALTURA/2, fill="blue", width=2)
linea_4 = c.create_line(0, 0, BASE/2, ALTURA/2, fill="green", width=2)

linea_1 = c.create_line(BASE/2, ALTURA/2, BASE/2, 0, fill="pink", width=2)
linea_2 = c.create_line(BASE/2, ALTURA/2, BASE/2, ALTURA, fill="white", width=2)
linea_3 = c.create_line(BASE/2, ALTURA/2, 0, ALTURA/2, fill="orange", width=2)
linea_4 = c.create_line(BASE/2, ALTURA/2, BASE, ALTURA/2, fill="purple", width=2)

#dibujar texto
texto_1 = c.create_text(BASE/4, ALTURA/2, anchor="center", text="sistemas!!", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
texto_2 = c.create_text(3*BASE/4, ALTURA/2, anchor="center", text="colegio", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
texto_3 = c.create_text(BASE/2, ALTURA/4, anchor="center", text="especialidad", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")
texto_2 = c.create_text(BASE/2, 3*ALTURA/4, anchor="center", text="guanenta", font=("Arial", 25, "bold"), fill="blue", activefill="yellow")

# dibujar rectangulo
rect_1 = c.create_rectangle(BASE/2,ALTURA/2,BASE,ALTURA,fill="pink",outline="blue")
rect_2 = c.create_rectangle()

#---------------------
#frame de controles
#---------------------
frame_controles = Frame(ventana_principal)
frame_controles.config(bg="green", width=480, height=230)
frame_controles.place(x=10, y=260)

cross_1 = c.create_arc(3*BASE/2,ALTURA/2, fill="red")

#desplegar ventana
ventana_principal.mainloop()
 