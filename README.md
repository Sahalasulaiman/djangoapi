# djangoapi
django token authentication

RUN PROJECT

REGISTRATION
use our terminal then migrate our project, create super user(python manage.py createsuperuser),then run our project using python manage.py runserver
after run project click to link to go django administrate.then we have to open postman Api administrate to create a register collection then set post and url path
the inside of body write {"username":"name","email":"name@gmail.com","password":"pass123","password2":"pass123"}then click send. recive  response:registered

LOGIN
open postman API administrate  create login inside of collection  set POST method and set URL.then inside of body select form-data then enter username and password then click to send. then get the output is Token :"/tokenno". create another file in postman collection . name  is Welcome  then header section  to input autherization and user token
to get the result is username and userid

GET USER
create a file in postman collection userDetails, then set Get and url(http://127.0.0.1:8000/userDetails/1/) then click SEND ,then show our output userdetails(username,email,lastname and first name)
 
UPDATE USER
 open postman select file userDetails,then set PUT function and url(http://127.0.0.1:8000/userDetails/1/)then inside of body writte{"username":"dela","email":"dela@gmail.com","first_name":"naju","last_name":"hj"}then get updated output (first name and lastname in first user).

SEARCH USER
create another file inside of our postman collection name is pagination open the file set GET function and url ( http://127.0.0.1:8000/paginationApi?search=dela)
get the output is user dela details, then another way to check using email (http://127.0.0.1:8000/paginationApi?search=dela@gmail.com).
