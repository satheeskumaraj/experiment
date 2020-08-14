# redis-window-exercise
Windows problem solving

Problem statement: We have an issue with the web application installed. When browsing to http://localhost/ we get a 503 exception.

Issue identification: 

While checking that issue, i came to know that , DefaultAppPool is in stopped status in IIS Manger. So i tried to start the default one. But it’s again went down. After dig that issue. I came to know that, the Identity was mentioned “AppPoolServiceUser”, But is should be the “ApplicationPoolIdentity”.

Solution:
After changed Identity from “AppPoolServiceUser”  to  “ApplicationPoolIdentity”. And restarted, it’s working fine.


For more information please refer the document.