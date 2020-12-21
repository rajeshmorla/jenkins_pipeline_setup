pipeline {
    agent none
    stages {
        stage('Non-Sequential Stage') {
            agent any
            steps {
                echo "On Non-Sequential Stage"
            }
        }
        stage('Sequential') {
            agent any
            environment {
                FOR_SEQUENTIAL = "some-value"
            }
            stages {
                stage('In Sequential 1') {
                    steps {
                        echo "In Sequential 1"
                    }
                }
                stage('In Sequential 2') {
                    steps {
                        echo "In Sequential 2"
                    }
                }
                stage('Parallel In Sequential') {
                     stages {
                        stage('In Sequential 1') {
                            steps {
                                echo "In Sequential 1"
                            }
                        }
                        stage('In Sequential 2') {
                            steps {
                                echo "In Sequential 2"
                            }
                        }
                     }
                    parallel {
                        stage('In Parallel 1') {
                            steps {
                                echo "In Parallel 1"
                            }
                        }
                        
                    }
                }
            }
        }
    }
}
