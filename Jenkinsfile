node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm

   // Get the maven tool.
   // ** NOTE: This 'M3' maven tool must be configured
   // **       in the global configuration.
   //def mvnHome = tool 'M3'
   def mvnHome= "D:\\apache-maven-3.1.1"
   env.JAVA_HOME = tool 'Java 1.7.0_101'

   // Mark the code build 'stage'....
   stage 'Build'
   input 'Ready to go?'
   // Run the maven build
   bat "${mvnHome}\\bin\\mvn verify"
}
