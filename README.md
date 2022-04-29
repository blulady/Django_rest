# Django_rest
An API created with the Django Rest Framework<br>

Here I have followed the tutorial from https://www.django-rest-framework.org/ to learn how to create an API. I learned how to make `Serializers`, define their fields by using Django Rest Framework's `Serializers` class `HyperlinkedModelSerializer`, to represent relationships using a url instead of a primary key, and Meta Class (this was my introduction to the Meta Class and type).The tutorial guided me in naming the URL patterns. <br><br>
I made use of Django's class based views and Django Rest Framework decorators to include the `Serializers` I made and DRF's `Permissions` to handle authentication. I use the DRF's `Viewsets` to provide CRUD procedures. <br><br>
I created a permissions.py file to custom define object level permissions in the class `IsOwnerOrReadOnly` which we import into views to restrict updating to only authenticated users and create another user class for looking at snippets without accessing them. We build the `IsOwnerOrReadOnly` from DRF's `BasePermission` class from `Permissions`. <br><br>
I also make use of the `ReadOnlyModelViewSet` class from Django Rest Framework's viewsets to create the read only views. Then multiple views are created from each ViewSet class by binding the HTTP methods to the action for each view and registering them with the URL conf utilizing `format_suffix_patterns` to add provide an endpoint for the API.<br>
The tutorial uses the browsable API so you can login and create snippets in the browser.<br><br>
http responses
![image](https://user-images.githubusercontent.com/67162265/165794613-47070456-b5db-406d-baad-ddc52abe3ff4.png) <br>
browsable API
![image](https://user-images.githubusercontent.com/67162265/165794847-2495d397-e2e8-4608-8515-8e2618503f02.png)
logged into browsable API
![image](https://user-images.githubusercontent.com/67162265/165795321-16b70b6c-7a1e-4a8c-9f8d-ffd2d811d155.png)
choosing data format
![image](https://user-images.githubusercontent.com/67162265/165796110-b1649b8a-edab-4285-9459-1b07f2405840.png)
data in API format
![image](https://user-images.githubusercontent.com/67162265/165796710-594bb349-31e5-419a-a67d-e3b7cb9f390a.png)
data in JSON format
![image](https://user-images.githubusercontent.com/67162265/165796877-03054da4-e064-4230-be69-1529269c062a.png)
