
![12](https://user-images.githubusercontent.com/70065792/159885113-340993f1-2b8b-440c-8720-01a3698568b9.PNG)


![13](https://user-images.githubusercontent.com/70065792/159885496-ff4cc78e-fb7c-4d15-a914-437c5f8635dd.PNG)

![2](https://user-images.githubusercontent.com/70065792/159885156-2d3ec076-cc0f-4e13-82b7-f73b33be2f14.PNG)

#### Create virtual environment ===> use git bash

> pip install pipenv

#### Activate virtual environment to create pip file to hold your dependencies

> pipenv shell

#### Install dependencies

> pipenv install flask flask-sqlalchemy flask-marshmallow marshmallow-sqlalchemy

- This creates a Pipfile.lock

#### Run server

> flask run or python app.py

#### To fix could not resolve a package

> Ctrl + Shift + P , then type Python: select interpreter and choose the desired env

#### Create initial db

> To create the initial database, just import the db object from an interactive Python shell and run the SQLAlchemy.create_all() method to create the tables and database:

```javascript
>>> from yourapplication import db
>>> db.create_all()
```

```javascript
Enter the shell mode
from app import db
db.create_all()
```

#### Avoid the strict=True error by not using

- Instead of

```
product_schema = ProductSchema(strict=True)
products_schema = ProductSchema(strict=True,many=True)
```

- Use

```
product_schema = ProductSchema()
products_schema = ProductSchema(many=True)
```

---

#### Post request

```javascript
{
  "name": "samsumg",
  "description": "2022 model",
  "price": 450.90,
  "qty": 2
}
```
