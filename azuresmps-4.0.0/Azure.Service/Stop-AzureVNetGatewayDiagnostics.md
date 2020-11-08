---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 706CBF65-C796-4525-BAEB-AAFAD44C0464
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37c2ce3b32d23f7c5bb682d2116de84cc90f047
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046019"
---
# Stop-AzureVNetGatewayDiagnostics

## SYNOPSIS
실행 중인 VPN 게이트웨이 진단 세션을 중지 합니다.

## 구문과

```
Stop-AzureVNetGatewayDiagnostics -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Stop-Azurevnet2| 진단** cmdlet은 실행 중인 가상 개인 네트워크 (VPN) 게이트웨이 진단 세션을 중지 합니다.
이 명령은 진단 세션의 결과를 시작 하 고 **Azurevnet2| 진단** cmdlet이 지정 하는 저장소 계정에 저장 합니다.

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
이 cmdlet이 진단을 중지 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.

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

[Get-Azurevnet게이트웨이 진단](./Get-AzureVNetGatewayDiagnostics.md)

[Start-Azurevnet2| 진단](./Start-AzureVNetGatewayDiagnostics.md)


