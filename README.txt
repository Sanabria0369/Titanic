TITANIC DJANGO API

PASOS:
1. Crear entorno virtual e instalar dependencias:
   python -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt

2. Entrenar el modelo:
   python ml/train_model.py

3. Ejecutar el servidor Django:
   python manage.py migrate
   python manage.py runserver

4. Probar el endpoint:
   POST http://127.0.0.1:8000/api/predict/
   Body JSON:
   {
     "Pclass": 3,
     "Sex": "male",
     "Age": 22,
     "SibSp": 1,
     "Parch": 0,
     "Fare": 7.25,
     "Embarked": "S"
   }
