# TS-LoRa 
Time-Slotted LoRa(WAN) for the Industrial Internet of Things

This is a stand-alone implementation of the TS-LoRa protocol as it is presented in the paper "TS-LoRa: Time-Slotted LoRaWAN for the Industrial Internet of Things". The implementation consists of 4 parts; the node part, the gateway request part, the gateway data part, and the Raspberry Pi part. The code has been designed for and tested on Pycom Lopy4 and Fipy devices with SF7-9. To run this code you will need at least 3 Pycom devices with LoRa and Wifi support (2 for the gateways + 1 node). Modifications may be needed to adjust the scenarios to your own needs. All the code except of the Raspberry Pi TCP server script is strictly licensed under the GNU GPL v3 (see LICENSE file).

Features:
- Time-slotted LoRa transmissions with a fixed slot length
- Inter and intra-SF collision-free transmissions
- Synchronisation and ACKnowledgements (SACK)
- Retransmissions
- 1% radio duty cycle
- Multiple SFs/BWs
- A simple registration mechanism (similar to LoRaWAN OTAA) including the generation of AppSKeys
- Statistics per node

Limitations / Work in progress:
- Two or more 1-channel gateways must currently be used. 
- No data encryption is currently performed. The keys are calculated but I don't encrypt/decrypt data for testing purposes. 
- ~~A 98-byte data packet consisting of 98 1's is currently sent for testing purposes.~~
- Python's pack and unpack struct functions are currently used to send data. 
- Sleep mode is not currently implemented.

For any serious inquires please contact the author at dimzorbas@ieee.org
