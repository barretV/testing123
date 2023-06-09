pipeline {
    agent {
        node {
            label 'linux' // linux
        }
    }
    stages {
        stage('Get posts') {
            steps {
                script {
                    def response = sh(script: 'curl https://jsonplaceholder.typicode.com/posts', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Get comments') {
            steps {
                script {
                    def response = sh(script: 'curl https://jsonplaceholder.typicode.com/posts/1/comments', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Get albums') {
            steps {
                script {
                    def response = sh(script: 'curl https://jsonplaceholder.typicode.com/albums', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Get todos') {
            steps {
                script {
                    def response = sh(script: 'curl https://jsonplaceholder.typicode.com/todos', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Create post') {
            steps {
                script {
                    def response = sh(script: 'curl -X POST -H "Content-Type: application/json" -d \'{"title": "New post", "body": "This is a new post", "userId": 1}\' https://jsonplaceholder.typicode.com/posts', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Update post') {
            steps {
                script {
                    def response = sh(script: 'curl -X PUT -H "Content-Type: application/json" -d \'{"title": "Updated post", "body": "This post has been updated", "userId": 1}\' https://jsonplaceholder.typicode.com/posts/1', returnStdout: true).trim()
                    println(response)
                }
            }
        }
        stage('Delete post') {
            steps {
                script {
                    def response = sh(script: 'curl -X DELETE https://jsonplaceholder.typicode.com/posts/1', returnStdout: true).trim()
                    println(response)
                }
            }
        }
    }
}