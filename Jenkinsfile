pipeline {
  agent any
  stages {
    stage('Create PR') {
      steps {
        echo 'Create PR'
      }
    }
    stage('Write and define policyfile.rb') {
      parallel {
        stage('Policy File') {
          steps {
            echo 'InSpec Profile'
          }
        }
        stage('Source/s') {
          steps {
            echo 'Artifactory or GitHub or Supermarket'
          }
        }
        stage('Runlist') {
          steps {
            echo 'test'
          }
        }
        stage('Attrbutes') {
          steps {
            echo 'Compliance profile version in Audit Cookbook'
          }
        }
        stage('Cookbook Versions') {
          steps {
            echo 'Version pinning'
          }
        }
        stage('include_policy') {
          steps {
            echo 'test'
          }
        }
      }
    }
    stage('Lint/Syntax Check') {
      parallel {
        stage('Syntax Check') {
          steps {
            echo 'test'
          }
        }
        stage('Rubocop') {
          steps {
            echo 'test'
          }
        }
      }
    }
    stage('Kitchen Integration Test') {
      parallel {
        stage('OS Tests') {
          steps {
            echo 'test'
          }
        }
        stage('Middleware Test') {
          steps {
            echo 'test'
          }
        }
      }
    }
    stage('Code Review') {
      steps {
        echo 'Test'
      }
    }
    stage('Produce policyfile archive as tarball and lockfile') {
      parallel {
        stage('loads all of the policyfile lock files in a directory into the Chef server') {
          steps {
            echo 'test'
          }
        }
        stage('chef export base.rb . -a # generates base-VERSION.tgz') {
          steps {
            echo 'test'
          }
        }
        stage('export base.rb') {
          steps {
            echo 'test'
          }
        }
        stage('chef push-archive POLICY_GROUP base-VERSION.tgz -c config_file --debug') {
          steps {
            echo 'test'
          }
        }
      }
    }
    stage('Publish Archove/Lock') {
      steps {
        echo 'Publish to Artifactory, or Git or Habichef or ChefServer'
      }
    }
    stage('Commit to Master') {
      steps {
        echo 'test'
      }
    }
  }
}
