# IoTLS: Understanding TLS Usage in Consumer IoT Devices
### Repository for the IMC'21 paper  

We have made the following **data** from our research publicly available: 

- TLS handshake data for 40 devices covering a span of more than 2 years (from, at least, January 2018 to March 2020).

- _./HistoricalCAcertificates_: Historical CA root certificates from Ubuntu, Android, Mozilla and Microsoft. Detailed source information is provided in (Table 3) of the paper. 

- _./FingerprintingAnalysis_: TLS fingerprints for 32 devices along with the TLS handshakes from which they were generated. TLS fingerprints have the same format as the dataset from prior work (https://github.com/platonK/tls_fingerprints). 

- _./RootStoresAnalysis_: Controlled experiments for 8 devices to explore their sets of trusted root certificates (Table 9). Also contains the roots that are common to all platforms, and the ones that have been deprecated from different platorms (Section 4.2). 

- _./InterceptionAttacksTraffic_ Controlled experiments for 32 devices for the interception and other on-path attacks (Tables 5, 6, 7). The SSLKEYLOGFILE files to decrypt successfully MITM'ed connections are also available. Different experiments are denoted by specific indexes in file names:
  
  - 0: NoValidation 
  - 1: InvalidBasicConstraints
  - 2: WrongHostname
  - 3: NoValidation (with TrafficPassthrough -- https://github.com/mitmproxy/mitmproxy/blob/v7.0.3/examples/contrib/tls_passthrough.py)
  - 4: InvalidBasicConstraints (with TrafficPassthrough)
  - 5: WrongHostname (with TrafficPassthrough)
  - 6: IncompleteHandshake
  - 7: TLS 1.0Available 
  - 8: TLS 1.1Available 

In order to access the TLS handshake data and SSLKEYLOGFILE files for MITM attacks, please read the conditions and access instructions at our data sharing agreement (https://github.com/NEU-SNS/IoTLS/blob/main/DataSharingAgreement.pdf). 
