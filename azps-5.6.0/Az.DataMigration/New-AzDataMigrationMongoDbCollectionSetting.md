---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 817a4c8469d1d3652dade426857f88f9249f82b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966571"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
mongoDb 마이그레이션에 따라 마이그레이션에 대한 컬렉션 설정을 만듭니다.

## 구문

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## 설명
New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리 시간 및 삭제 동작을 지정하는 마이그레이션 설정 개체를 만듭니다.
cmdlet의 출력은 컬렉션의 이름과 설정 값이 있는 키 값 쌍입니다. 출력은 마이그레이션에 대한 데이터베이스 수준 설정을 어셈블하는 데 사용됩니다.

## 예제

### 예제 1
```
PS C:\> $x = New-AzDataMigrationMongoDbCollectionSetting -Name myCollection -TargetRequestUnit 1000 -CanDelete -ShardKey "_id:-1,age:1,name"
PS C:\> $x

Name         Setting
----         -------
myCollection Microsoft.Azure.Management.DataMigration.Models.MongoDbCollectionSettings

PS C:\> $x.Setting

CanDelete ShardKey                                                               TargetRUs
--------- --------                                                               ---------
     True Microsoft.Azure.Management.DataMigration.Models.MongoDbShardKeySetting      1000

```

## 매개 변수

### -Name
컬렉션 이름

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShardKey
콤마가 분리된 셰이드 키 목록입니다. mongoDb 대상의 경우 "shardKeyName:Order"의 샤드 키 순서(예: "_id,email:-1")를 해시에 대해 1, -1 또는 비어 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetRequestUnit
전용 컬렉션 요청 단위 값입니다. 설정하지 않은 경우 해당 컬렉션은 공유 데이터베이스 RU를 사용합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: RU

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CanDelete
대상 데이터를 삭제해야 하는지 여부, 스위치가 설정된 경우 마이그레이션 시 정리됩니다.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```


### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting>

## 참고 사항

## 관련 링크
