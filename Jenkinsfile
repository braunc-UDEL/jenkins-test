@Library('piper-lib-os') _
pipeline {
  agent any
environment {
     PATH = "/bin:/usr/bin:usr/local/bin"
}
node() {
    stage('prepare') {
        checkout scm
        setupCommonPipelineEnvironment script:this
    }
    stage('build') {
        mtaBuild script: this
    }
}
}
