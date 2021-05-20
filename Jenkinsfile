pipeline {
	agent any
	environment {
        	Result = "null"
    	}
		stages {
			stage('First') {
				steps {
					echo "Result = ${env.Result}"
					agent{
						label "Flag"
					}
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
						echo "${.envResult}"
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

