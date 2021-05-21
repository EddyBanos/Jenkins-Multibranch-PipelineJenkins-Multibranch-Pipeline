pipeline {
	agent any
	environment {
        	RESULTADO = "True"
    	}
		stages {
			stage('First') {
				steps {
					echo "Step one "
				}
			}
			
			stage('Second') {
				steps {
					sh '''
						echo "Step -Two"
						echo "Updating Second Stage"
					'''
				}

			} 
			stage('Third') {
				steps {
					sh '''
						echo "Third Step"
					'''
				}
			}
		}
}

