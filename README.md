# Django_rest
an api created with the Django Rest Framework

Here I have followed the tutorial from https://www.django-rest-framework.org/ to learn how to create an api. Here I learned how to make `Serializers`, define their fields by using Django Rest Framework's Serializers class ```HyperlinkedModelSerializer``` and Meta Class (this was my introduction to the Meta Class and type). I made use of Django's class based views and Django Rest Framework decorators to include the Serializers I made and DRF's ```Permissions``` to handle authentication. I use the DRF's ```Viewsets``` to provide list, create, retrieve, update and destroy. There is a permissions.py file to custom define object level permissions in the class ```IsOwnerOrReadOnly``` which we import into views to restrict updating to only authenticated users and create another user class for looking at snippets without accessing them. We build the ```IsOwnerOrReadOnly``` from DRF's `BasePermission` class from `Permissions`. 

The tutorial uses the browsable API so you can login and create snippets in the browser.
