#Firmware Action Service
The Firmware Action Service (FAS) will be the predominant tool used to affect a firmware image state change (upgrade/downgrade) for Shasta.  FAS is a RESTful microservice (written in Go), maintained by CASM-HMS.  FAS as a service is deployed inside the service mesh in the management plane. FAS performs out-of-band (oob) firmware image updates via Redfish. 

### FAS Replaces FUS
FAS is the replacement for FUS.  FUS (Firmware Update Service) was the first implementation, and it has been decided for [many reasons that FUS must be replaced.](docs/Replacing_firmware_update_service.md)

### FAS CT Testing
This repository builds and publishes hms-fas-ct-test RPMs along with the service itself containing tests that verify FAS on the
NCNs of live Shasta systems. The tests require the hms-ct-test-base RPM to also be installed on the NCNs in order to execute.
The version of the test RPM installed on the NCNs should always match the version of FAS deployed on the system.

## Table of Contents

* [FAS v1.0 vs FUS Feature Comparison](docs/Feature_Comparison.md)
* [Scenarios](docs/action_scenarios.md)
* [Control Logic](docs/control_loop.md)
* [Dependency Management](docs/Dependency_Management.md)
* [Developer Environment](docs/developer_environment.md)
* [Test Environment](docs/test_environment.md)
* [Understanding Images](docs/Understanding_Images.md)





