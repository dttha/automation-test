pipeline {
    agent any
    stages {
        stage('Pull Code') {
            when {
                expression { return params.pullCode }
            }
            steps {
                git(url: "https://github.com/dttha/automation-test.git", branch: "main")
            }
        }
        stage('Build') {
            steps {
                echo "Build step chạy, pullCode = ${params.pullCode}"
            }
        }
    }
}
