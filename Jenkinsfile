pipeline {
    agent any 
    stages {
        stage(Build) { 
            steps {
                sh python3 -m py_compile sources/add2vals.py
                sh python3 -m py_compile sources/calc.py 
                stash(name: compiled-results, includes: sources/*.py*) 
            }
        }
    }
}
