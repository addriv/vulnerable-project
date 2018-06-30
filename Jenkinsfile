node {
    stage('Clone Repository') {
        echo "Build number ${BUILD_NUMBER} in ${WORKSPACE}"
        checkout scm
    }

    stage('Dependency Check') {
        dependencyCheckAnalyzer datadir: '', hintsFile: '', includeCsvReports: false, includeHtmlReports: false, includeJsonReports: false, includeVulnReports: false, isAutoupdateDisabled: false, outdir: '', scanpath: '', skipOnScmChange: false, skipOnUpstreamChange: false, suppressionFile: '', zipExtensions: ''
        dependencyCheckPublisher canComputeNew: false, defaultEncoding: '', healthy: '', pattern: '', unHealthy: '', unstableTotalHigh: '5', unstableTotalLow: '10', unstableTotalNormal: '7'
    }
}