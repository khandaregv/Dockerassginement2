
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

					sh "sudo docker run -itd --name Q2 httpd"

					sh "sudo cp /mnt/slave2/index.html /Git"

					sh "sudo docker cp /Git/index.html Q2:/usr/local/apache2/htdocs/"

					}

				     }

			}

	}
