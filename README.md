# t2tanic webapp

![T2taNic](https://images.chosun.com/resizer/gE-go0I5-2QsuwlgUUavoU3SfiI=/616x0/smart/cloudfront-ap-northeast-1.images.arcpublishing.com/chosun/TPUMVAPDGDTDD2ST4RDJB56LVU.jpg)

## ENV
- python 3.9

- pyenv
```
$ pyenv install --list
$ pyenv install 3.9.16
$ pyenv global 3.9.16
$ pyenv versions
pyenv versions
  system
  3.7.16
* 3.9.16 (set by /Users/js/.pyenv/version)
```

- pipenv
```
$ pip install pipenv
$ pipenv --python 3.9.16
$ pipenv shell
```

## DEV
```
$ pipenv shell
$ pipenv install streamlit
```

## RUN
- streamlit run app.py

## DEPLOY
```
$ docker build -t titanic-ti:0.1.0
$ docker images titanic-ti
REPOSITORY        TAG       IMAGE ID       CREATED          SIZE
titanic-ti   0.1.0     c891796ee3ba   18 seconds ago   1.05GB

$ docker run --name titanic010 -d -p 8501:8501 titanic-ti:0.1.0
$ sudo docker ps
CONTAINER ID   IMAGE                     COMMAND                  CREATED         STATUS                            PORTS                                                 NAMES
b17d1a501ee9   titanic-ti:0.1.0     "streamlit run app.p…"   7 seconds ago   Up 6 seconds (health: starting)   8501/tcp, 0.0.0.0:8501->8501/tcp, :::8501->8501/tcp   titanic010
```

## REF
- https://30days.streamlit.app/?challenge=Day2
