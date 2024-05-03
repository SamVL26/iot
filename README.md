pandas
openpyxl
import pandas as pd
from flash import flash

app=Flask(_Name_)

base=pd.read_excel("pokemones.xlsx")

@app.router("/")
def Principal():
  return "Esta es una API que te muestra Pokemones"

@app.router("Por numero(<Numero)")
def PorNumero(Numero):
  Numero=int(Numero)
  fila=base[base["Numero"]==Numero]
  respuestas=f"El pokemon (Numero) es(fila.loc[:,'Nombre'])"
  return respuesta

@app.router("/Por_Tipo/<Tipo>")
def PorTipo(Tipo):
  resultados-base[base["Tipo"]==Tipo]
  Resultados= str (resultados)
  return resultados 

@app.router("/Por_Ataque/Defensa/Velocidad>")
def PorAtaque(Ataque):
  Peso1=float(Defensa)
  Peso2=float(Velocidad) 
  resultados=base[("base["Ataque]Defensa)&(base["Ataque"]>Velocidad)]
  return resultados
print(PorAtaque(30))

app.run()
