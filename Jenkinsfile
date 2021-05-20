pipeline {
	agent any
	environment {
        	VARIABLE = 'Test'
    	}
		stages {
			stage('First') {
				steps {
					agent {
						Test="true"
					}
				}
			}
			stage('Second') {
				steps {
					script {
						echo "${EXECUTE}"
						echo "Updating Second Stage"
					}
					when{
						beforeAgent true
					}
					steps{
						script {
						echo "${EXECUTE}"
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

