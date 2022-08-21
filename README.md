# docker-basic
for workshop

## docker?
docker is ....

## Arsitektur Docker
### Client
Docker Client adalah seluruh Command Docker yang kita jalankan di layar terminal. Command ini nantinya akan masuk ke Docker Host untuk kemudian dieksekusi sesuai fungsinya.
### Host and Daemon
Docker Host merupakan mesin (komputer,server) yang terinstall Docker didalamnya. Didalam Docker Host terdapat Docker Daemon yang merupakan otak utama untuk memproses setiap permintaan (command) dari Docker Client. Docker Daemon yang akan mengatur bahwa misalnya command “docker image push” akan melakukan upload sebuah image ke Registry, atau command “docker container ls” akan menampilkan seluruh daftar container yang sedang berjalan di sistem.
### Image
Image adalah aplikasi yang ingin kita jalankan. Image berisi binary, library dan source code dari aplikasi yang ingin kita jalankan tersebut
### Container
Container adalah instance yang menjalankan image dalam bentuk sebuah proses
### Registry
Registry merupakan tempat penyimpanan Image yang dapat berupa penyimpanan Publik maupun lokal.


## Penggunaan Secara Umum
### Create dockerfile
A Dockerfile is a text document that contains all the commands a user could call on the command line to assemble an image
### Create docker Image
  docker build -t <nama image> .
  docker build -t <registry>/<nama image>:<version> .
  ```
  docker build -t dedewahyuh/testimage:1.0 .
  ```  
### Push/Pull docker image to docker Registry
  ```
  docker push dedewahyuh/testimage:1.0
  ```
### Running docker Container
  docker run [OPTIONS] IMAGE [COMMAND] [ARG...]
  
  ```
  docker run dedewahyuh/testimage:1.0
  
  docker run --name masa471 --volume /home/ubuntu/deploy/config/app:/var/dbo -e REBEL_CLI_CONFIG_PATH=/var/dbo/file.json  dedewahyuh/masa471 /go/bin/dbocore_migration -type=471_migrate_activities_redis_data -limit=800 -start=0 -end=2
  ```
### Docker Compose
  Docker Compose is a tool that was developed to help define and share multi-container applications. With Compose, we can create a YAML file to define the services and with a single command, can spin everything up or tear it all down.

  ```
  docker compose up -d
  docker compose down
  ```
  
  
  ##source
  [Docker](https://docs.docker.com/reference/)
  [Docker Compose](https://docs.docker.com/get-started/08_using_compose/#:~:text=Docker%20Compose%20is%20a%20tool,or%20tear%20it%20all%20down.)
  


