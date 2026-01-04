FROM python:3.10

WORKDIR /app
COPY requirements.txt requirements.txt
RUN pip3 install --no-cache-dir -r requirements.txt

COPY . .

CMD ["python", "demo.py"]

#ibmcloud ce project get --name "Code Engine - sn-labs-jinkaslearni"
#ibmcloud ce build create --name build-local-dockerfile1  --build-type local --size large   --image us.icr.io/${SN_ICR_NAMESPACE}/myapp1  --registry-secret icr-secret
#ibmcloud ce buildrun submit --name buildrun-local-dockerfile1 --build build-local-dockerfile1 --source .
#ibmcloud ce buildrun get -n buildrun-local-dockerfile1
#ibmcloud ce buildrun logs -f -n buildrun-local-dockerfile1
#ibmcloud ce application create --name demo1  --image us.icr.io/${SN_ICR_NAMESPACE}/myapp1  --registry-secret icr-secret --es 2G   --port 7860 --minscale 1
#ibmcloud ce application get -n demo1
#ibmcloud ce application events -n demo1
#ibmcloud ce application logs -f -n demo1
#ibmcloud ce app get --name demo1 --output url