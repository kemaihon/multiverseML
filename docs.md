publicar
https://blog.alura.com.br/como-publicar-seu-codigo-python-no-pypi/
python setup.py sdist
twine upload dist/* --repository-url https://test.pypi.org/legacy/
twine upload dist/* --repository-url https://upload.pypi.org/legacy/
git
https://support.codebasehq.com/articles/getting-started/git-on-windows
https://anaconda.org/anaconda/git

exemplo 
request
dicti = {"columns":["alcohol", "chlorides", "citric acid", "density", "fixed acidity", "free sulfur dioxide", "pH", "residual sugar", "sulphates", "total sulfur dioxide", "volatile acidity"],"data":[12.8, 0.029, 0.48, 0.98, 6.2, 29, 3.33, 1.2, 0.39, 75, 0.66]}
import requests
url = 'http://localhost:5000/api'
r = requests.post(url,json=dicti)
print(r.json())

exemplo curl
curl -X POST -H "Content-Type: application/json"  -d '{ "columns": [        "alcohol",        "chlorides",        "citric acid",        "density",        "fixed acidity", "free sulfur dioxide",        "pH",        "residual sugar",        "sulphates",        "total sulfur dioxide",        "volatile acidity"    ],    "data": [        12.8,        0.029,        0.48,        1.98,        6.2,        29,        3.33,        1.2,        0.39,        75,        0.66    ]}' \
http://localhost:5000/api