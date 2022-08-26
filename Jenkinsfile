pipeline {
    agent {
        any { image 'node:latest' }
    }
    stages {
        stage('check') {
            steps {
                sh 'pwd'
                sh 'docker info'
                sh 'docker container ls'
                sh 'docker images'
            }
        }
        // stage('server') {
        //     when {
        //         expression { params.REFRESH_CONTAINER == 'server' || params.REFRESH_CONTAINER == 'all' }
        //     }
        //     steps {
        //         script {
        //             sh 'docker build ./server -t server'
        //
        //             try {
        //                 sh "docker stop server"
        //                 sh "docker rm server"
        //             }
        //             catch (exc) {
        //                 sh "echo 'continue'"
        //             }
        //
        //             sh "docker run -d \
        //             --restart always \
        //             -e MONGOHOST1=${params.MONGOHOST1} \
        //             -e MONGOHOST2=${params.MONGOHOST2} \
        //             -e MONGOHOST3=${params.MONGOHOST3} \
        //             -e SQL_HOST=${params.SQL_HOST} \
        //             -e SQL_USERNAME=${params.SQL_USERNAME} \
        //             -e SQL_PASSWORD=${params.SQL_PASSWORD} \
        //             -e SQL_DATABASE=${params.SQL_DATABASE} \
        //             -e ACCESS_TOKEN_SECRET=${params.ACCESS_TOKEN_SECRET} \
        //             -e REFRESH_TOKEN_SECRET=${params.REFRESH_TOKEN_SECRET} \
        //             -e NODE_MODULES_INIT=${params.NODE_MODULES_INIT} \
        //             -e SESSION_TIME=${params.SESSION_TIME} \
        //             --name server -p 6000:5000 server"
        //         }
        //     }
        // }
        // stage('cleanup') {
        //   steps {
        //     script {
        //       try {
        //         sh 'docker rmi $(docker images -q -f dangling=true)'
        //       } catch (exc) {
        //         sh 'docker images'
        //       }
        //     }
        //   }
        // }
    }
}
