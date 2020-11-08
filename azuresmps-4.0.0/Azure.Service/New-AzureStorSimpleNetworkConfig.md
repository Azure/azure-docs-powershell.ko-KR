---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 99D9EFA6-3506-4B0E-ACB5-C6EDBCB5A130
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d73ede26d4bd85a39f4baf2090e581300eafb1b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045515"
---
# New-AzureStorSimpleNetworkConfig

## SYNOPSIS
네트워크 구성 개체를 준비 합니다.

## 구문과

```
New-AzureStorSimpleNetworkConfig -InterfaceAlias <String> [-EnableIscsi <Boolean>] [-EnableCloud <Boolean>]
 [-Controller0IPv4Address <String>] [-Controller1IPv4Address <String>] [-IPv6Gateway <String>]
 [-IPv4Gateway <String>] [-IPv4Address <String>] [-IPv6Prefix <String>] [-IPv4Netmask <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleNetworkConfig** Cmdlet은 **AzureStorSimpleDevice** cmdlet에 전달할 네트워크 구성 개체를 준비 합니다.
Data0 인터페이스 에서만 *Controller0IPAddress* 매개 변수와 *Controller1IPAddress* 매개 변수를 설정 합니다.
Data0는 *Controller0IPAddress* , *Controller1IPAdress* , *enableiscsi* 의 세 가지 설정만 지원 합니다.

## 예제의

### 예제 1: Data0 인터페이스 구성
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
VERBOSE: ClientRequestId: 0621d220-a460-48ec-84ec-02a3a82f88b2_PS


IsIscsiEnabled         : True
IsCloudEnabled         : 
Controller0IPv4Address : 10.67.64.48
Controller1IPv4Address : 10.67.64.49
IPv6Gateway            : 
IPv4Gateway            : 
IPv4Address            : 
IPv6Prefix             : 
IPv4Netmask            : 
InterfaceAlias         : Data0

VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
```

이 명령은 Data0 인터페이스에 대 한 네트워크 구성을 만듭니다.
이 명령은 *Controller0IPv4Address* , *Controller1IPv4Address* 및 *enableiscsi* 매개 변수를 지정 합니다.
이 cmdlet은 이러한 세 가지 매개 변수에 대해서만 Data0를 구성할 수 있습니다.

### 예제 2: Data0 이외의 인터페이스를
```
PS C:\>New-AzureStorSimpleNetworkConfig -InterfaceAlias Data1 -EnableIscsi $True -EnableCloud $True -IPv6Gateway "db8:421e:9a8::a4:1c50" -IPv4Gateway "10.67.64.1" -IPv4Address "10.67.64.48" -IPv6Prefix "2001:db8:a::123/64" -IPv4Netmask "255.255.0.0"
VERBOSE: ClientRequestId: 3a15ff0e-b769-4329-9147-676b1e0acd7d_PS


IsIscsiEnabled         : True
IsCloudEnabled         : True
Controller0IPv4Address : 
Controller1IPv4Address : 
IPv6Gateway            : db8:421e:9a8::a4:1c50
IPv4Gateway            : 10.67.64.1
IPv4Address            : 10.67.64.48
IPv6Prefix             : 2001:db8:a::123/64
IPv4Netmask            : 255.255.0.0
InterfaceAlias         : Data1
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data1
```

이 명령은 Data1 인터페이스를 구성 합니다.

