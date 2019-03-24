FROM yunabe/lgo:latest

WORKDIR /examples

User root

RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -

RUN apt-get update && apt-get install -y nodejs

RUN jupyter labextension install jupyterlab_vim

User gopher

# To use JupyterLab, replace "notebook" with "lab".
CMD ["jupyter", "lab", "--ip=0.0.0.0"]
