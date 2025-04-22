pipeline {
    agent any

    stages {
        stage('Second Task: Create Files and Show Contents') {
            steps {
                script {
                    sh 'mkdir -p loop_folder'

                    for (int i = 1; i <= 5; i++) {
                        def filename = "loop_folder/file${i}.txt"
                        sh "echo 'Это файл номер ${i}' > ${filename}"
                    }

                    sh 'cat loop_folder/*'
                }
            }
        }

        stage('Third Task: Disk and Memory Info') {
            steps {
                script {
                    sh 'df -h'

                    sh 'free -h'

                    sh 'who'
                }
            }
        }

        stage('Fourth Task: Create and Delete File') {
            steps {
                script {
                    sh 'mkdir -p temp_folder'

                    sh 'touch temp_folder/delete_me.txt'

                    sh 'ls temp_folder'

                    sh 'rm -rf temp_folder/delete_me.txt'

                    sh 'ls temp_folder'
                }
            }
        }

        stage('Fifth Task: Show Environment Variables') {
            steps {
                script {
                    sh 'printenv'

                    sh 'whoami'

                    sh 'pwd'
                }
            }
        }
	stage('cheack jenkins file') {
		steps {
			script {

		sh 'cat Jenkinsfile'
			}
		}
	}
    }
}
