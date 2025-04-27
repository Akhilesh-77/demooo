This is a demo file




























FROM openjdk:11
WORKDIR /Users/AKHILESH/docker
COPY . /Users/AKHILESH/docker
RUN javac Test.java
CMD [ "java", "Test"]

FROM python:3
WORKDIR /Users/AKHILESH/docker
COPY . /Users/AKHILESH/docker

CMD [ "python","-u", "hello.py"]

docker build -t "example"
docker build example
