node {
    stage('Clone Repository') {
        echo "Build number ${BUILD_NUMBER} in ${WORKSPACE}"
        checkout scm
    }

    stage('Dependency Check') {
        dependencyCheckAnalyzer datadir: "${JENKINS_HOME}", hintsFile: '', includeCsvReports: false, includeHtmlReports: false, includeJsonReports: false, includeVulnReports: false, isAutoupdateDisabled: true, outdir: '', scanpath: '', skipOnScmChange: false, skipOnUpstreamChange: false, suppressionFile: '', zipExtensions: ''
        dependencyCheckPublisher canComputeNew: false, defaultEncoding: '', failedTotalAll: '6', failedTotalHigh: '1', failedTotalLow: '3', failedTotalNormal: '2', healthy: '0', pattern: '', thresholdLimit: 'normal', unHealthy: '10', unstableTotalAll: '12', unstableTotalHigh: '2', unstableTotalLow: '6', unstableTotalNormal: '4'
    }

    stage('Deploying to Dev') {
        echo 'Deployed to dev'
    }
}