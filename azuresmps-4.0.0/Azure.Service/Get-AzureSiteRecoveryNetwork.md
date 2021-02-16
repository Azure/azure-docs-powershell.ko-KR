---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 615D2C5D-AB31-45DB-9535-9B9C8E957322
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4a5701fc6308f1884bbf0237887a223a62a58669
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100411588"
---
# Get-AzureSiteRecoveryNetwork

## SYNOPSIS
현재 자격 증명 모음에 대한 Site Recovery에서 관리하는 네트워크에 대한 정보를 얻습니다.

## 구문

```
Get-AzureSiteRecoveryNetwork -Server <ASRServer> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명
**Get-AzureSiteRecoveryNetwork** cmdlet은 현재 Site Recovery 자격 증명 모음에 대한 Azure Site Recovery 네트워크에 대한 정보를 얻습니다.

## 예제

### 예제 1: 사이트 복구 네트워크 얻기
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> Get-AzureSiteRecoveryNetwork -Server $Servers[0]
Name                : phase2RecoveryVMNetwork
ID                  : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
FabricObjectID      : 7cfd636e-5cc2-4e01-873b-8a7aa4962341
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}

Name                : phase2PrimaryVMNetwork
ID                  : d903e2c6-3141-4cef-bfe1-04616cd43cbb
FabricObjectID      : d903e2c6-3141-4cef-bfe1-04616cd43cbb
ServerId            : 774859b0-1966-48cc-9df7-759c441b7a8c
Type                : NoIsolation
FabricType          : VMM
VmNetworkSubnetList : {}
```

첫 번째 명령 cmdlet은 **Get-AzureSiteRecoveryServer** cmdlet을 사용하여 현재 Azure Site Recovery 자격 증명 모음에 대한 서버를 얻습니다.
이 명령은 Site Recovery 서버를 $Servers 변수에 저장합니다.

두 번째 명령은 $Servers 배열의 첫 번째 서버에 대한 사이트 복구 네트워크를 얻습니다.

## PARAMETERS

### -Profile
이 cmdlet이 읽을 Azure 프로필을 지정합니다.
프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.

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

### -Server
Site Recovery 서버를 지정합니다.

```yaml
Type: ASRServer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

## 출력

## 참고 사항

## 관련 링크




