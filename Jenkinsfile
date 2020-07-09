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
    sh "ls"
    sh "echo $PWD"
  }
}