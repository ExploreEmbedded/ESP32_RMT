
//remote library structure.

begin(uint8_t pin, bool mode)

/*
@param pin: Pin number on ESP32 hardware.
@param mode: Use the remote as transmitter(1) or receiver(0)

-- Allocotes RTM Peripheral channnel (0-7) depending on avialiblity
-- Allocates channel memory. Currently only fixed allocation of 64 x 32 bits (265 bytes) is   allowed for each channel.
-- ToDo: allocate additional memory for first channels if needed.

*/


//sends address and command data with specified protocol

send(uint8_t addr, uint8_t data, uint8_t protocol);

/*
|
|  @param addr remote address to be sent. Some
|   
|
|
|   It is assumed that we would want to send commands to receivers with different 	  	  |   protocols,hence protocol input is necessary.
|   
|
*/


// bulk data send 
send(uint8_t addr, uint16_t dataArray[], uint8_t protocol);




