---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046407"
---
# Stop-AzureSiteRecoveryJob

## SYNOPSIS
사이트 복구 작업을 중지 합니다.

## 구문과

### ByObject (기본값)
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 중지 합니다.

## 예제의

### 예제 1: 모든 작업 중지
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

첫 번째 명령은 **AzureSiteRecoveryJob** cmdlet을 사용 하 여 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 작업을 가져온 다음 결과를 $Jobs 변수에 저장 합니다.

두 번째 명령은 $Jobs에 지정 된 작업을 중지 합니다.

## 변수

### -Id
중지할 작업의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -작업
중지할 작업을 지정 합니다.

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureSiteRecoveryJob](./Get-AzureSiteRecoveryJob.md)

[다시 시작-AzureSiteRecoveryJob](./Restart-AzureSiteRecoveryJob.md)

[이력서-AzureSiteRecoveryJob](./Resume-AzureSiteRecoveryJob.md)


