This is the change log of the Elektron-SDK (ESDK) for C++/C. ESDK consists of both the Elektron Message API (EMA) and the Elektron Transport API (ETA). This file contains history starting from ESDK 1.2.0 which is when all components (EMA C++, EMA Java, ETA C, ETA Java) of ESDK were fully open sourced. Note that ESDK version numbers start from 1.2.0 and EMA/ETA version numbers start from 3.2.0.

There are three types of ESDK releases that append a letter directly followed by a number to the version number. 

"L" releases (e.g., 1.2.0.L1) are full ESDK releases that are uploaded to MyRefinitiv (formerly Customer Zone), Developer Community and GitHub. 
"G" releases (e.g., 1.2.0.G1) are releases that are only uploaded to GitHub. 
"E" releases (E-Loads) are emergency ESDK releases that are uploaded to MyRefinitiv and Developer Community but not to GitHub. Also note that emergency releases may only be partial (i.e., Java or C++/C only).

----------------------------------------------------------------------------------------
CURRENT RELEASE HIGHLIGHTS - ESDK C/CPP 1.5.0.L1 aka EMA 3.5.0.L1 and ETA 3.5.0.L1
----------------------------------------------------------------------------------------

New Features Added
------------------
This is a maintenance GitHub push which resolves customer issus, bugs and adds support for the following: ability for providers to get round trip latency measurements, provider support for posting, permit server side socket to be reused and ability to configure takeExclusiveSignOn in EDP connectivity.

