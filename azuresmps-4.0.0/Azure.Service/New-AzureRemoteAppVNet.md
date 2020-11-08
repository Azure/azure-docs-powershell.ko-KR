---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: B6881AEC-7DFD-43F8-92A9-7AB56323B86F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 36476b34f74c44facf84ba2246afd0b6d8e49007
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045994"
---
# New-AzureRemoteAppVNet

## SYNOPSIS
Azure RemoteApp 가상 네트워크를 만듭니다.

## 구문과

```
New-AzureRemoteAppVNet -VNetName <String> -VirtualNetworkAddressSpace <String[]>
 -LocalNetworkAddressSpace <String[]> -DnsServerIpAddress <String[]> -VpnDeviceIpAddress <String>
 [-Location] <String> -GatewayType <GatewayType> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**새 AzureRemoteAppVNet** Cmdlet은 Azure RemoteApp 가상 네트워크를 만듭니다.

## 예제의

### 예제 1: 가상 네트워크 만들기
```
PS C:\> New-AzureRemoteAppVnet -VNetName "ContosoVNet" -DnsServerIpAddress "192.168.0.5" -LocalNetworkAddressSpace "192.168.0.0/24" -Location "Central US" -VirtualNetworkAddressSpace "10.10.0.0/24" -VpnDeviceIpAddress "131.107.33.200" -GatewayType StaticRouting

TrackingId

----------

b0ca9d1b-d1b9-4f24-9a08-5e021926587f
```

이 명령은 ContosoVNet 이라는 가상 네트워크를 만듭니다.

작업의 상태를 확인 하려면이 cmdlet이 반환 하는 추적 ID와 함께 **AzureRemoteAppOperationResult** cmdlet을 사용 합니다.

## 변수

### -DnsServerIpAddress
DNS 서버의 IPv4 주소 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -게이트웨이 종류
사용할 게이트웨이 라우팅 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 StaticRouting 또는 DynamicRouting.

```yaml
Type: GatewayType
Parameter Sets: (All)
Aliases: 
Accepted values: StaticRouting, DynamicRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -LocalNetworkAddressSpace
CIDR (클래스 없는 도메인간 라우팅) 표기법으로 로컬 네트워크 주소 공간을 지정 하는 문자열의 배열을 지정 합니다.
이 주소 공간은 *VirtualNetworkAddressSpace* 매개 변수에서 지정 하는 가상 네트워크 주소 공간과 중복 되 면 안 됩니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -위치
가상 네트워크를 만들 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -VirtualNetworkAddressSpace
CIDR 표기법으로 가상 네트워크 주소 공간을 지정 하는 문자열 배열을 지정 합니다.
이것은 개인 IP 주소 범위에 있어야 하며, *LocalNetworkAddressSpace* 매개 변수에서 지정 하는 로컬 네트워크 주소 공간과 중복 될 수 없습니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VNetName
Azure RemoteApp 가상 네트워크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VpnDeviceIpAddress
VPN (가상 개인 네트워크) 장치의 주소를 지정 합니다.
이것은 공공 주소 여야 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRemoteAppOperationResult](./Get-AzureRemoteAppOperationResult.md)

[Get-AzureRemoteAppVNet](./Get-AzureRemoteAppVNet.md)

[제거-AzureRemoteAppVNet](./Remove-AzureRemoteAppVNet.md)

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


