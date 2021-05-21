pipeline {
	agent any
	environment {
        	RESULTADO = "True"
    	}
		stages {
			stage('First') {
				steps {
					echo "Result = ${env.RESULTADO}"
					script {
						env.RESULTADO = "True"
					}
				}
			}
			
			stage('Second') {
				when {
					expression { RESULTADO == "True"}
				}
				steps {
					sh '''
						echo "Step -Two"
						echo "Updating Second Stage"
					'''
					script {
						echo "${RESULTADO}"
					}
				}

			} 
			stage('Third') {
				when {
					expression { EXECUTE == "False"}
				}
				steps {
					sh '''
						echo "Third Step"
					'''
				}
			}
		}
}

