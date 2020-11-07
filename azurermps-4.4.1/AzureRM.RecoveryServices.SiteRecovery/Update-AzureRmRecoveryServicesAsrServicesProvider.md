---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: b1a68b3500f28e7a72c5d62996e0c62dc00107d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703644"
---
# Update-AzureRmRecoveryServicesAsrServicesProvider

## SYNOPSIS
Azure Site Recovery 서비스 공급자 로부터 받은 정보를 새로 고칩니다 (서버 새로 고침).

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmRecoveryServicesAsrServicesProvider -InputObject <ASRRecoveryServicesProvider> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**업데이트 AzureRmRecoveryServicesAsrServicesProvider** Cmdlet은 Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.
이 cmdlet을 사용 하 여 복구 서비스 공급자 로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.

## 예제의

### 예제 1
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrServicesProvider -ServicesProvider $ServicesProvider
```

지정 된 ASR services 공급자에서 정보를 새로 고치는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다. 

## 변수

### -InputObject
입력 개체: 정보가 업데이트 되는 서버를 식별 하는 ASR 서비스 공급자 (asr services provider) 개체를 지정 합니다 (새로 고침 됨).

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: ServicesProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### SiteRecovery. r m/RecoveryServices 공급자

## 출력

### System. 개체

## 상속자

## 관련 링크

[Get-AzureRmRecoveryServicesAsrServicesProvider](./Get-AzureRmRecoveryServicesAsrServicesProvider.md)

[제거-AzureRmRecoveryServicesAsrServicesProvider](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)
