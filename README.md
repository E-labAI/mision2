Instrucciones:
1. Validar que tengas instalado la versión de python 3.10.11

2. Crear una maquina virtual
python -m venv venv

3. Activar la maquina
venv/Scripts/Activate

4. colocar las siguientes lineas que instalan las librerias necesarias para correr el programa
   - pip install sklearn
   - pip install pickle
   - pip install flask
   - pip install flask-cors
   - pip install scikit-learn
   - pip install numpy
   - pip install pandas
   - pip install matplotlib
   - pip install rasa
   - pip install openpyxl

5. Ajustar la siguiente línea de código que se encuentra ubicado en venv/lib/rasa/core/channels/socketio.py

 if self.session_persistence:
            await sio.enter_room(sid, data["session_id"])
            await sio.emit("session_confirm", data["session_id"], room=sid)
* agregar el await en la linea después del if

6. abrir dos poweshell terminal en visual studio y ejecutar en cada terminar lo siguiente:
venv/Scripts/Activate
rasa run actions
rasa run --cors "*"

7. cuando tengan todo listo se ubica en el website.html y le damos clic derecho Open With Live Server

