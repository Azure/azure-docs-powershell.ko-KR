---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationMongoDbCollectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationMongoDbCollectionSetting.md
ms.openlocfilehash: 4e0082d742aff54ba4d4b57d4e148e249ab8ecf7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305399"
---
# New-AzDataMigrationMongoDbCollectionSetting

## SYNOPSIS
MongoDb 마이그레이션에 따라 마이그레이션에 대 한 컬렉션 설정을 만듭니다.

## 구문과

```
New-AzDataMigrationMongoDbCollectionSetting -Name <Name> [-TargetRequestUnit <TargetRequestUnit>] [-CanDelete] [-ShardKey <ShardKey>]
```

## 설명은
New-AzDataMigrationMongoDbCollectionSetting cmdlet은 처리량 및 삭제 동작을 지정 하는 마이그레이션 설정 개체를 만듭니다.
출력 cmdlet은 컬렉션의 이름과 설정 값이 포함 된 키 값 쌍입니다. 출력이 마이그레이션에 대 한 데이터베이스 수준 설정을 어셈블하는 데 사용 됩니다.

## 예제의

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

## 변수

### -이름
컬렉션의 이름입니다.

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
샤 드 키의 쉼표로 구분 된 목록입니다. MongoDb 대상의 경우 "ShardKeyName: Order"의 샤 드 키 순서를 지정할 수 있으며, 여기서 "_id, 전자 메일:-1"과 같이, 해시에 대해 order가 1,-1 이거나 비어 있습니다.

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
전용 컬렉션 요청 단위 값입니다. 설정 하지 않은 경우 해당 컬렉션은 공유 데이터베이스를 사용 합니다.

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
대상 데이터를 삭제 해야 하는지 여부, 스위치가 설정 된 경우 마이그레이션하는 동안 정리 됩니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### DataMigration를 MongoDbCollectionSetting>.

## 상속자

## 관련 링크
