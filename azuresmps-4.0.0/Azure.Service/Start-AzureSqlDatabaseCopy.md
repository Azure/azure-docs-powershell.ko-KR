---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7F07494-FBCA-4A77-92BF-E0A2D7ACCD21
online version: ''
schema: 2.0.0
ms.openlocfilehash: fc350cdf117ebbf72b023f64895f4c563e73566b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045845"
---
# Start-AzureSqlDatabaseCopy

## SYNOPSIS
Azure SQL 데이터베이스의 복사 작업을 시작 합니다.

## 구문과

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

## 설명은
**AzureSqlDatabaseCopy** cmdlet은 특정 Azure SQL Database에 대 한 일회성 복사 작업 또는 연속 복사 작업을 시작 합니다.
이 cmdlet은 트랜잭션이 아닙니다.

원래 데이터베이스는 원본 데이터베이스입니다.
사본은 보조 또는 대상 데이터베이스입니다.
연속 복사본의 경우 원본 및 대상 데이터베이스가 같은 서버에 상주할 수 없으며 원본 및 대상 데이터베이스를 호스트 하는 서버는 동일한 구독의 일부 여야 합니다.

*ContinuousCopy* 매개 변수를 지정 하지 않으면이 cmdlet은 원본 데이터베이스의 일회성 복사본을 만듭니다.
응답을 받으면 작업을 계속 진행할 수 있습니다.
Get-AzureSqlDatabaseCopy 또는 Get-AzureSqlDatabaseOperation cmdlet을 사용 하 여 작업을 모니터링할 수 있습니다.

*ContinuousCopy* 를 지정 하는 경우이 cmdlet은 원본 데이터베이스의 연속 복사본을 만듭니다.
응답을 받으면 작업이 진행 되 고 있는 것입니다.
**Get-AzureSqlDatabaseCopy** 또는 **get-AzureSqlDatabaseOperation** 를 사용 하 여 작업을 모니터링할 수 있습니다.

연속 복사본을 온라인 또는 오프 라인 데이터베이스로 만들 수 있습니다.
온라인 연속 복사본은 Azure SQL 데이터베이스의 활성 Geo-Replication를 구성 하는 데 사용 됩니다 https://azure.microsoft.com/en-us/documentation/articles/sql-database-geo-replication-overview/ .
오프 라인 연속 복사본은 Azure SQL 데이터베이스에 대 한 표준 Geo-Replication를 구성 하는 데 사용 됩니다 https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/ .

## 예제의

### 예제 1: 연속 데이터베이스 복사본 예약
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사본을 예약 합니다.
명령이 bk0b8kf658 라는 서버에 대상 데이터베이스를 만듭니다.

### 예제 2: 동일한 서버에서 일회성 복사본 만들기
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerDatabase "OrdersCopy"
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 일회성 복사본을 만듭니다.
이 명령은 같은 서버에 OrdersCopy 이라는 복사본을 만듭니다.

### 예제 3: 연속 오프 라인 데이터베이스 복사본 예약
```
PS C:\> Start-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf65" -ContinuousCopy -OfflineSecondary
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사본을 예약 합니다.
이 명령은 bk0b8kf658 이라는 서버에서 오프 라인 대상 데이터베이스를 만듭니다.

## 변수

### -ContinuousCopy
데이터베이스 복사본이 연속 복사본 (복제본 데이터베이스)이 됨을 나타냅니다.
동일한 서버 내에서는 연속 복사가 지원 되지 않습니다.
이 매개 변수를 지정 하지 않으면 일회성 복사가 수행 됩니다.
일회성 복사본의 경우 원본 및 파트너 데이터베이스가 같은 서버에 있어야 합니다.

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

### -데이터베이스
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.
이 매개 변수는 파이프라인 입력을 허용 합니다.

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
원본 데이터베이스의 이름을 지정 합니다.

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
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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
연속 복사본이 활성 복사본이 아닌 수동 복사본 임을 지정 합니다.
원본 데이터베이스가 Standard edition 데이터베이스인 경우이 매개 변수는 필수입니다.
이 매개 변수를 지정 하면 *ContinuousCopy* 도 지정 되어야 합니다.

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

### -데이터 데이터베이스
대상 데이터베이스의 이름을 지정 합니다.
*ContinuousCopy* 매개 변수를 지정 하는 경우 함께 사용할 *데이터베이스* 의 값은 원본 데이터베이스의 이름과 일치 해야 합니다.
*ContinuousCopy* 를 지정 하지 않으면 원본 데이터베이스 이름과 다를 수 있는 대상 데이터베이스의 이름을 지정 해야 합니다.

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

### -또는 서버
대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.
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

### -ServerName
원본 데이터베이스가 상주 하는 서버의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. * 데이터베이스

## 출력

### WindowsAzure. SqlDatabase. DatabaseCopy

## 상속자
* 인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다. 인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법의 예는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.
* 모니터링: 서버에서 활성 상태인 하나 이상의 연속 복사본 관계의 상태를 확인 하려면 **AzureSqlDatabaseCopy** cmdlet을 사용 합니다. 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인 하려면 **AzureSqlDatabaseOperation** cmdlet을 사용 합니다.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[데이터베이스 복사본 시작](https://msdn.microsoft.com/en-us/library/azure/dn509576.aspx)

[Azure SQL 데이터베이스 Cmdlet](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[중지-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


