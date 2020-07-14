# kubernetes-helm
this is a resource for me , so i remember how to deploy a docker image


**first of all we should create an account on docker hub repository
and login in terminal with this command :**


```
- docker login --username=yourhubusername --email=youremail@company.com (for the first time , then just type docker login)
```


**to show your previous images :**


```
- docker images
```


you should see something like that :- 


```
REPOSITORY              TAG       IMAGE ID         CREATED           SIZE
verse_gapminder_gsl     latest    023ab91c6291     3 minutes ago     1.975 GB
verse_gapminder         latest    bb38976d03cf     13 minutes ago    1.955 GB
rocker/verse            latest    0168d115f220     3 days ago        1.954 GB
```


**now we will link the image with tag by run this command**


``` docker tag bb38976d03cf yourhubusername/image_name:firsttry ```


**we almost finished , just push your image into hub**


```docker push yourhubusername/image_name```


---------------------------



**now we should create a HELM folder in the project
by run this command : **


```
- helm create $FILE_NAME
```


**and then edit the values to your new values 
now we wanna deploy this helm file ,
(you can use the my-app folder as an example "from Saif Al Nuaimi")**

-------------------------

**how to install kobernetes and use it for deploy a docker image by yaml file (helm)**


**for reinstall microk8s :**

**remove** :

``` sudo snap remove microk8s ```


**install** :

``` sudo snap install microk8s --classic```


**after installing -> check for status** 


```- microk8s.status```


```- microk8s.start```


```- microk8s.config```


```- microk8s.config > ~/.kube/config```


**now if we run this command**


```- kubectl get node```


**we should see the node and the STATUS of it is Ready
now if we run the apply command it should works fine**


```- kubectl apply -f <path>/deployment.yaml```


and DONE.
