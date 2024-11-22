pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/nirranjana6/fs_lab.git'
            }
        }
        stage('Install Dependencies') {
            steps {
                // Ensure that the correct Python environment is being used
                bat 'python -m pip install --upgrade pip'
                bat 'python -m pip install -r fs_lab/requirements.txt'
                bat 'python -m pip install pytest' // Ensure pytest is installed
            }
        }
        stage('Run Tests') {
            steps {
                // Run pytest using the correct Python environment
                bat 'python -m pytest fs_lab/tests'
            }
        }
    }
}
