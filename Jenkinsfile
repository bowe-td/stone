def label = "develop-bowe-b2b"
def container_name = "stone-planilhas"

node(label) {
  stage("Clone repository") {
    checkout scm
  }

  stage("remove old containers") {
    sh "docker rm -f ${container_name} || true"
  }

  stage("UP stone repository") {
    sh 'pwd'
    sh "docker run -dit --name ${container_name} -p 1000:80 -v \$(pwd):/usr/local/apache2/htdocs httpd:2.4"
  }
}