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


##Penggunaan Secara Umum
### Create dockerfile
### Create docker Image
### Push/Pull docker image to docker Registry
### Running docker Container
### Docker Compose


