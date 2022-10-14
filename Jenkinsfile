pipeline
{
	agent{
		label{
			label 'built-in'
		}
	}
	
	stages{
		stage('stage-1'){
		
			agent{
				label{
					label '172.31.34.186'
					customWorkspace '/mnt/project-1/'
				}
			}
			
			steps{
				sh "sudo yum install git -y"
				sh "sudo yum install httpd -y"
				sh "sudo service httpd start"
				sh "sudo chmod -R 777 /var/www/"
				sh "sudo cp /mnt/project-1/index.html /var/www/html/index.html"
				
			}
		}
	}
}
