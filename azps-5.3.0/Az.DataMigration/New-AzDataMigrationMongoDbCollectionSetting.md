---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98387563"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
mongoDb 마이그레이션에 따라 마이그레이션에 대한 컬렉션 설정을 만듭니다.

## 구문

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## 설명
New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리 및 삭제 동작을 지정하는 마이그레이션 설정 개체를 만듭니다.
cmdlet의 출력은 컬렉션의 이름과 설정 값이 있는 키 값 쌍입니다. 출력은 마이그레이션을 위한 데이터베이스 수준 설정을 어셈블하는 데 사용됩니다.

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

## PARAMETERS

### -Name
컬렉션의 이름

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
콤마로 구분된 Shard 키 목록입니다. mongoDb 대상의 경우 "shardKeyName:Order"의 공유 키 순서를 지정할 수 있습니다. 여기서 순서는 해시에 대해 1, -1 또는 비어 있습니다(예: "_id,email:-1").

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
전용 컬렉션 요청 단위 값입니다. 설정되지 않은 경우 해당 컬렉션은 공유 데이터베이스 RU를 사용합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### 없음

## 출력

### Microsoft.Azure.Commands.DataMigration.Models.MongoDbCollectionSetting>

## 참고 사항

## 관련 링크
