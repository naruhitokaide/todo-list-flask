#Flask-Todolist
In this project I explored Flask and some of its great
extensions. The most basic features of most web apps can be found here.

Using the [Skeleton](http://www.getskeleton.com/) CSS framework I tried to achieve a look that is minimal and also modern. Opposed to a lot of small projects which are proof of concepty/exploratory I made a conscious effort to also build something that looks nice. Nonetheless I'm not a designer, so I strived for good enough.

A bit more information can be found here: https://0xfoo.github.io/flask-todolist/

Cross promotion: I'm currently building a quite similar app in Django: https://github.com/0xfoo/django-todolist


### Explore
To try out the app yourself install the requirements.
```
pip install -r requirements.txt
```
For your exploration you might find it useful to have some data. (This takes a moment or two.)
```
python manage.py fill_db
```
And then start the server (default: http://localhost:5000)
```
python manage.py runserver
```

Now you can browse the API:
http://localhost:5000/api/users

Pick a user, login as the user. Default password after fill_db is *correcthorsebatterystaple*.
Click around, there is not to much, but I like the overview under: http://localhost:5000/todolists
(You must be logged in to see it.)


### Extensions

In the process of this project I used a couple of extensions.

Usage               | Flask-Extension  
------------------- | -----------------------
Model & Database    | [Flask-SQLAlchemy](http://flask-sqlalchemy.pocoo.org/2.0/)
Forms               | [Flask-WTF](https://flask-wtf.readthedocs.org/en/latest/)
Login               | [Flask-Login](http://flask-login.readthedocs.org/en/latest/)
Extras              | [Flask-Script](http://flask-script.readthedocs.org/en/latest/)

I tried out some more, but for the scope of this endeavor the above mentioned extensions sufficed.


### Issues

So here a few issues, that are still bothering me and hopefully I will come to later.

 - [ ] In testing I found that login_required was returning the site even when not logged in
 - [ ] find a way to test admin_required views
 - [ ] making the todolist titles editable (maybe with some jQuery magic, or use title forms)
 - [ ] using login_required/admin_required for access control on API
 - [ ] showing some stats on the admin page (currently empty)


### Features (nice to have)

- [ ] **adding groups**
- [ ] automatic updates via [Pub-Sub](http://redis.io/topics/pubsub/) for group todolists ([Websockets](http://lucumr.pocoo.org/2012/9/24/websockets-101/))
- [ ] adding private todolists
- [ ] todo overview + todo deadlines


### License (MIT)
As far as licenses go MIT seemed pretty decent, thus I used it.
