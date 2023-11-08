node 
{
    stage ("clone")
    {
        git branch: 'main', url: 'https://github.com/Sreeni15/sample-html-app.git'
        sh "ls"
    }
    stage ("docker image")
    {
        sh "docker build -t csnivas15/html ."
        
    }
    stage ("docker hub")
    {
        sh "docker login -u csnivas15 -p admin@15"
        sh "docker push csnivas15/html"
    }
    stage("docker container")
    {
     sh "docker rm -f html"
     sh "docker run -d --name html -p 86:80 csnivas15/html"
    }
    
}
