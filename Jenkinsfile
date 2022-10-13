pipeline{

		agent {
				label {
					label "built-in"
					customWorkspace "/mnt/project-1/"
				}
		}
		
		stages{
			stage('deploy-index'){
			
				steps {
					sh "cp -r index.html /var/www/html/index.html"
					sh "chmod -R 777 /var/www/html/index.html"
				}
		}
	}
}