### 예제 3: 장치에 대 한 구성 수정
```
PS C:\>$NetworkConfigData0 = New-AzureStorSimpleNetworkConfig -InterfaceAlias Data0 -EnableIscsi $True -Controller0IPv4Address "10.67.64.48" -Controller1IPv4Address "10.67.64.49"
$OnlineDevice = @(Get-AzureStorSimpleDevice | Where { $_.Status -eq "Online"})[0]
$UpdatedDetails = Set-AzureStorSimpleDevice -DeviceId $OnlineDevice.DeviceId -StorSimpleNetworkConfig $NetworkConfigData0
VERBOSE: ClientRequestId: 0f163163-5ad0-4635-a7b5-870d47297f66_PS
VERBOSE: Successfully created a StorSimple Network Configuration for interface Data0
VERBOSE: ClientRequestId: 552e4a6c-7006-4015-a20b-9def6428a85e_PS
VERBOSE: ClientRequestId: f31cc84c-bc8a-404a-9da6-4670a7999e75_PS
VERBOSE: 1 StorSimple device found! 
VERBOSE: ClientRequestId: 545bc1a9-3c1b-4e50-89a6-9678aefe79e5_PS
VERBOSE: ClientRequestId: f114ad08-47f5-4fb8-8a01-1ea7f1ed1b98_PS
VERBOSE: About to configure the device : newDeviceName ! 
VERBOSE: ClientRequestId: 6afe7927-1c19-48d3-ac22-68148fd056b8_PS
VERBOSE: The task created for your Setup operation has completed successfully. 
VERBOSE: ClientRequestId: 467c142c-90da-4d75-82a4-c114afce953d_PS
VERBOSE: Successfully updated configuration for device newDeviceName with id 865e68f6-1e71-47b6-80d5-15d3a23bd2b0
```

첫 번째 명령은 Data0 인터페이스에 대 한 네트워크 구성을 만듭니다.
이 명령은 *Controller0IPv4Address* , *Controller1IPv4Address* 및 *enableiscsi* 매개 변수를 지정 합니다.
이 명령은 $NetworkConfigData 0 변수에 결과를 저장 합니다.

두 번째 명령은 **AzureStorSimpleDevice** Cmdlet 및 **Where-Object** core cmdlet을 사용 하 여 온라인 StorSimple 장치를 가져오고 $OnlineDevice 변수에 저장 합니다.

마지막 명령은 **Set-AzureStorSimpleDevice** cmdlet을 사용 하 여 지정 된 디바이스 ID의 장치에 대 한 구성을 수정 합니다.
명령에서 첫 번째 명령에 현재 cmdlet이 생성 하는 구성 개체를 사용 합니다.

## 변수

### -Controller0IPv4Address
컨트롤러 0에 대 한 IPv4 주소를 지정 합니다.
Data0 인터페이스에만이 매개 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Controller1IPv4Address
컨트롤러 1에 대 한 IPv4 주소를 지정 합니다.
Data0 인터페이스에만이 매개 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableCloud
인터페이스를 클라우드와 사용할 수 있는지 여부를 나타냅니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableIscsi
인터페이스에 대해 인터넷 SCSI (ISCSI)를 사용할지 여부를 나타냅니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -인터페이스 별칭
이 cmdlet이 설정을 제공 하는 인터페이스의 인터페이스 별칭을 지정 합니다.
유효한 값은 Data0부터 Data5입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Address
인터페이스에 대 한 IPv4 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Gateway
게이트웨이의 IPv4 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv4Netmask
인터페이스에 대 한 IPv4 넷마스크를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Gateway
인터페이스에 대 한 IPv6 게이트웨이를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPv6Prefix
인터페이스의 IPv6 접두사를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### NetworkConfig
이 cmdlet은 다음 속성을 포함 하는 NetworkConfig 개체를 반환 합니다. 

- **IsIscsiEnabled** ( **부울** ) 
- **Iscloudenabled** ( **Boolean** )
- **Controller0IPv4Address** ( **IPAddress** ) 
- **Controller1IPv4Address** ( **IPAddress** ) 
- **IPv6Gateway** ( **IPAddress** ) 
- **IPv4Gateway** ( **IPAddress** ) 
- **IPv4Address** ( **IPAddress** ) 
- **IPv6Prefix** ( **String** )
- **IPv4Netmask** ( **IPAddress** ) 
- **NetInterfaceId** ( **인터페이스 별칭** )

## 상속자

## 관련 링크

[Set-AzureStorSimpleDevice](./Set-AzureStorSimpleDevice.md)

[Get-AzureStorSimpleDevice](./Get-AzureStorSimpleDevice.md)


