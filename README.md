BUILD INSTRUCTIONS
==================

In some new versions of PyCharm, it doesn't find pycharm_helpers docker-image for remote interpreter. So we can build it manualy.

1 Copy Dockerfile to PyCharm location:

    cp Dockerfile {PyCharm home}/helpers/Dockerfile && cd {PyCharm home}/helpers/
    
2 Build container:

    docker build -t pycharm_helpers:`cat ../build.txt` --label com.jetbrains.pycharm_helpers.version=`cat ../build.txt` .
