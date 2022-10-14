pipeline
{
	agent{
		label{
			label 'built-in'
			customWorkspace "/mnt/pipe/"
		}
	}
	
	stages{
		stage('stage-1'){
		
			agent{
				label{
					label '172.31.34.186'
					customWorkspace '/mnt/project/'
				}
			}
			
			steps{
				
				sh "sudo yum install httpd -y"
				sh "sudo service httpd start"
				sh "sudo chmod -R 777 /var/www/"
				sh "sudo git clone https://github.com/bhushan3478/git-assignment.git -b master"
				sh "sudo cp /mnt/project/git-assignment/index.html /var/www/html/index.html"
				
			}
		}
	}
}
