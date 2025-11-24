# mi-flask
from flask import Flask
app = Flask(__name__)
@app.route("/")
def inicio():
	return "Bienvenido a mi pagina principal"

 
@app.route("/que rollo preciosa")
def saludo():
	return "Hola! Esta es la pagina del saludo"


@app.route("/usuario/<nombre>")
def usuario(nombre):
	return f"hola {nombre}, bienvenido a tu pagina personalizada"


if __name__ == "__main__":
	app.run(debug=True)
