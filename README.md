## Bioinformatics tool blastn Jupyter Docker analysis

This example contains a Dockerfile which includes two research tools and a sample notebook:
 - Jupyter notebook container pulled from [source](https://github.com/jupyter/docker-stacks/tree/master/base-notebook).  
 - blastn bioinformatics tool (installed during the container build via `apt-get...`)
 - Jupyter notebook blastn example based on the blastn tutorial from [source](https://github.com/edamame-course/BLAST-tutorial/blob/master/running-BLAST.md). 
 
 ### How to use this Dockerfile
 
 A. To start an instance using the pre-built container image on DockerHub
 1) Verify the [image on DockerHub](https://hub.docker.com/r/lynnlangit/blastn-jupyter-docker/)  
 2) Get a local copy of the image from Docker Hub by running `docker pull lynnlangit/blastn-jupyter-docker`
 3) Start an instance of the image by running `docker run -p 8888:8888 lynnlangit/blastn-jupyter-docker`
 4) Connect to the example Jupyter notebook in your browser using the link generated
 5) Navigate and run the jupyter notebook located in /work/

 B. To build a Dockerfile from image source files (on GitHub):
 1) Clone the source repo
 2) Build the image by running `docker build -t blastn-jupyter-docker .` 
 3) Wait for the build to complete (takes ~15 minutes)
 4) Start an instance of the image by running `docker run -p 8888:8888 blastn-jupyter-docker`
 5) Connect to the example Jupyter notebook in your browser using the link generated
 6) Navigate and run the jupyter notebook located in /work/
 
 TIP: If your browser returns a 'connection_refused' error, when you attempt to connect using   
 the generate URL (such as `http://0.0.0.0:8888/?token=87ea7335fd396f88fa945aa7dd871fe9de49767a3f626875`,  
 then determine the mapped IP (such as 192.168.10.100), connect using that IP:port (such as `http://192.168.10.100:8888`    
 and then copy the token value from the generated URL and paste it into the token text box in the browser.

[![blastn-jupyter-notebook](/images/blast-jupyter-notebook.png)]()
