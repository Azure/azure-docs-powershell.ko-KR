---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35e29655e8447644b6c5449309424595e45ca187
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100413067"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Azure SQL 데이터베이스의 복사 작업을 시작합니다.

## 구문

### ByInputObject
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByInputObjectContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseName
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 -PartnerDatabase <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabaseNameContinuous
```
Start-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> -PartnerServer <String>
 [-PartnerDatabase <String>] [-ContinuousCopy] [-OfflineSecondary] [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Start-AzureSqlDatabaseCopy** cmdlet은 특정 Azure SQL Database의 일회성 복사 작업 또는 연속 복사 작업을 시작합니다.
이 cmdlet은 트랜잭션이 아니며

원본 데이터베이스는 원본 데이터베이스입니다.
복사본은 보조 데이터베이스 또는 대상 데이터베이스입니다.
연속 복사의 경우 원본 및 대상 데이터베이스는 동일한 서버에 있을 수 없습니다. 원본 및 대상 데이터베이스를 호스트하는 서버는 동일한 구독의 일부가 되어야 합니다.

*ContinuousCopy* 매개 변수를 지정하지 않으면 이 cmdlet은 원본 데이터베이스의 일회성 복사본을 만듭니다.
응답을 수신하면 작업이 계속 진행 중일 수 있습니다.
Get-AzureSqlDatabaseCopy cmdlet을 사용하여 작업을 Get-AzureSqlDatabaseOperation 있습니다.

*ContinuousCopy를 지정하는* 경우 이 cmdlet은 원본 데이터베이스의 연속 복사본을 만듭니다.
응답을 수신하면 작업이 진행 중입니다.
**Get-AzureSqlDatabaseCopy** 또는 **Get-AzureSqlDatabaseOperation을** 사용하여 작업을 모니터링할 수 있습니다.

연속 복사본을 온라인 또는 오프라인 데이터베이스로 만들 수 있습니다.
온라인 연속 복사는 Azure Geo-Replication Database에 대한 Active SQL 구성하는 데 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ 사용됩니다.
오프라인 연속 복사는 Azure SQL Database에 대한 표준 Geo-Replication 구성하는 데 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ 사용됩니다.

## 예제

### 예제 1: 연속 데이터베이스 복사 예약
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사본을 예약합니다.
이 명령은 bk0b8kf658이라는 서버에 대상 데이터베이스를 만듭니다.

### 예제 2: 동일한 서버에 일회성 복사본 만들기
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

이 명령은 lpqd0zbr8y라는 서버에 주문이라는 데이터베이스의 일회성 복사본을 만듭니다.
이 명령은 동일한 서버에 OrdersCopy라는 복사본을 만듭니다.

### 예제 3: 연속 오프라인 데이터베이스 복사 예약
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사본을 예약합니다.
이 명령은 bk0b8kf658이라는 서버에 오프라인 대상 데이터베이스를 만듭니다.

## PARAMETERS

### -ContinuousCopy
데이터베이스 복사본이 연속 복사(복제본 데이터베이스)를 나타냅니다.
연속 복사는 동일한 서버 내에서 지원되지 않습니다.
이 매개 변수를 지정하지 않으면 일회성 복사본이 수행됩니다.
일회성 복사본의 경우 원본 및 파트너 데이터베이스가 동일한 서버에 있어야 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Database
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.
이 매개 변수는 파이프라인 입력을 허용합니다.

```yaml
Type: Database
Parameter Sets: ByInputObject, ByInputObjectContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
원본 데이터베이스의 이름을 지정합니다.

```yaml
Type: String
Parameter Sets: ByDatabaseName, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OfflineSecondary
연속 복사본이 활성 복사본이 아닌 수동 복사본으로 지정합니다.
원본 데이터베이스가 Standard Edition 데이터베이스인 경우 이 매개 변수가 필요합니다.
이 매개 변수를 지정하는 경우 *ContinuousCopy도* 지정해야 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerDatabase
대상 데이터베이스의 이름을 지정합니다.
*ContinuousCopy* 매개 변수를 지정하는 경우 *PartnerDatabase의* 값은 원본 데이터베이스의 이름과 일치해야 합니다.
*ContinuousCopy를* 지정하지 않으면 원본 데이터베이스 이름과 다를 수 있는 대상 데이터베이스의 이름을 지정해야 합니다.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PartnerServer
대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.
이 서버는 원본 데이터베이스 서버와 동일한 Azure 구독에 있어야 합니다.

```yaml
Type: String
Parameter Sets: ByInputObject, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObjectContinuous, ByDatabaseNameContinuous
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
이 cmdlet이 읽을 Azure 프로필을 지정합니다.
프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.

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

### -ServerName
원본 데이터베이스가 있는 서버의 이름을 지정합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 출력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## 참고 사항
* 인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다. 인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 New-AzureSqlDatabaseServerContext 참조하세요.
* 모니터링: 서버에서 활성 상태인 하나 이상의 연속 복사 관계의 상태를 확인하기 위해 **Get-AzureSqlDatabaseCopy** cmdlet을 사용하세요. 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인하기 위해 **Get-AzureSqlDatabaseOperation** cmdlet을 사용하세요.

## 관련 링크

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[데이터베이스 복사 시작](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


