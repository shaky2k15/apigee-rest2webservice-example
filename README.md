# apigee-rest2webservice-example
These examples give an idea of how to use apigee to convert backend webservices into RESTFul json responses with JSON requests as inputs. In simple terms REST 2 WEBSERVICE translation.

I tried these 2 examples as a part of an interview exercise with one of the IT product/services company.

First example :
APIGEE proxy instance using public SOAP web service for weather reports based on ZIP inputs.

Apigee url to test :  (Here ZIP value refers to US post code)
http://apigee2k15-test.apigee.net/weather/cityweatherbyzip?ZIP=70126

Backend SOAP url service:
http://wsf.cdyne.com/WeatherWS/Weather.asmx?WSDL

Backend request input : 
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns1="http://ws.cdyne.com/WeatherWS/">
  <SOAP-ENV:Body>
    <ns1:GetCityWeatherByZIP>
      <ns1:ZIP>70126</ns1:ZIP>
    </ns1:GetCityWeatherByZIP>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>


Second example :
Apigee proxy using public SOAP web service to retrieve bank details based bank code 

Apigee url to test :  (Here blz value refers to German bank code)
http://apigee2k15-test.apigee.net/blzservice/bank?blz=54862500

Backend SOAP url service:
http://www.thomas-bayer.com/axis2/services/BLZService?wsdl

Backend request input : 
<?xml version="1.0" encoding="UTF-8"?>
<SOAP-ENV:Envelope xmlns:SOAP-ENV="http://schemas.xmlsoap.org/soap/envelope/" xmlns:ns1="http://thomas-bayer.com/blz/">
  <SOAP-ENV:Body>
    <ns1:getBank>
      <ns1:blz>54862500</ns1:blz>
    </ns1:getBank>
  </SOAP-ENV:Body>
</SOAP-ENV:Envelope>
