# Practica1-contrase-a-
import tkinter as tk

def regis_tro():
    usuario = nombre_usuario.get()
    contraseña = contraseña_usuario.get()
    if usuario == "mauridog" and contraseña == "mau": #validar la contraseña 
        resultado.config(text="Inicio de sesión exitoso")
    else:
        resultado.config(text="Nombre de usuario o contraseña incorrectos")

ventana = tk.Tk()
ventana.title("registro") 
ventana.configure (padx=40) 

nombre_usuario = tk.Entry(ventana)
nombre_usuario.pack(pady=20)
contraseña_usuario=tk.Entry(ventana,show="*")
contraseña_usuario.pack()

regis_tro = tk.Button(ventana, text="iniciar sesion", command=regis_tro)
regis_tro.pack(padx=40, pady=20)
salir = tk.Button(ventana, text="salir", command=ventana.quit)
salir.pack()

resultado = tk.Label(ventana, text="")
resultado.pack(pady=20)

ventana.mainloop()

