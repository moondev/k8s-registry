node {
    
    checkout scm

    stage "Install Registry"
        sh "kubectl apply -f registry.yml"
        sh "kubectl rollout status deployment/registry"

    // stage "run registry proxy"
    //     sh "docker stop socat-registry"
    //     sh "docker rm socat-registry"
    //     sh "docker run -d -e REGIP=192.168.99.100 --name socat-registry -p 30400:5000 chadmoon/socat:latest bash -c 'socat TCP4-LISTEN:5000,fork,reuseaddr TCP4:192.168.99.100:30400'"
    //     sh "sleep 5"
}