Customer Issues Resolved
------------------
- [GitHub # 117] [ESDK-504] Support Posting in EMA Providers
- [Case Number: 06708565] [ESDK-1650] rsslDoubleToReal conversion function doesn't work as expected 
- [Case Number: 07697024] [GitHub # 141] [ESDK-3292] Dictionary.entry(int fieldId) returns the same DictionaryEntry instance
- [Case Number: 07823520] [ESDK-3441] ETA Reactor API persistently retains memory not released until shutdown (reactor events)

----------------------------------------------------------------------------------------
FULL CHANGELOG
----------------------------------------------------------------------------------------

---------------------------------------------
ESDK C++/C Release 1.5.0.G1 (Jun 30, 2020)
---------------------------------------------

EMA C++ 3.5.0.G1 Issues Resolved
--------------------------------
- [ESDK-504] Support Posting in EMA Providers [GitHub # 117]
- [ESDK-1440] Rename EMAC++ Unit Test input files to be more descriptive
- [ESDK-2587] Cons170 memory leak reported from valgrind
- [ESDK-3292] Dictionary.entry(int fieldId) returns the same DictionaryEntry instance [Case Number: 07697024] [GitHub # 141]
- [ESDK-3843] Support SO_REUSEADDR to permit server side socket to be reused for loadbalancing
- [ESDK-3907] Ema Cons113 Example does NOT work with EncryptedProtocolType::RSSL_WEBSOCKET
- [ESDK-3908] Support EMA EDP Websocket encrypted connection example 
- [ESDK-3933] Suppport Round Trip Latency Monitoring
- [ESDK-3988] Change EMA EDP example to take RIC as an input

ETA C 3.5.0.G1 Issues Resolved
--------------------------------
- [ESDK-1650] rsslDoubleToReal conversion UPA C API lib function doesn't work as we expected [Case Number: 06708565]
- [ESDK-3441] ETA Reactor API persistently retains memory and is not released until shutdown [Case Number: 07823520]
- [ESDK-3819] Suppport Round Trip Latency Monitoring
- [ESDK-3850] VS110 and VS120 json conversion test issues
- [ESDK-3963] Add ability to catch WSAEWOULDBLOCK  error
- [ESDK-4069] Tunnel stream must notify application when login timeout occurs for authenticating a tunnel stream

Both ETA C and EMA C++ 3.5.0.G1 Issues Resolved
-----------------------------------------------
- [ESDK-3859] JSON to RWF conversion passing thru errors in Time
- [ESDK-3860] Invalid conversion of UINT64 when value on wire is -1
- [ESDK-3903] Provide the ability to configure the takeExclusiveSignOnControl parameter for the password grant type
- [ESDK-4084] EMA should not set compression threshold unless explicitly configured by application 

---------------------------------------------
ESDK C++/C Release 1.5.0.L1 (Mar 31, 2020)
---------------------------------------------

EMA C++ 3.5.0.L1 Issues Resolved
--------------------------------
- [ESDK-3244] Catch polymorphic type by reference, not by value [GitHub Pull Request# 97]
- [ESDK-3274] EMAC++ 'OmmInvalidUsageException', Text='The Field name STOCK_TYPE does not exist in the field dictionary' [Case Number: 07645599]

ETA C 3.5.0.L1 Issues Resolved
--------------------------------
- [ESDK-3616] Watchlist example issue: With service down, posting is still attempted
- [ESDK-3805] Integrate rsslReactorQueryServiceDiscovery() method with centralized token management to reuse token when using same credentials 

Both ETA C and EMA C++ 3.5.0.L1 Issues Resolved
-----------------------------------------------
- [ESDK-3419] ESDKC Websocket Transport Support 
- [ESDK-3437] Add port info into OmmConsumerEvent::getChannelInformation [GitHub # 113]
- [ESDK-3475] ESDK C RWF<->JSON conversion
- [ESDK-3818] Support for SNI (server name indication) in TLS communication in client side encryption with openSSL
- [ESDK-3834] Update default token service URL to use verison v1

---------------------------------------------
ESDK C++/C Release 1.4.0.G1 (Jan 10, 2020)
---------------------------------------------

EMA C++ 3.4.0.G1 Issues Resolved
--------------------------------
- [ESDK-3472] Added support for NoWait dispatch timeout in Consumer and NiProvider [GitHub # 110] 
- [ESDK-3596] Removed TLS 1.0 and 1.1 enumerations from EMA interface

ETA C 3.4.0.G1 Issues Resolved
--------------------------------
- [ESDK-126] Fix to Ansi library build and runtime issues [Case Number: 04035985 GitHub #124]

Both ETA C and EMA C++ 3.4.0.G1 Issues Resolved
-----------------------------------------------
- [ESDK-3594] Documentation changes with addtional rebranding changes

---------------------------------------------
ESDK C++/C Release 1.4.0.L1 (Nov 15, 2019)
---------------------------------------------

EMA C++ 3.4.0.L1 Issues Resolved
--------------------------------
- [ESDK-3294] Enhancement Request: Added ability to dynamically increase number of allocated output buffers for handling "out of buffers" error [Case Number: 07652023]
- [ESDK-3417] Documentation Issue: Specify in EMA Config guide, the precedence of configuration vectors
- [ESDK-3495] Memory leak in C++/EMA (in OmmConsumer/OmmLoggerClient [Case Number: 08003411 GitHub # 118])
- [ESDK-3535] Inconsistency contents in default and description of ReissueTokenAttemptInterval and ReissueTokenAttemptLimit parameter [GitHub # 120]

ETA C 3.4.0.L1 Issues Resolved
--------------------------------
- [ESDK-755] Trying to establish more than 2 encrypted connections fails returning an error, when using ETAC provider
- [ESDK-3503] Memory Growth with ESDK 1.3.X: Remove error struct from event to avoid memory usage
- [ESDK-3504] Add option for maxOutputBuffer on ProvPerf
- [ESDK-3505] Add ability of upacTransportPerf to support compressionType lz4 as the input argument
- [ESDK-3538] Uptick version on non-open source libs only when binary version changes

Both ETA C and EMA C++ 3.4.0.L1 Issues Resolved
-----------------------------------------------
- [ESDK-3181] ESDKC Server side encryption support
- [ESDK-3202] ESDK Documentation: Remove classic portal, refer to VARefman
- [ESDK-3204] ESDK Documentation: Fix copyright link after removal of classic portal from esdk repository
- [ESDK-3500] Enhancement Request: Add ability to retrieve number of tunnel stream buffers in use
- [ESDK-3340] Rebrand ESDK documentation 

---------------------------------------------
ESDK C++/C Release 1.3.1.G2 (Oct 18, 2019)
---------------------------------------------

Both ETA C and EMA C++ 3.3.1.G2 Issues Resolved
-----------------------------------------------
- [ESDK-3265] Sporadic crash in ESDK consumers with service interruptions [Case Number: 07573905,08051848 GitHub # 103,108]
- [ESDK-2562] Shared pool buffers actively queued upon client disconnection are not cleaned up correctly [Case Number: 07010347]

---------------------------------------------
ESDK C++/C Release 1.3.1.G1 (Sept 25, 2019)
---------------------------------------------

EMA C++ 3.3.1.G1 Issues Resolved
--------------------------------
- [ESDK-3440] Provider fails to accept client connections with dispatch timeOut=NoWaitEnum [GitHub #110]

ETA C 3.3.1.G1 Issues Resolved
--------------------------------
- [ESDK-3442] ipcWaitProxyAck should return RIPC_CONN_IN_PROGRESS for all success cases 
- [ESDK-3453] ReactorChannel event -3 causing reactor to shutdown

Both ETA C and EMA C++ 3.3.1.G1 Issues Resolved
-----------------------------------------------
- [ESDK-3468] Add EDP Auth proactive token renewal with password grant prior to refresh token expiration

---------------------------------------------
ESDK C++/C Release 1.3.1.L1 (July 31, 2019)
---------------------------------------------

New Features Added
------------------
This release adds ability in EMA to clone and copy messages in order to decode payload outside of message callbacks. This release enables Realtime Cloud users to centralized session management per OAuth user shared between multiple connections. Please note that client_id is now a mandatory input for Cloud connectivity. ESDK C/C++ now supports GCC 7.4.0. 

EMA C++ 3.3.1.L1 Issues Resolved
--------------------------------
- [ESDK-509] Add InitializationTimeout to EMA Config at Channel Level
- [ESDK-633] EmaCppConsPerf does not reach steady state occasionally [Case Number: 05594510]
- [ESDK-900] Change documentation to reflect user-defined Config filename
- [ESDK-1750] Clone/copy facility for message payload to decode it outside of onUpdateMsg() [Case Number: 06854285,5201994]
- [ESDK-3238] Incorrect spelling in interface name in EmaCpp
- [ESDK-3251] Fix extendedHeader typo where Status is returned instead of Close
- [ESDK-3252] Please restore version headers, eg EmaVersion.h [GitHub #105]

ETA C 3.3.1.L1 Issues Resolved
--------------------------------
- [ESDK-3176] Windows build warning
- [ESDK-3182] Documentation, ETAJ Dev Guide: Fix "UPA" in Figure 36 to "Transport API Consumer App"
- [ESDK-3184] Warning when building rsslTransportUnitTest on RH6
- [ESDK-3185] Warning rsslRestClientImpl.c about RsslRestCurlHandleSumFunction
- [ESDK-3202] ESDK Documentation: Remove links to "Transport API Value Added Components" in html and refer to VARefman
- [ESDK-3243] Fix application ID length in Eta Examples [GitHub #100]
- [ESDK-3253] Compile Error: rsslTransport.h:1343:82: error: too many initializers for ‘RsslWriteInArgs’
- [ESDK-3255] Enhance the Reactor to specify OAuth token credentials in rsslReactorOmmConsumerRole
- [ESDK-3258] The rsslCreateReactor() method crashes when the RsslCreateReactorOptions.serviceDiscoveryURL is empty
- [ESDK-3267] Expose ping stats and rsslReadEx in reactor
- [ESDK-3269] Enhance the Reactor for applications to specify the password for OAuth via the callback method
- [ESDK-3278] Enhance the Reactor error handling wrt to session mgmt POST
- [ESDK-3285] Add ability to turn on debugging for encrypted connections to diagnose TLS issues on incoming packets
- [ESDK-3295] Crash in reactor when multiple reactor channels are used with session management
- [ESDK-3296] Provides centralized location to keep the OAuth tokens to share between multiple connections using the same OAuth credential

Both ETA C and EMA C++ 3.3.1.L1 Issues Resolved
-----------------------------------------------
- [ESDK-3249] Support 32-bit builds with ESDK 
- [ESDK-3260] EMA log files exist in ESDK AMI
- [ESDK-3266] Add 32-bit DACS libraries into BinaryPack and open source ANSI
- [ESDK-3272] Qualify ESDK with GCC Version 7.4.0
- [ESDK-3410] Removed extra "/" to service discovery URL to get an Elektron cloud endpoint

---------------------------------------------
ESDK C++/C Release 1.3.0.G1 (April 16, 2019)
---------------------------------------------

EMA/ETA C/C++ 3.3.0.G1 Issues Resolved
--------------------------------
- [ESDK-3194] Documentation improvements for EDP examples [GitHub #98]
- [ESDK-3239] CMake fix for build of cjson libraries

---------------------------------------------
ESDK C++/C Release 1.3.0.L1 (March 26, 2019)
---------------------------------------------

New Features Added
------------------
This ESDK release provides support for EDP Session management (token renewal) and Service Discovery (discovering host/port information based on Cloud region and type of connection ). Also available is added support for encrypted transport using openSSL versions 1.0.X and 1.1.X on Windows and Linux for EMA C++ and ETA C. Also in this release, all external dependencies such as libxml2, zlib, lz2 rely on associated external distribution locations and incorporated into build using cmake. 

EMA C++ 3.3.0.L1 Issues Resolved
--------------------------------
- [ESDK-484] EMA Consumer application that requests a streaming source directory does not receive source directory updates. [ Case 05257390 ]
- [ESDK-619] RMTES Partial updates are not processed correctly if OmmRmtes.toString() is called before OmmRmtes.apply() is called [Case Number: 05533464, GitHub #74]
- [ESDK-1245] Qualify Linux GCC 4.8.5
- [ESDK-1480] Default CMAKE option in GSG package to be cmake -DUSE_PREBUILT_ETA_EMA_LIBRARIES=ON
- [ESDK-1565] Turn on OpenSSL support for Windows Client connections
- [ESDK-1611] Client side encryption
- [ESDK-1622] Elektron-SDK-BinaryPack should be optional, client can't download external resources via git [Case Number: 06643952]
- [ESDK-1626] Update OpenSSL usage to support both 1.0.X and 1.1.X interfaces at run-time
- [ESDK-1687] Use Cmake to obtain Zlib from GitHub
- [ESDK-1688] Use Cmake to obtain Libxml2 from GitHub
- [ESDK-1714] Provides interface design and implementation for EMACPP to support session managment from the Reactor
- [ESDK-1760] Fix uname program name in cmake setup [GitHub #81]
- [ESDK-2599] Require a new utility or interface similar to asHexString that shows raw hex output [Case Number: 07023993]
- [ESDK-2678] Expose initializationTimeout configuration and make default to higher value for Encrypted

ETA C 3.3.0.L1 Issues Resolved
--------------------------------
- [ESDK-132] ETAC WL consumer example with encrypted connection is crashing when channel initialization fails
- [ESDK-627] Remove references to UPA in ETA C and ETA Java Developers Guide [Case Number: 05543578]
- [ESDK-212] Incorrect syntax for command line argument example with upacTransportPerf example
- [ESDK-1245] Qualify Linux GCC 4.8.5
- [ESDK-1565] Turn on OpenSSL support for Windows Client connections
- [ESDK-1611] Client side encryption
- [ESDK-1626] Update OpenSSL usage to support both 1.0.X and 1.1.X interfaces at run-time
- [ESDK-1628] ETAC: Extend OpenSSL usage to verify the certificate
- [ESDK-1687] Use Cmake to obtain Zlib from GitHub
- [ESDK-1688] Use Cmake to obtain Libxml2 from GitHub
- [ESDK-1710] Provides HTTP requests for blocking and non-blocking call for ETAC
- [ESDK-1716] Implements EDP service discovery and token management for ETAC reactor
- [ESDK-1746] Update ETA examples to connection using HTTPS connection type with/without a proxy
- [ESDK-1747] Fix Cpp-C ANSI and DACS Guide links in reference manual
- [ESDK-2603] CMake changes for new add external project cmake modules
- [ESDK-2605] Remove references to TS1 Parser

---------------------------------------------
ESDK C++/C Release 1.2.2.L1 (November 15, 2018)
---------------------------------------------

New Features Added
------------------
Provides the functionality for Non-interactive, Interactive, and Consumer applications to get channel information from the EMA's callback methods via OmmProviderEvent and OmmConsumerEvent classes

EMA C++ 3.2.2.L1 Issues Resolved
--------------------------------
- [ESDK-632] Elektron SDK EmaCppConsPerf latencyFile doesn't create log file [Case Number: 05541113]
- [ESDK-1125] EMA ConsPerf applications do not use specified username in Login Request [Case Number: 05958811]
- [ESDK-1517] Unable to exit with EMAC multithread app
- [ESDK-1601] Provide channel information in EMA's callback methods [Case Number: 06611113]
- [ESDK-1751] Remove undefined increment operator behavior [GitHub Pull Request #80]
- [ESDK-1753] Add support for WindowsServer2016
- [ESDK-1723] IProvider application with UserDispatch has 100% cpu
- [ESDK-2543] Change to EMA Devlopers Guide to accurately show map encoding follow up to ESDK-1323

ETA C 3.2.2.L1 Issues Resolved
--------------------------------
- [ESDK-647] EMAJ or ETAJ consumer sends duplicate FIDs in a snapshot view request
- [ESDK-1753] Add support for WindowsServer2016 
- [ESDK-2550] ETA RDM Usage guide section 6.2.4 shows market price update instead of status [Developer Community]

---------------------------------------------
ESDK C++/C Release 1.2.1.L1 (August 15, 2018)
---------------------------------------------

New Features Added
------------------
Programmatic configuration for EMA IProvider and NIProvider.

EMA C++ 3.2.1.L1 Issues Resolved
--------------------------------
- [ESDK-380] If CompressionType is set to "None", the CompressionThreshold range check still occurs
- [ESDK-398] XMLTrace may not flush all information to trace file
- [ESDK-405] Example 421 is not using the Dictionary_1 and Logger_1 defined in the code [Case Number: 04296327]
- [ESDK-415] Clarify parent handle usage in EMA interface [Case Number: 05109877]
- [ESDK-430, ESDK-1323, ESDK-1552] EMA C++ crashes when encoding a large Map [Case Numbers: 05354708, 06292070, GitHub #54]
- [ESDK-635] EMA C++ Compiler warnings [Case Number: 05830919]
- [ESDK-1496] Double login reissue & Exception with EMA C++ NIProvider (430)
- [ESDK-1529] Ema Example Cons100 valgrind errors when EmaConfig.xml is present
- [ESDK-1548] Update RDMUsageGuide to include information on the required filters to mark a service back Up [Case Number: 06538048]
- [ESDK-1556] Update Doxygen for OmmDateTime, OmmDate and OmmTime [GitHub #55]
- [ESDK-1560] Provide ability to modify the configuration programmatically for IProvider [Case Number: 06548186]
- [ESDK-1593] Migration Guide Issues with CMake Elektron SDK 1.2
- [ESDK-1595] Calling toString on a newly created message throws Access Violation Exception [Case Number: 06484891]
- [ESDK-1624] Can't build Elektron-SDK1.2.0.win.rrg on MS Windows [Case Number: 06612117]
- [ESDK-1644] Fix README content Github to have change log (without duplicating information)

ETA C 3.2.1.L1 Issues Resolved
------------------------------
- [ESDK-380] If CompressionType is set to "None", the CompressionThreshold range check still occurs
- [ESDK-398] XMLTrace may not flush all information to trace file
- [ESDK-1423] Warnings ( 240 ) when doing build all
- [ESDK-1574] Check for empty string instead of null pointer [GitHub #61]
- [ESDK-1593] Migration Guide Issues with CMake Elektron SDK 1.2
- [ESDK-1624] Can't build Elektron-SDK1.2.0.win.rrg on MS Windows [Case Number: 06612117]
- [ESDK-1635] ETA should not have EDF/Queue examples
- [ESDK-1636] Consumer Module_2_Login training example does not properly fall through
- [ESDK-1644] Fix README content Github to have change log (without duplicating information)
- [ESDK-1659] ETA Consumer reserves too little space for AuthenticationToken

------------------------------------------
ESDK C++/C Release 1.2.0.G1 (May 31, 2018)
------------------------------------------

EMA C++ 3.2.0.G1 Issues Resolved
--------------------------------
- [ESDK-1572] IProvider application hits 100% CPU in API dispatch mode after Consumer disconnects [Case Number: 06564982]

ETA C 3.2.0.G1 Issues Resolved
------------------------------
- [ESDK-1573] rsslNumericStringToReal() conversion error [GitHub #62]

--------------------------------------------
ESDK C++/C Release 1.2.0.L1 (April 27, 2018)
--------------------------------------------

New Features Added
------------------
ESDK C/C++ now utilizes a CMake build environment. Refer to the ESDK C/C++ Migration Guide for detailed instructions regarding how to build EMA C++ with CMake.

ESDK C/C++ now supports Visual Studio 2017.

EMA now supports encrypted connection type.

ETA C is now fully open sourced except for reliable multicast transport and VA cache. Open source transports include TCP, HTTP, HTTP encrypted, shared memory and sequenced multicast transport types. The OMM encoder and decoder have also been open sourced.

Note that the memory footprint has increased this release due to the following:

Around 20 MB is introduced by changing the container type for handling message fragmentation. The hash table is initialized when a rsslChannelImpl is created which ETA allocates 10 of them upfront for this first initialization of Rssl library.

Around 4.6 MB is introduced by the new functionality of RsslDataDictionary to look up
RsslDictionaryEntry by name (rsslDictionaryGetEntryByFieldName).

EMA C++ 3.2.0.L1 Issues Resolved
--------------------------------
- [ESDK-487] EMA throws OmmInvalidUsageException if an empty Map is encoded [Case No. 05338640 and GitHub #28]
- [ESDK-813] Date/Time/DateTime to string and from string conversions should support ISO 8601 format.
- [ESDK-907] EMA can't handle a SERVICE_DIRECTORY refresh that contains a lot of services [Case No 05896732, 06042281 and 06443659]
- [ESDK-1145] Add const to EMAString
- [ESDK-1194] Expose encrypted connection support through EMACPP
- [ESDK-1280] Remove duplicated assignments [GitHub pull request #45]
- [ESDK-1290] ripc sslName cryptoName copy limits to 8 bytes
- [ESDK-1359] Add VS2017 to ESDK

ETA C 3.2.0.L1 Issues Resolved
------------------------------
- [ESDK-709] No genericmsg be fan out to the client on directory domain stream
- [ESDK-901] EMA does not honor the filters on the directory request message [Case No. 05881972]
- [ESDK-1262] Fix bigBufferPoolCleanup for loop [GitHub Pull Request #43]
- [ESDK-1280] Remove duplicated assignments [GitHub pull request #45]