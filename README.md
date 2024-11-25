# django-todo
A simple todo app built with django

![todo App](https://raw.githubusercontent.com/shreys7/django-todo/develop/staticfiles/todoApp.png)
### Setup

Create a EC2 instance of ubuntu of instance type of t2.micro in AWS

Edit inbound rules:
    Add Security Rules:
      Create a Custom TCP of Port Range 8000 with source of Anywhere IPv4.

Now Connect the instance.
Update the instance
```bash
  sudo apt update
```

To get this repository, run the following command inside your git enabled terminal
```bash
git clone https://github.com/0mchoudhary/Django_todo_Docker.git
```

Change the permission of directory
```bash
chmod 777 Django_todo_Docker
```

Install Docker in instance
```bash
  sudo apt install docker.io -y
```

Change the directory
```bash
  cd Django_todo_Docker
```

Build a docker image
```bash
  sudo docker build  . -t django:v1
```

Run a docker image
```bash
sudo docker run -d -p 8000:8000 django:v1
```

Once the server is hosted, head over to http:$(YOUR_IP_ADDRESS)/todos for the App.

Cheers and Happy Coding :)
