node('docker') {
    docker.image('darinpope/ant:latest').inside {
        sh '''
            java -version
            ant -version
            mvn -version
            ant -Dsrc=src -Dbuild=build -Ddist=dist clean
        '''
    }
}
