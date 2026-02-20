
pipeline {

	agent {
		label "slave1"
		customWorkspace "/mnt/slave1" 
	      }

		stages {

			stage ("One"){

				steps {

					sh "sudo docker ps -aq | xargs -r sudo docker rm -f"

					sh "sudo docker run -itd --name Q1 httpd"

					sh "sudo cp /mnt/slave1/index.html /Git"

					sh "sudo docker cp /Git/index.html Q1:/usr/local/apache2/htdocs/"

					}

				     }

			}

	}
