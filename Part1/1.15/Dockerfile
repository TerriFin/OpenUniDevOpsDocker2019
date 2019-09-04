FROM python:3

WORKDIR /forum
COPY Keskustelufoorumi .

RUN pip install --no-cache-dir -r requirements.txt

EXPOSE 5000

CMD ["python", "./run.py"]
