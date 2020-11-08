---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045773"
---
# Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan

## SYNOPSIS
마이그레이션 계획 만들기를 시작 합니다.

## 구문과

### MigrateSpecificContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### MigrateAllContainer
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet은 마이그레이션 계획 만들기를 시작 합니다.
마이그레이션 계획 만들기는 비동기입니다.
마이그레이션 계획의 상태를 보려면 **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet을 사용 합니다.

## 예제의

### 예제 1: 마이그레이션 계획 시작
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

이 명령은 OneSDKAzureCloud 이라는 레거시 컨테이너에 대 한 마이그레이션 계획 만들기를 시작 합니다.
이 명령은 계획의 상태에 대 한 메시지를 반환 하 고 최신 정보에 대 한 **AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet을 사용 합니다.

### 예제 2: 모든 볼륨 컨테이너에 대 한 마이그레이션 계획 시작
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

이 명령은 가져온 구성 파일의 모든 레거시 볼륨 컨테이너에 대 한 마이그레이션 계획 만들기를 시작 합니다.

## 변수

### -All
이 cmdlet이 가져온 구성 파일의 모든 볼륨 컨테이너에 대 한 마이그레이션 시간 예상을 시작 함을 나타냅니다.

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
마이그레이션 계획을 만들 볼륨 컨테이너 이름의 배열을 지정 합니다.

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

### 않아야

## 출력

### 이름
이 cmdlet은 기기에서 성공적으로 시작 된 마이그레이션 계획 작업의 상태를 반환 합니다.

## 상속자

## 관련 링크

[Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


