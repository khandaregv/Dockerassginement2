
pipeline {

	agent {
label {
		label "slave2"
		customWorkspace "/mnt/slave2/" 
	      }
	}
		stages {

			stage ("One"){

				steps {

					sh "sudo docker ps -aq | xargs -r sudo docker rm -f"

					sh "sudo docker run -itdp 80:80 --name Q2 httpd"

					sh "sudo cp /mnt/slave2/index.html /Git"

					sh "sudo chmod -R 777 /Git/index.html"

					sh "sudo docker cp /Git/index.html Q2:/usr/local/apache2/htdocs/"

					}

				     }

			}

	}
