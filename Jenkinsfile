def label = "develop-bowe-b2b"
def container_name = "stone-planilhas"

node(label) {
  stage("Clone repository") {
    checkout scm
  }

  stage("UP stone repository") {
    sh "docker run -dit --name stone-temp -p 1000:80 -v "$PWD":/usr/local/apache2/htdocs httpd:2.4"
  }
}