pipeline {
    agent any
    stages(){
            stage('github-clone') {
                steps {
                    git branch: 'main', credentialsId: 'github-token', url: 'https://github.com/fftl/study_jenkins_branch.git'
                }
                steps {
                    script {
                        // Docker ps 명령어 실행
                        def dockerPsOutput = sh(script: 'docker ps', returnStdout: true).trim()
                        
                        // 출력 결과를 echo로 처리
                        echo "Docker ps output: ${dockerPsOutput}"
                    }
                }
            }
        }
    }
}
