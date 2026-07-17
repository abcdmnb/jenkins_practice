pipeline{
 agent any
 stages{
  stage ("Build_stage"){
   steps{
    echo "building"
   }
   }
  stage ("test_stage"){
   steps{
   echo "testing..."
   }
   }
  stage ("deploy_stage"){
   steps{
    echo "deploying..."
  }
  }
  stage ("running_py_code"){
   steps{
    bat '"C:\\Users\\HP\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" test.py'
   }
  }
}
 post{
  always{
      mail to: "bhagya17211@gmail.com",
        subject: "Job: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
        body: "job runned successfully.\n${env.BUILD_URL}"
  }
  success{
   mail to: "bhagya17211@gmail.com",
        subject: "SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
        body: "Build completed successfully.\n${env.BUILD_URL}"
  }
  failure{
   mail to: "bhagya17211@gmail.com",
        subject: "FAILED: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
        body: "Build failed.\n${env.BUILD_URL}"
  }
 }
}
