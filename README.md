# ICPF_DEMO
ICPF的周邊範例，WEBAPI範例，ICPF接口繼承範例，獲取ICPF中的設備數據範例，MQTT範例。

# 使用介紹
- Lib資料夾下存放一份ICPF.dll方便開發時引用，若是有更新版的核心請自行更換。
- ICPFWebAPI提供簡單的GET方法請求數據。
- PFC則是外部C#軟體需要調用可以透過這份插件，原理是WS底層透過網路方式傳遞數據(可跨平台，跨語言)，目前只針對C#端開發。
- Plugin.Mqtt提供了簡易的Broker架設，使用者可以輕鬆的建構一個Mqtt Broker，並且可以定時上報ICPF中設備的數據。(這裡的Mqtt庫使用[MqttNet](https://github.com/dotnet/MQTTnet))
- Plugin.PFCClient提供了PFC插件的連線邏輯，由外部PFC下指令Plugin.PFCClient接收並且返回相對應的資料。(這裡的Socket使用[TouchSocket](## DataType
| 類型   | 編號 |
| ------ | ---- |
| Bool   | 1    |
| Uint16 | 2    |
| Int16  | 3    |
| Uint32 | 4    |
| Int32  | 5    |
| Uint64 | 6    |
| Int64  | 7    |
| Float  | 8    |
| Double | 9    |
| String | 10   |

## CommunicationInterface

| 類型     | 編號 |
| -------- | ---- |
| Serial   | 1    |
| Ethernet | 2    |

## CommunicationProtocol
| 類型           | 編號 |
| -------------- | ---- |
| KvHost         | 1    |
| McProtocol_Tcp | 2    |
| Modbus_Tcp     | 3    |
| Vigor_Tcp      | 4    |
| SiemensS7Net   | 5    |))
- Plugin.A提供了如何讀取TagName數據
- Plugin.B提供了插件樣板(更詳細的可以直接去IPlugin介面詳看)

- PluginBase實作了IPlugin的大部分介面，開發者若是不想管那麼多可以直接繼承PluginBase，以下是結構圖:
- ![image](https://github.com/godchadigo/ICPF_DEMO/assets/19208239/598f112b-ef6b-409f-a64e-c238aa9bdb20)
- IPlugin是整體插件的接口，事件觸發由ICPF提供，以下是結構圖:
- ![image](https://github.com/godchadigo/ICPF_DEMO/assets/19208239/146696fe-a842-4ac5-8385-67e7f601ea16)



## DataType
| 類型   | 編號 |
| ------ | ---- |
| Bool   | 1    |
| Uint16 | 2    |
| Int16  | 3    |
| Uint32 | 4    |
| Int32  | 5    |
| Uint64 | 6    |
| Int64  | 7    |
| Float  | 8    |
| Double | 9    |
| String | 10   |

## CommunicationInterface

| 類型     | 編號 |
| -------- | ---- |
| Serial   | 1    |
| Ethernet | 2    |

## CommunicationProtocol
| 類型           | 編號 |
| -------------- | ---- |
| KvHost         | 1    |
| McProtocol_Tcp | 2    |
| Modbus_Tcp     | 3    |
| Vigor_Tcp      | 4    |
| SiemensS7Net   | 5    |
