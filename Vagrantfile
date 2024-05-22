
Vagrant.configure("2") do |config|
  
  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname = "Examen-David-Fraga"
  config.vm.network "private_network", ip:"192.168.56.74"

  config.vm.provision "shell", inline: <<-SHELL

  
   echo "-- Insertar datos de ejemplo en la tabla 'libros'" > /home/vagrant/datos_pacientes.sql
   echo "INSERT INTO gestion_clinica_veterinaria.pacientes (idPaciente, nombre, especie, raza, edad, dueño) VALUES" >> /home/vagrant/datos_pacientes.sql
   echo "(1, 'Juan', 'pitbull', 'perro', 3, 'Mario')," >> /home/vagrant/datos_pacientes.sql
   echo "(2, 'Cheto', 'pastor aleman', 'perro', 5, 'Laura')," >> /home/vagrant/datos_pacientes.sql
   echo "(3, 'Lola', 'chihuahua', 'perro', 2, 'Pedro');" >> /home/vagrant/datos_pacientes.sql

  SHELL


end
