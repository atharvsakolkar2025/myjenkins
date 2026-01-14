pipeline {
    agent any
stages {
    // NEW STAGE: Pull the source code first!
    stage('pull SCM') {
        steps {
            echo "Pulling code from GitHub..."
            // This 'git' step is provided by the Git Plugin
            git url: 'https://github.com/mayur-z/3t-aws.git', branch: 'main'
        }
    }

    stage('my Build') {
        steps {
            // Let's run a real command now that we have the code
            // 'sh' is a step for running a shell command on Linux/macOS
            sh 'ls -la'
            sh 'pwd'
            echo "In a real build, we'd run 'mvn clean install'."
        }
    }

    stage('cbz Test') {
        steps {
            sh 'hostnamectl'
            echo "Running tests..."
        }
    }

    stage('Deploy to productionn') {
        steps {
            echo "Deploying to staging..."
        }
    }
}
}
