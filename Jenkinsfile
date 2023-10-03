node {
   def mvnHome
  stage('Prepare') {
      git url: 'https://github.com/sindhujareddy09/abc.git', branch: 'jenkin'
      mvnHome = tool 'maven'
   }
    stage ('Code Quality') {
      sh "'${mvnHome}/bin/mvn' sonar:sonar"
  }

  stage ('Clean') {
      sh "'${mvnHome}/bin/mvn'  clean"
  }
  stage ('Validate') {
      sh "'${mvnHome}/bin/mvn'  validate"
  }
  stage ('Compile') {
      sh "'${mvnHome}/bin/mvn'  compile"
  }
  stage ('Test') {
      sh "'${mvnHome}/bin/mvn'  test"
  }
  stage ('Package') {
      sh "'${mvnHome}/bin/mvn'  package"
  }
  stage ('Verify') {
      sh "'${mvnHome}/bin/mvn'  verify"
  }
  stage ('Install') {
      sh "'${mvnHome}/bin/mvn' install"
  }
}
