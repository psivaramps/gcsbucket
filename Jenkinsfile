pipeline {
 agent any 

	
	stages {
		stage ('Checkout') {
			steps {
			git branch : 'master' , url: 'https://github.com/ishaqmdgcp/nexus.git'

			}
		}

		
		stage ('Creating a Bucket') {
			steps {
			sh 'gsutil mb -p sivaramgcp -c nearline -l us-eas1 -b on g://pipelinebucket'
			
			}
		}

		stage ('list the buckets') {
			steps {
			sh 'gsutil ls'
			}
		}
		stage ('To Display the size of bucket') {
			steps {
			sh 'gsutil du -s gs://pipelinebucket'
			}
		}
		
		stage ('To Display Bucket Metadata') {
			steps {
			sh 'gsutil ls -L -b gs://pipelinebucket'
			}
		}
		stage ('To List the Objects in Bucket') {
			steps {
			sh 'gsutil ls -r gs://pipelinebucket'
			}
		}
		
		stage ('To List the Objects in Bucket') {
			steps {
			sh 'gsutil cp  gs://siva-simple-bucket/dsktp.jpg  gs://pipelinebucket/dsktp1.jp'
			}
		}
	
	}
	}
