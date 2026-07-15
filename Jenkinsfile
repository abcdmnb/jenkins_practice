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
  success{
   echo "job is successful"
  }
  failure{
   echo "fob failed"
  }
 }
}
