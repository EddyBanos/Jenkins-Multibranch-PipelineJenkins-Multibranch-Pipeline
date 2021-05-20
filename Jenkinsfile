pipeline {
	agent any
	environment {
        	Result = 'null'
    	}
		stages {
			stage('First') {
				steps {
					script {
						env.Result="true"
					}
					agent{
						label "Flag"
					}
				}
			}
			stage('Second') {
				steps {
					script {
						echo "${Result}"
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

