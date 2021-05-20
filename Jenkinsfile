pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					script {
						env.VARIABLE="value"
					}
				}
			}
			stage('Second') {
				steps {
					script {
						echo "${VARIABLE}"
						echo "Updating Second Stage"
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

