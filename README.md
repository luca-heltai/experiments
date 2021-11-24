# Experiments

## Some jupyter notebooks

These notebooks require fenics_mixed_dimensional branch. To run them use:


    docker run -ti -p 127.0.0.1:8080:8080 \
        -v $(pwd):/home/fenics/shared \
        -w /home/fenics/shared \
        ceciledc/fenics_mixed_dimensional:latest \
        'jupyter-notebook --ip 0.0.0.0 --port 8080'

This will pull the correct docker image, and run a jupyter notebook in it, 
mounting the current directory on `/home/fenics/shared`. After you issue the 
above command, you should see something like 


```    
    To access the notebook, open this file in a browser:
        file:///home/fenics/.local/share/jupyter/runtime/nbserver-15-open.html
    Or copy and paste one of these URLs:
        http://2ca5cc47339c:8080/?token=7ef4a7327149128ca1bdce88aeec928d5ba36a08a4905740
     or http://127.0.0.1:8080/?token=7ef4a7327149128ca1bdce88aeec928d5ba36a08a4905740
```

Notice that the local file above is *inside* the docker image, 
so you don't have access to it from outside. 

To access the notebooks using the right kernel, copy the address
you see on *your* terminal (not the above one!), and paste it in
your favorite browser.