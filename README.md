# simulink-udpip-blocks
Simulink&reg blocks for UDP/IP communication

  These two blocks allow exchanging data bytes via an UDP/IP connection 
  between simulink schemes possibly running as different processes on 
  different (windows) machines.
  
  Differently from the TCP/IP protocol, UDP/IP is totally asyncronous and 
  non-blocking thus generally allowing a faster communication.
  Additionally, the client and server can be started or stopped in any order,
  as opposite to the TCP/IP case, where the server must always be started
  before the client is started and stopped after the client is stopped.

  To recompile the code, from the matlab command window, type:
  mex SimUdpClient3.c ws2_32.lib 
  mex SimUdpServer3.c ws2_32.lib

  Finally, note that you can use the "byteview" block, available 
  at https://github.com/giampy1969/simulink-signal-byteview
  (or under MATLAB Central >  File Exchange > Utilities > Simulink) 
  to transform any simulink data type into bytes (aka uint8) and back.
  
