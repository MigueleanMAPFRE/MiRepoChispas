pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hola TRON, ¿como tu TaaS?'
            }
        }
 
 
         stage ('Ejemplo shell script') {
            agent { label 'docker-agent' }
            steps {
                sh """
                   hostname
                   ls -la
                   pwd
		   sh ejecuta.sh
                """
            }
        }
	stage ('Test') {
		when {
			branch 'PR-*'
		}
		step {
			echo 'lo hace'
		}
	}

    }
    }

