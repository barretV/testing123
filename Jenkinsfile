pipeline {
    agent {
        node {
            label 'linux' // linux
        }
    }
    stages {
        stage('Get posts') {
            steps {
                sh 'curl https://jsonplaceholder.typicode.com/posts'
            }
        }
        stage('Get comments') {
            steps {
                sh 'curl https://jsonplaceholder.typicode.com/posts/1/comments'
            }
        }
        stage('Get albums') {
            steps {
                sh 'curl https://jsonplaceholder.typicode.com/albums'
            }
        }
        stage('Get todos') {
            steps {
                sh 'curl https://jsonplaceholder.typicode.com/todos'
            }
        }
        stage('Create post') {
            steps {
                sh 'curl -X POST -H "Content-Type: application/json" -d \'{"title": "New post", "body": "This is a new post", "userId": 1}\' https://jsonplaceholder.typicode.com/posts'
            }
        }
        stage('Update post') {
            steps {
                sh 'curl -X PUT -H "Content-Type: application/json" -d \'{"title": "Updated post", "body": "This post has been updated", "userId": 1}\' https://jsonplaceholder.typicode.com/posts/1'
            }
        }
        stage('Delete post') {
            steps {
                sh 'curl -X DELETE https://jsonplaceholder.typicode.com/posts/1'
            }
        }
    }
}