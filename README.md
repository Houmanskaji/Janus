# LotusCom Janus Lab, 10 users

LotusCom Janus is a cloud-native packet core for mobile operators,
private 5G, and MEC: 4G EPC and 5G Core in one integrated system,
built on 3GPP Release 18, under one licence.

LotusCom Janus carries data. LotusCom Janus+ is Janus with IMS added,
so it also carries voice: VoNR over 5G, VoLTE over 4G, and WiFi
Calling over WiFi, with SIP and RTP media. This package is the
Janus+ lab build.

This build is 3GPP R-18-based and includes Dual Core, the 5GC and
4G EPC, network slicing, policy control, WiFi offload through
N3IWF and ePDG, IMS voice with SIP and RTP, and a NOC console.

The build contains AMF, SMF, UPF, AUSF, UDM, UDR, NRF, PCF, NSSF,
and NEF for 5G; MME, SGW, PGW, and HSS for 4G; N3IWF and ePDG for
WiFi offload; P-CSCF, I-CSCF, S-CSCF, and MRF for IMS; and the NOC
console.

This is the Janus Real build, version 1.0.0-real. Compared with the
earlier lab build, it adds the real wire protocols (NGAP, Xn,
GTP-U, PFCP, S1AP, GTPv2, Diameter S6a, IKEv2), SUCI concealment,
SNOW 3G and ZUC (128-NEA1, 128-NIA1, 128-NEA3, 128-NIA3), TLS for
the SBI, console login with roles, a file-backed persistent store,
CHF charging, NEF callback push, IPv6 and ATSSS steering, and IMS
services (TAS, ENUM, emergency calls, SRVCC, AMR-WB and EVS,
SRTP). The installation guide in this package is the earlier lab
guide, reused unchanged; the new ports and features are listed in
the Janus Real README.

## Limits

This lab build is locked by licence to 10 subscribers, 2 eNB and
2 gNB, and expires on 2027-11-23. The store is file-backed and
survives a restart. The subscriber data lives in janus-store.json
next to the binary. The console default login is
LotusComSuperAdmin; change the password at first login. The
/status endpoint stays open for the Panoptes polling point.

SCTP is the real deployment transport for NGAP and S1AP; this lab
build runs those protocols over TCP. A real deployment supplies
the SCTP stack.

## Contact

For installation and licence requests, contact LotusCom at
houman@lotuscom.net.

LotusCom Janus is a product of Lotus Communication Systems Inc.
