# VERSIÓN PYTHON
FROM python:3.7.7-slim

WORKDIR .

COPY editarTituloHTML.py .

RUN apt-get update -y

RUN apt-get install git -y

RUN git clone https://github.com/CDPS-ETSIT/practica_creativa2.git
RUN pip3 install -r practica_creativa2/bookinfo/src/productpage/requirements.txt

EXPOSE 9080

ENV GROUP_NUMBER 11

CMD ["python3", "editarTituloHTML.py"]

#ENTRYPOINT ["python3", "practica_creativa2/bookinfo/src/productpage/productpage_monolith.py", "9080"]



# En el terminal, deberemos ejecutar los siguientes comandos Docker:
# sudo docker build -t grupo11/product-page .
# sudo docker run -e GROUP_NAME="GRUPO 11" -dp 9080:9080 --name GRUPO11-BOOKSTORE grupo11/product-page
