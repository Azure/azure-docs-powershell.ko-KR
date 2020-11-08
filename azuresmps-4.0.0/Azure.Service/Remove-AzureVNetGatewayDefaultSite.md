---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 67260128-D57B-4587-BB61-2475703ABA66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38aca36799c57dd5a135af99e4b99ab713d2b1ca
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045489"
---
# Remove-AzureVNetGatewayDefaultSite

## SYNOPSIS
강제 터널링 트래픽에 대 한 기본 경로를 제거 합니다.

## 구문과

```
Remove-AzureVNetGatewayDefaultSite -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Remove-Azurevnet2| Defaultsite** cmdlet은 강제 터널링 트래픽을 위해 온-프레미스 사이트의 기본 경로를 제거 합니다.
이 cmdlet은 가상 네트워크의 Azure virtual 사설 네트워크 (VPN) 게이트웨이에서 경로를 제거 합니다.

## 예제의

### 예제 1: 기본 사이트에 대 한 경로 제거
```
PS C:\> Remove-AzureVNetGatewayDefaultSite -VnetName "ContosoVNet01"
```

이 명령은 ContosoVNet01 이라는 가상 네트워크의 VPN에서 기본 사이트에 대 한 경로를 제거 합니다.

## 변수

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
이 cmdlet은이 매개 변수에서 지정 하는 가상 네트워크의 VPN 게이트웨이에서 기본 경로를 제거 합니다.

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

[Set-Azurevnet게이트웨이 Defaultsite](./Set-AzureVNetGatewayDefaultSite.md)
