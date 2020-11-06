---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 69A26BF3-7FE7-41ED-8C21-C8DC72D09615
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqlserverupgrade
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlServerUpgrade.md
ms.openlocfilehash: d33635cd3876a3426c3db96489d623d0a61f1d03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532599"
---
# Start-AzureRmSqlServerUpgrade

## SYNOPSIS
SQL 데이터베이스 서버의 업그레이드를 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Start-AzureRmSqlServerUpgrade -ServerVersion <String> [-ScheduleUpgradeAfterUtcDateTime <DateTime>]
 [-DatabaseCollection <RecommendedDatabaseProperties[]>]
 [-ElasticPoolCollection <UpgradeRecommendedElasticPoolProperties[]>] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmSqlServerUpgrade** Cmdlet은 Azure SQL 데이터베이스 서버 버전 11을 버전 12로 업그레이드 하기 시작 합니다.
Get-AzureRmSqlServerUpgrade cmdlet을 사용 하 여 업그레이드 진행률을 모니터링할 수 있습니다.

## 예제의

### 예제 1: 서버 업그레이드
```
PS C:\>Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0
ResourceGroupName               : ResourceGroup01
ServerName                      : Server01
ServerVersion                   : 12.0
ScheduleUpgradeAfterUtcDateTime : 
DatabaseCollection              :
```

이 명령은 리소스 그룹 TesourceGroup01에 할당 된 server01 이라는 서버를 업그레이드 합니다.

### 예제 2: 일정 시간 및 데이터베이스 권장 구성을 사용 하 여 서버 업그레이드
```
PS C:\>$ScheduleTime = (Get-Date).AddMinutes(5).ToUniversalTime()
PS C:\> $DatabaseMap = New-Object -TypeName Microsoft.Azure.Management.Sql.Models.RecommendedDatabaseProperties
PS C:\> $DatabaseMap.Name = "contosodb"
PS C:\> $DatabaseMap.TargetEdition = "Standard"
PS C:\> $DatabaseMap.TargetServiceLevelObjective = "S0"
PS C:\> Start-AzureRmSqlServerUpgrade -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ServerVersion 12.0 -ScheduleUpgradeAfterUtcDateTime $ScheduleTime -DatabaseCollection ($DatabaseMap)
```

첫 번째 명령은 Get-Date cmdlet을 사용 하 여 5 분 후에 시간을 만듭니다.
이 명령은 $ScheduleTime 변수에 날짜를 저장 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

두 번째 명령은 **RecommendedDatabaseProperties** 개체를 만든 다음이 개체를 변수 $DatabaseMap에 저장 합니다.

다음 세 개의 명령은 $DatabaseMap에 저장 된 개체의 속성에 값을 할당 합니다.

마지막 명령은 Server01 이라는 기존 서버를 버전 12.0으로 업그레이드 합니다.
가장 빠른 업그레이드 시간은 $ScheduleTime 변수에 지정 된 대로 명령을 실행 한 후 5 분입니다.
업그레이드 후 데이터베이스 contosodb는 표준 버전을 실행 하 고 서비스 수준 목표가 S0으로 사용 됩니다.

## 변수

### -DatabaseCollection
이 cmdlet에서 서버 업그레이드에 사용 하는 **RecommendedDatabaseProperties** 개체의 배열을 지정 합니다.

```yaml
Type: RecommendedDatabaseProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolCollection
서버 업그레이드에 사용할 **UpgradeRecommendedElasticPoolProperties** 개체의 배열을 지정 합니다.

```yaml
Type: UpgradeRecommendedElasticPoolProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
서버가 할당 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ScheduleUpgradeAfterUtcDateTime
빠른 시간을 **DateTime** 개체로 지정 하 여 서버를 업그레이드 합니다.
UTC (협정 세계시)로 ISO8601 형식으로 값을 지정 합니다.
자세한 내용은을 입력 `Get-Help Get-Date` 하세요.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
이 cmdlet이 업그레이드 하는 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerVersion
이 cmdlet에서 서버를 업그레이드할 버전을 지정 합니다.
유일 하 게 유효한 값은 12.0입니다.

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

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### AzureSqlServerUpgradeModel 업그레이드. 모델. m a.

## 상속자

## 관련 링크

[Get-AzureRmSqlServerUpgrade](./Get-AzureRmSqlServerUpgrade.md)

[중지-AzureRmSqlServerUpgrade](./Stop-AzureRmSqlServerUpgrade.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


