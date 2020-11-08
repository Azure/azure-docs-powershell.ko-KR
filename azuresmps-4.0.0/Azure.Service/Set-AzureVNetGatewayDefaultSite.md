---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: A34A2B01-A658-410E-8B68-98A6427DFC33
online version: ''
schema: 2.0.0
ms.openlocfilehash: 345d9048ea729b6fe954d2da5e01310be42c79ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046413"
---
# Set-AzureVNetGatewayDefaultSite

## SYNOPSIS
강제 터널링 트래픽에 대 한 기본 사이트를 설정 합니다.

## 구문과

```
Set-AzureVNetGatewayDefaultSite -VNetName <String> -DefaultSite <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Set-Azurevnet2| Defaultsite** cmdlet은 강제 터널링 트래픽을 위해 온-프레미스 사이트의 기본 경로를 설정 합니다.
이 명령은 가상 네트워크에 대 한 Azure VPN (가상 사설망) 게이트웨이에서 경로를 설정 합니다.

## 예제의

## 변수

### -DefaultSite
강제 터널링 트래픽에 대 한 온-프레미스 로컬 네트워크 사이트의 이름을 지정 합니다.

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

### -VNetName
가상 네트워크를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 강제 터널링 트래픽에 대 한 VPN 게이트웨이의 기본 경로를 설정 합니다.

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

[제거-Azurevnet2| Defaultsite](./Remove-AzureVNetGatewayDefaultSite.md)
