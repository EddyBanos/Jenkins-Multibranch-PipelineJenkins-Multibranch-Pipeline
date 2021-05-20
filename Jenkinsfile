pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					sh '''
						env.EXECUTE="true"
					'''
				}
			}

			stage('Second') {
				steps {
					sh '''
						echo "Updating Stage"
					'''
					when {
                				branch 'master'
						EXECUTION: "true"
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

