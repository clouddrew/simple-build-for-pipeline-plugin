 node ('faux'){
  stage ('Build and Test') {

simpleBuild {
 
    env = [
        FOO : 42,
        BAR : "YASS"
    ]
    
 

    before_script = "echo before"
    script = 'echo after $FOO'
    
    notifications = [
        email : "deasley@cloudbees.com"    
    ]
    
    
}
}}
