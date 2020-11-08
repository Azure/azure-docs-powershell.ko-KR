---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B7E2561D-0FE8-4B34-9188-E89AA0B5C9DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: dce79fc891018c3100140581e89639dbc76b543d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046276"
---
# Get-AzureVNetGatewayIPsecParameters

## SYNOPSIS
가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 IPsec 매개 변수를 가져옵니다.

## 구문과

```
Get-AzureVNetGatewayIPsecParameters -VNetName <String> -LocalNetworkSiteName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-Azurevnet2| 매개 변수** cmdlet은 가상 네트워크 게이트웨이와 로컬 네트워크 사이트 간 연결에 대 한 현재 IPsec (인터넷 프로토콜 보안) 및 IKE (Internet Key Exchange) 매개 변수를 가져옵니다.

## 예제의

## 변수

### -LocalNetworkSiteName
가상 네트워크 게이트웨이에 연결 하는 로컬 네트워크 사이트의 이름을 지정 합니다.

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -VNetName
이 cmdlet이 연결에 대 한 IPsec 매개 변수를 가져오는 가상 네트워크를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Set-Azurevnet2| 매개 변수](./Set-AzureVNetGatewayIPsecParameters.md)


