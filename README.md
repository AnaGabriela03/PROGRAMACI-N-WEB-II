#CODIGO DEL ARCHIVO VIEWS(POLLS)
from django.shortcuts import render
from django.http import HttpResponse
def index(request):
    return HttpResponse("Hello, World. You'are in the polls index")

#CODIGO DEL ARCHIVO URLS(MYSITE)
from django.contrib import admin
from django.urls import include, path
urlpatterns = [
    path("polls/", include("polls.urls")),
    path('admin/', admin.site.urls),
]

#CODIGO DEL ARCHIVO URLS(POLLS)
from django.urls import path
from . import views
urlpatterns = [
    path("", views.index, name="index")
]
