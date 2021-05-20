pipeline {
	agent any
	environment {
        	Result = "True"
    	}
		stages {
			stage('First') {
				steps {
					echo "Result = ${env.Result}"
					
				}
			}
			stage('Second') {
				steps {
					script {
						echo "${env.Result}"
						echo "Updating Second Stage"
					}
					when{
						beforeAgent true
					}
					steps{
						script {
						echo "${env.Result}"
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

