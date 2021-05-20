pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					sh '''
						env.EXECUTE='true'
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

