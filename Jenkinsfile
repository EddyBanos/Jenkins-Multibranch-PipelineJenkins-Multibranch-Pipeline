pipeline {
	agent any
		stages {
			stage('First') {
				script {
					env.VARIABLE="value"
					}
				steps {
					sh '''
						echo ${EXECUTE}
					'''
				}
			}

			stage('Second') {
				steps {
					sh '''
						echo "Updating Stage"
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

