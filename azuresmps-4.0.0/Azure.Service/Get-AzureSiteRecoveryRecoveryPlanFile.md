---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045583"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## SYNOPSIS
Azure Site Recovery 계획을 XML 형식으로 다운로드 합니다.

## 구문과

### ByRPObject (기본값)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSiteRecoveryRecoveryPlanFile** Cmdlet은 Azure Site Recovery 계획을 XML 형식으로 다운로드 합니다.
이 파일을 사용 하 여 복구 계획을 업데이트 한 다음 사이트 복구 서버로 업로드할 수 있습니다.

복구 계획은 장애 조치와 복구를 위해 그룹의 가상 컴퓨터를 수집 합니다.

## 예제의

### 예제 1: 복구 계획 파일 가져오기
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

이 명령은 **AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 하 여 복구 계획을 얻은 다음 $RecoveryPlan 변수에 저장 합니다.

두 번째 명령은 **GetAzureSiteRecoveryRecoveryPlanFile** cmdlet을 사용 하 여 $RecoveryPlan에서 사이트 복구 계획 XML 파일을 가져옵니다.
명령은 지정 된 경로에 XML 파일을 저장 합니다.

## 변수

### -Id
가져올 복구 계획의 ID를 지정 합니다.

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

### -Path
복구 계획 XML 파일을 저장할 전체 경로를 지정 합니다.

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

### -RecoveryPlan
복구 계획을 가져올 **Asrrecoveryplan** 개체를 지정 합니다.
**Asrrecoveryplan** 개체를 얻으려면 **Get-AzureSiteRecoveryRecoveryPlan** cmdlet을 사용 합니다.

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
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

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


