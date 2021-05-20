pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					script {
						env.EXECUTE="true"
					}
					agent {
						EXECUTE
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

