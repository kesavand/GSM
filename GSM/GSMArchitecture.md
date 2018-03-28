
![Optional Text](https://github.com/kesavand/GSM/blob/master/Images/GSMArchitecture.jpg)



Mobile Station (MS):
-------------------
A mobile station communicates across the air interface with a base station transceiver in the same cell in which the mobile subscriber unit is located. 

Base Station Subsystem (BSS):
============================
The Base Station Subsystem (BSS) section of the GSM network architecture that is fundamentally associated with communicating with the mobiles on the network. It consists of two elements:

BTS:
---
Base Transceiver Station (BTS):
The BTS used in a GSM network comprises the radio transmitter receivers, and their associated antennas that transmit and receive to directly communicate with the mobiles.

BSC:
----
Base Station Controller (BSC):
The BSC forms the next stage back into the GSM network. It controls a group of BTSs,It communicates with the BTSs over what is termed the Abis interface.

![Optional Text](https://github.com/kesavand/GSM_GPRS/blob/master/Images/GSM_NSS_logical_placement.PNG)

Network Switching Subsystem (NSS):
=================================
The NSS has one hardware, Mobile switching center and four software database element: Home location register (HLR), Visitor location Register (VLR), Authentications center (Auc) and Equipment Identity Register (EIR). 
Mobile switch center (MSC)
Home location register (HLR)
Visitor location Register (VLR)
Authentications center (Auc)
Equipment Identity Register (EIR)

Mobile switching center (MSC):
-----------------------------
The mobile switching center (MSC) is responsible for switching the calls to PSTN,ISDN from the mobile network  Interfaces to other MSCs are provided to enable calls to be made to mobiles on different networks., MSC sets up and releases the end-to-end connection, handles mobility and hand-over requirements during the call.

The visited MSC (V-MSC) is the MSC where a customer is currently located. The visitor location register (VLR) associated with this MSC will have the subscriber's data in it.

The gateway MSC (G-MSC) is the MSC that determines which "visited MSC" (V-MSC) the subscriber who is being called is currently located at. It also interfaces with the PSTN.The GMSC is the point to which a ME terminating call is initially routed, without any knowledge of the MS's location.The GMSC is thus in charge of obtaining the MSRN (Mobile Station Roaming Number) from the HLR based on the MSISDN (Mobile Station ISDN number, the "directory number" of a MS) and routing the call to the correct visited MSC.

The anchor MSC is the MSC from which a handover has been initiated. The target MSC is the MSC toward which a handover should take place.
media gateway (MGW) makes it possible to cross-connect circuit switched calls switched by using IP, ATM AAL2 as well as TDM. More information is available in 3GPP TS 23.205.

Home location register (HLR):
----------------------------
This database contains all the administrative information about each subscriber, It stores the (IMSI,MSISDN, service profile, location information,current locations, forwarding address of the subscriber), In this way, the GSM network is able to route calls to the relevant base station for the MS. When a user switches on their phone, the phone registers with the network and from this it is possible to determine which BTS it communicates with so that incoming calls can be routed appropriately. Even when the phone is not active (but switched on) it re-registers periodically to ensure that the network (HLR) is aware of its latest position. There is one HLR per network, although it may be distributed across various sub-centres to for operational reasons.

Visitor Location Register (VLR):
-------------------------------
The VLR is temporary database software similar to the HLR identifying the mobile subscribers visiting inside the coverage area of an MSC. The VLR assigns a Temporary mobile subscriber Identity (TMSI) that is used to avoid using IMSI on the air. When a mobile subscriber roams from one LA (Local Area) to another, current location is automatically updated in the VLR. When a mobile station roams into anew MSC area, if the old and new LA’s are under the control of two different VLRs, the VLR connected to the MSC will request data about the mobile stations from the HLR. The entry on the old VLR is deleted and an entry is created in the new VLR by copying the database from the HLR.


Equipment Identity Register (EIR):
---------------------------------
The EIR is the entity that decides whether a given mobile equipment may be allowed onto the network. Each mobile equipment has a number known as the International Mobile Equipment Identity. This number, as mentioned above, is installed in the equipment and is checked by the network during registration. Dependent upon the information held in the EIR, the mobile may be allocated one of three states - allowed onto the network, barred access, or monitored in case its problems.

Authentication Centre (AuC):
---------------------------
The AuC is a protected database that contains the secret key also contained in the user's SIM card. It is used for authentication and for ciphering on the radio channel.

GSM Protocol Stack:
==================
![Optional Text](https://github.com/kesavand/GSM_GPRS/blob/master/Images/gsm-protocol-stack.gif)


GSM Address and Identificaton:
==============================
Mobile Subscriber ISDN Number (MSISDN):
---------------------------------------
The authentic telephone number of a mobile station is the Mobile Subscriber ISDN Number (MSISDN).Based on the SIM, a mobile station can have many MSISDNs, as each subscriber is assigned with a separate MSISDN to their SIM respectively.It consists of the following thress numbers.
1. Country Code (CC) : Up to 3 decimal places.
2. National Destination Code (NDC) : Typically 2-3 decimal places.
3. Subscriber Number (SN) : Maximum 10 decimal places.

Mobile Station Roaming Number (MSRN):
-------------------------------------
Mobile Station Roaming Number (MSRN) is an interim location dependent ISDN number, assigned to a mobile station by a regionally responsible Visitor Location Register (VLA). Using MSRN, the incoming calls are channelled to the MS.HLR maps the MSRN to the ISDN.
The MSRN has the same structure as the MSISDN.

1.Country Code (CC) : of the visited network.
2.National Destination Code (NDC) : of the visited network.
3.Subscriber Number (SN) : in the current mobile network.

Temporary Mobile Subscriber Identity (TMSI):
--------------------------------------------
Temporary Mobile Subscriber Identity (TMSI) can be assigned by the VLR, which is responsible for the current location of a subscriber. The TMSI needs to have only local significance in the area handled by the VLR. This is stored on the network side only in the VLR and is not passed to the Home Location Register (HLR).Together with the current location area, the TMSI identifies a subscriber uniquely. It can contain up to 4 × 8 bits.

Location Area Code(LAC) :
-------------------------
The Location Area Code uniquely identifies a LA (Location Area) within a PLMN (Public Land Mobile Network). It may range from 0 to 65,535.

Cell Identifier (CI):
---------------------
Using a Cell Identifier (CI) (maximum 2 × 8) bits, the individual cells that are within an LA of a PLMN can be recognized. 

Location Area Identity (LAI): 
----------------------------
Each location area of a public land mobile network (PLMN) has its own globally unique identifier which is known as its location area identity (LAI). This internationally unique identifier is used for location updating of mobile subscribers.
LAI = MCC + MNC + LAC

CellGlobalIdnetity(CGI):
------------------------
When the Global Cell Identity (LAI + CI) calls are combined, then a cell is globally uniquely identified.
