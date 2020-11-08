---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 22E8CB18-8CDD-4992-AB81-E1BB400E6BC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 294e931529b7de939a6a5c20181d48b18da1e892
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046277"
---
# Get-AzureVNetGatewayDiagnostics

## SYNOPSIS
가상 네트워크 게이트웨이에 대 한 진단의 현재 상태를 가져옵니다.

## 구문과

```
Get-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-Azurevnet2| 진단** cmdlet은 가상 네트워크 게이트웨이에 대 한 진단의 현재 상태를 가져옵니다.
Blob (binary large object)가 **시작-AzureVNetGatewayDiagnostics 진단** 유틸리티에서 이전 진단 세션을 저장 한 경우이 cmdlet은 해당 cmdlet이 진단 세션을 저장 한 BLOB의 URL도 반환 합니다.

## 예제의

## 변수

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
이 cmdlet이 진단 프로그램을 제공 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.

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

[Start-Azurevnet2| 진단](./Start-AzureVNetGatewayDiagnostics.md)

[중지-Azurevnet2| 진단](./Stop-AzureVNetGatewayDiagnostics.md)


