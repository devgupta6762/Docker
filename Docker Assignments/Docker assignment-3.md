#### Assignment-3
###### 1-	Signup on dockerhub.
###### 2-Login on dockerhub and create a repository by providing repo name “mytestrepo” and a little description about the same.
###### 3-Search for “centos” image on docker using commandline.
    docker search centos
###### 4-Limit out search result to 10 entries only.
    docker search centos --limit=10
###### 5-Apply a filter on search result to show entries for images having 3 stars.
    docker search --filter stars=3 centos
###### 6-Format the search result to get output containing only name,description and is_official values.
    docker search --filter is-official=true --filter stars=3 centos
###### 7-Pull an image named “centos” from dockerhub.
     git pull centos
###### 8-Tag “centos” image with name “mycentos” in your repository with version 1.1
    docker tag centos mytestrepo/mycentos:version1.1
###### 9-Push that image to your repo “mytestrepo” on your dockerhub.
     docker push devgupta262701/mytestrepo:mycentos
###### 10-Do commandline logout on dockerhub.
     docker logout mytestrepo:8080