node {
  stage("build") {
    //checkout scm
    def aa = readJSON file: "/var/jenkins_home/workspace/new3/common_packages_for_developers/json/1.json"
    println(aa)

    def postmanGet = new URL('http://10.10.0.44:8888/druid/indexer/v1/task')
    def connectionObject = (HttpURLConnection) postmanGet.openConnection()
    connectionObject.setRequestProperty("Content-Type", "application/json")
    connectionObject.requestMethod = 'POST'
    connectionObject.setDoOutput(true)
    
    // String jsonInputString1 = '{"name": "Upendra", "job": "Programmer"}'
    //String jsonInputString =  ='{"type":"index_parallel","resource":{"availabilityGroup":"index_parallel_wikipedia22_2021-04-28T08:20:54.447Z","requiredCapacity":1},"spec":{"dataSchema":{"dataSource":"sheet33","parser":{"type":"string","parseSpec":{"format":"json","timestampSpec":{"column":"timestamp","format":"iso"},"dimensionsSpec":{"dimensions":["channel","cityName","comment","countryIsoCode","countryName","diffUrl","flags","isAnonymous","isMinor","isNew","isRobot","isUnpatrolled","namespace","page","regionIsoCode","regionName","user"]}}},"metricsSpec":[{"type":"count","name":"count"},{"type":"longSum","name":"sum_added","fieldName":"added","expression":null},{"type":"longSum","name":"sum_commentLength","fieldName":"commentLength","expression":null},{"type":"longSum","name":"sum_deleted","fieldName":"deleted","expression":null},{"type":"longSum","name":"sum_delta","fieldName":"delta","expression":null},{"type":"longSum","name":"sum_deltaBucket","fieldName":"deltaBucket","expression":null},{"type":"longSum","name":"sum_metroCode","fieldName":"metroCode","expression":null}],"granularitySpec":{"type":"uniform","segmentGranularity":"DAY","queryGranularity":"HOUR","rollup":true,"intervals":null},"transformSpec":{"filter":null,"transforms":[]}},"ioConfig":{"type":"index_parallel","firehose":{"type":"http","uris":["https://druid.apache.org/data/wikipedia.json.gz"],"maxCacheCapacityBytes":1073741824,"maxFetchCapacityBytes":1073741824,"prefetchTriggerBytes":536870912,"fetchTimeout":60000,"maxFetchRetry":3,"httpAuthenticationUsername":null,"httpAuthenticationPassword":null},"appendToExisting":false},"tuningConfig":{"type":"index_parallel","maxRowsPerSegment":null,"maxRowsInMemory":1000000,"maxBytesInMemory":0,"maxTotalRows":null,"numShards":null,"partitionsSpec":null,"indexSpec":{"bitmap":{"type":"concise"},"dimensionCompression":"lz4","metricCompression":"lz4","longEncoding":"longs"},"indexSpecForIntermediatePersists":{"bitmap":{"type":"concise"},"dimensionCompression":"lz4","metricCompression":"lz4","longEncoding":"longs"},"maxPendingPersists":0,"forceGuaranteedRollup":false,"reportParseExceptions":false,"pushTimeout":0,"segmentWriteOutMediumFactory":null,"maxNumConcurrentSubTasks":1,"maxRetry":3,"taskStatusCheckPeriodMs":1000,"chatHandlerTimeout":"PT10S","chatHandlerNumRetries":5,"maxNumSegmentsToMerge":100,"totalNumMergeTasks":10,"logParseExceptions":false,"maxParseExceptions":2147483647,"maxSavedParseExceptions":0,"buildV9Directly":true,"partitionDimensions":[]}},"context":{"forceTimeChunkLock":true},"groupId":"index_parallel_wikipedia22_2021-04-28T08:20:54.447Z","dataSource":"wikipedia22"}'
    String jsonInputString = '{"type":"index_parallel","resource":{"availabilityGroup":"index_parallel_wikipedia22_2021-04-28T08:20:54.447Z","requiredCapacity":1},"spec":{"dataSchema":{"dataSource":"sheet33","parser":{"type":"string","parseSpec":{"format":"json","timestampSpec":{"column":"timestamp","format":"iso"},"dimensionsSpec":{"dimensions":["channel","cityName","comment","countryIsoCode","countryName","diffUrl","flags","isAnonymous","isMinor","isNew","isRobot","isUnpatrolled","namespace","page","regionIsoCode","regionName","user"]}}},"metricsSpec":[{"type":"count","name":"count"},{"type":"longSum","name":"sum_added","fieldName":"added","expression":null},{"type":"longSum","name":"sum_commentLength","fieldName":"commentLength","expression":null},{"type":"longSum","name":"sum_deleted","fieldName":"deleted","expression":null},{"type":"longSum","name":"sum_delta","fieldName":"delta","expression":null},{"type":"longSum","name":"sum_deltaBucket","fieldName":"deltaBucket","expression":null},{"type":"longSum","name":"sum_metroCode","fieldName":"metroCode","expression":null}],"granularitySpec":{"type":"uniform","segmentGranularity":"DAY","queryGranularity":"HOUR","rollup":true,"intervals":null},"transformSpec":{"filter":null,"transforms":[]}},"ioConfig":{"type":"index_parallel","firehose":{"type":"http","uris":["https://druid.apache.org/data/wikipedia.json.gz"],"maxCacheCapacityBytes":1073741824,"maxFetchCapacityBytes":1073741824,"prefetchTriggerBytes":536870912,"fetchTimeout":60000,"maxFetchRetry":3,"httpAuthenticationUsername":null,"httpAuthenticationPassword":null},"appendToExisting":false},"tuningConfig":{"type":"index_parallel","maxRowsPerSegment":null,"maxRowsInMemory":1000000,"maxBytesInMemory":0,"maxTotalRows":null,"numShards":null,"partitionsSpec":null,"indexSpec":{"bitmap":{"type":"concise"},"dimensionCompression":"lz4","metricCompression":"lz4","longEncoding":"longs"},"indexSpecForIntermediatePersists":{"bitmap":{"type":"concise"},"dimensionCompression":"lz4","metricCompression":"lz4","longEncoding":"longs"},"maxPendingPersists":0,"forceGuaranteedRollup":false,"reportParseExceptions":false,"pushTimeout":0,"segmentWriteOutMediumFactory":null,"maxNumConcurrentSubTasks":1,"maxRetry":3,"taskStatusCheckPeriodMs":1000,"chatHandlerTimeout":"PT10S","chatHandlerNumRetries":5,"maxNumSegmentsToMerge":100,"totalNumMergeTasks":10,"logParseExceptions":false,"maxParseExceptions":2147483647,"maxSavedParseExceptions":0,"buildV9Directly":true,"partitionDimensions":[]}},"context":{"forceTimeChunkLock":true},"groupId":"index_parallel_wikipedia22_2021-04-28T08:20:54.447Z","dataSource":"wikipedia22"}'
    println(jsonInputString)
    
    
    
    OutputStream os = connectionObject.getOutputStream()
        byte[] input = jsonInputString.getBytes("utf-8");
        os.write(input, 0, input.length);
    

    

    if (connectionObject.responseCode == 200) {
      println("[X] send request successfully...")
      println(connectionObject.content.text)
    } else {
      println("[X] can not send request ... try again ...")
      println(connectionObject.content.text)

    }
 

    println("Finish")

  }
}
