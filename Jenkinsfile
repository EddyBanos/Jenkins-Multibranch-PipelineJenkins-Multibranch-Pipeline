pipeline {
	agent any
	environment {
        	RESULTADO = "True"
    	}
		stages {
			stage('First') {
				steps {
					echo "Result = ${env.RESULTADO}"
					
				}
			}
			stage('Second') {
				steps {
					script {
						echo "${env.RESULTADO}"
						echo "Updating Second Stage"
					}
					when{
						beforeAgent true
					}
					steps{
						script {
						echo "${env.RESULTADO}"
						echo "Updating Second Stage"
					}
					}
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

