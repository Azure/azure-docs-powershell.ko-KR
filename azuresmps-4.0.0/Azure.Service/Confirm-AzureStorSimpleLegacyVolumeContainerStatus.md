---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045700"
---
# Confirm-AzureStorSimpleLegacyVolumeContainerStatus

## SYNOPSIS
마이그레이션된 볼륨 컨테이너의 커밋 또는 롤백을 시작 합니다.

## 구문과

### MigrateSpecificContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleLegacyVolumeContainerStatus** cmdlet은 레거시 마이그레이션의 일부로 마이그레이션된 볼륨 컨테이너의 커밋 또는 롤백을 시작 합니다.
롤백은 기기를 원래 소유권으로 복원 합니다.
커밋은 대상 기기에 소유권을 할당 합니다.

## 예제의

### 예제 1: 특정 볼륨 컨테이너에서 커밋 작업 시작
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

이 명령은 지정 된 레거시 구성 ID에 대해 지정 된 볼륨 컨테이너에서 커밋 작업을 시작 합니다.
작업 상태를 확인 하려면 **AzureStorSimpleLegacyVolumeContainerStatus** cmdlet을 사용 합니다.

### 예제 2: 특정 볼륨 컨테이너에서 롤백 작업 시작
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

이 명령은 지정 된 레거시 구성 ID에 대해 지정 된 볼륨 컨테이너에서 롤백 작업을 시작 합니다.

### 예제 3: 모든 볼륨 컨테이너에서 커밋 작업 시작
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

이 명령은 모든 볼륨 컨테이너에서 지정 된 레거시 구성 ID에 대 한 커밋 작업을 시작 합니다.

### 예제 4: 모든 볼륨 컨테이너에서 롤백 작업 시작
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

이 명령은 모든 볼륨 컨테이너에서 지정 된 레거시 구성 ID에 대 한 롤백 작업을 시작 합니다.

## 변수

### -All
이 cmdlet이 가져온 구성 파일의 모든 볼륨 컨테이너에 대해 롤백 또는 커밋 작업을 시작 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LegacyConfigId
레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.

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

### -LegacyContainerNames
마이그레이션 계획이 적용 되는 볼륨 컨테이너 이름의 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MigrationOperation
이 cmdlet이 커밋 또는 롤백을 수행할지 여부를 지정 합니다.
유효한 값은 Commit 및 Rollback입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureStorSimpleLegacyVolumeContainerStatus](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


