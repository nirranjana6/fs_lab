pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                // Clone the repository from GitHub
                bat 'git clone https://github.com/nirranjana6/fs_lab.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Install dependencies from the requirements.txt
                bat 'pip install -r fs_lab/requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                // Run pytest tests
                bat 'pytest fs_lab/tests'
            }
        }
    }
}
