# **DIO Driver based on AUTOSAR Layered Architecture v4.0.3 for Tiva-C (TM4C123GH6PM)**
This is a header file Dio.h for the TM4C123GH6PM microcontroller - DIO Driver. This DIO Driver is based on the AUTOSAR layered architecture v4.0.3 and provides APIs for initializing the DIO Driver, reading and writing a single channel, reading and writing a port, reading and writing a channel group, flipping a channel, and getting the version information.

# **Installation**
This header file Dio.h should be included in your project's source code directory.

# **Usage**
1.Include Dio.h header file in your source code.
2.Initialize the DIO Driver using Dio_Init() function with a pointer to a configuration structure of type Dio_ConfigType.
3.Read or write a single channel using Dio_ReadChannel() and Dio_WriteChannel() functions with the channel number and the desired level.
4.Read or write a port using Dio_ReadPort() and Dio_WritePort() functions with the port number and the desired level.
5.Read or write a channel group using Dio_ReadChannelGroup() and Dio_WriteChannelGroup() functions with the channel group structure and the desired level.
6.Flip a channel using Dio_FlipChannel() function with the channel number.
7. Get the version information of the DIO Driver using Dio_GetVersionInfo() function.

# **Configuration**
This DIO Driver doesn't have a configuration tool, so the symbolic names of each DIO channel in the microcontroller must be defined in the source code by the user. The user also needs to configure the Dio_ConfigType structure to initialize the DIO Driver with the desired channels' direction.

# **API Service Id Macros**
- DIO_READ_CHANNEL_SID: service ID for reading a single channel.
- DIO_WRITE_CHANNEL_SID: service ID for writing a single channel.
- DIO_READ_PORT_SID: service ID for reading a port.
- DIO_WRITE_PORT_SID: service ID for writing a port.
- DIO_READ_CHANNEL_GROUP_SID: service ID for reading a channel group.
- DIO_WRITE_CHANNEL_GROUP_SID: service ID for writing a channel group.
- DIO_GET_VERSION_INFO_SID: service ID for getting version info.
- DIO_INIT_SID: service ID for initializing the DIO Driver.
- DIO_FLIP_CHANNEL_SID: service ID for flipping a channel.

# **DET Error Codes**
DIO_E_PARAM_INVALID_CHANNEL_ID: DET code for invalid channel ID requested.
DIO_E_PARAM_CONFIG: DET code for Dio_Init() service called with a NULL pointer parameter.
DIO_E_PARAM_INVALID_PORT_ID: DET code for invalid port ID requested.
DIO_E_PARAM_INVALID_GROUP: DET code for invalid channel group requested.
DIO_E_PARAM_POINTER: DET code for APIs called with a Null Pointer.
DIO_E_UNINIT: DET code for API service called without module initialization.

# **Data Types**
- Dio_ChannelType: data type for the symbolic name of a DIO channel.
- Dio_PortType: data type for the symbolic name of a DIO port.
- Dio_LevelType: data type for the level of a DIO channel.
- Dio_PortLevelType: data type for the level of a DIO port.
- Dio_ChannelGroupType: structure for a DIO channel group.
- Dio_ConfigChannel: structure to configure each individual channel.
- Dio_ConfigType: structure that is required for initialization API.
- Std_VersionInfoType: standard version information type.

# **Version Information**
- Module Version: 1.0.0
- AUTOSAR Version: 4.0.3
- Software Version:
    - Major Version: 1
    - Minor Version: 0
    - Patch Version: 0

# **Credits**
This DIO Driver header file was created by Belal Mohamed.