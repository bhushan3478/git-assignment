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
					customWorkspace '/mnt/project/git-1'
				}
			}
			
			steps{
				
				sh "sudo yum install httpd -y"
				sh "sudo service httpd start"
				sh "sudo chmod -R 777 /var/www/"
				sh "sudo cp /mnt/project/index.html /var/www/html/index.html"
				
			}
		}
	}
}
