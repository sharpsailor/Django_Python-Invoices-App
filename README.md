### Invoice Project

This Project is part of RiDiv Technologies Assignment for Python/Django Internship
this project problem statements details are as follows:

Assignment Details -


```bash
You need to create a single url /invoices/ for thisCreate a Django application (Django Rest Framework) using the given information:


You need to create a single url /invoices/ for this


/invoices/

/invoices/<int:pk>/


- Create two Django models viz. Invoice and Invoice Detail.

- Invoice model fields -> Date, Invoice CustomerName.

- InvoiceDetail model fields -> invoice (ForeignKey), description, quantity, unit_price, price.

- Create APIs using Django Rest Framework for all the HTTP methods for the invoice models.

- The API should also accept invoice_details in the payload and create/update the associated invoice details too


- Create test cases to test all the API endpoints.
```

## 1. Clone repository

```bash
git clone https://github.com/sharpsailor/Django_Python-Invoices-App.git 
```
## 2. Setup Virtual Environment
```bash
cd Django_Python-Invoices-App
python3 -m venv venv 
source venv/bin/activate
```
## 3.Install requirements
```bash
pip install -r requirements
```

## 4. Runserver Command
```bash
python3 manage.py runserver 8000
```
 This command will run the server on the the local host at Port 8000, you can change the port by passing the port number instead of 8000 here .

## 5. API Endpoints 
    The Api endpoint will be as follows:
- ```localhost:8000/api/invoices``` and this Api endpoint will be the first endpoint  in the list of endpoints i.e /invoices/

- ```localhost:8000/api/invoices/<int:pk>``` and this Api endpoint will be the Second 
endpoint  in the list of endpoints i.e /invoices/<int:pk>/


- Apart from this an endpoint will be present in the list of endpoints which will be
```localhost:8000/api/invoices-details/<int:pk>``` Which will help in adding data reuired to be added in the list which includes the blow fields
    
    -> invoice (ForeignKey), description, quantity, unit_price.

 ```   Price is calculated from the the unit price and quantity
    Price =unit_price * quantity
 ```  

## 6. Test

```bash
python3 manage.py test invoices.tests.InvoiceTests 
```
