pipeline {
    agent any 

    stages {
        stage('Build') {
            steps {
                echo '🚀 Starting the build process...'
                sh 'docker build -t my-app .' // Build the Docker image
                echo '✔️ Build completed successfully!'
            }
        }
        stage('Test') {
            steps {
                echo '🧪 Running tests...'
                sh 'docker run --rm my-app:latest tests' // Run tests inside a Docker container
                echo '✅ All tests passed!'
                echo '🔍 Reviewing test results...'
            }
        }
        stage('Deploy') {
            steps {
                echo '🚢 Preparing for deployment...'
                sh 'docker push my-app:latest' // Push the Docker image to a registry
                echo '🌐 Deployment in progress...'
                // Add your deployment commands here (e.g., deploying to a server)
                echo '🎉 Deployment finished successfully!'
            }
        }
    }
}
