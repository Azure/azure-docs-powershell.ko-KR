---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970208"
---
# New-AzSqlElasticPool

## SYNOPSIS
데이터베이스의 탄력적 데이터베이스 풀을 SQL 만듭니다.

## 구문

### DtuBasedPool(기본값)
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### VcoreBasedPool
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명
**New-AzSqlElasticPool** cmdlet은 Azure SQL 데이터베이스 풀을 만듭니다.
여러 매개 *변수(-Dtu, -DatabaseDtuMin 및 -DatabaseDtuMax)에는* 설정되는 값이 해당 매개 변수에 대한 유효한 값 목록에서 설정되어 있어야 합니다. 예를 들어 표준 100 eDTU 풀의 -DatabaseDtuMax는 10, 20, 50 또는 100으로만 설정할 수 있습니다.  유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## 예제

### 예제 1: DTU 탄력적 풀 만들기

```powershell
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

이 명령은 ElasticPool01이라는 표준 서비스 계층에 탄력적 풀을 만듭니다. ResourceGroup01이라는 Azure 리소스 그룹에 할당된 server01이라는 서버는 탄력적 풀을 호스트합니다. 명령은 풀 및 풀의 데이터베이스에 대한 DTU 속성 값을 지정합니다.

### 예제 2: vCore 탄력적 풀 만들기

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

이 명령은 ElasticPool01이라는 GengeralPurpose 서비스 계층에 탄력적 풀을 만듭니다. ResourceGroup01이라는 Azure 리소스 그룹에 할당된 server01이라는 서버는 탄력적 풀을 호스트합니다. 명령은 풀 및 풀의 데이터베이스에 대한 vCore 속성 값을 지정합니다.

### 예제 3

데이터베이스의 탄력적 데이터베이스 풀을 SQL 만듭니다. (자동 재생)

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## 매개 변수

### -AsJob
백그라운드에서 cmdlet 실행

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeGeneration
할당할 계산 생성입니다.

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
풀의 단일 데이터베이스가 사용할 수 있는 DTUS(Database Throughput Units)의 최대 수를 지정합니다.
다른 버전에 대한 기본값은 다음과 같습니다.
- 기본. 5DUS
- 표준입니다. 100 DUS
- 프리미엄입니다. 125 DTUS 유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMin
탄력적 풀이 풀의 모든 데이터베이스에 보장하는 최소 DUS 수를 지정합니다.
기본값은 0(0)입니다.
유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMax
풀에서 사용할 수 있는 SqlAzure Database의 최대 VCore 수입니다.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseVCoreMin
풀에서 사용할 수 있는 SqlAzure 데이터베이스의 최소 VCore 수입니다.

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Dtu
탄력적 풀에 대한 공유 DUS의 총 수를 지정합니다.
다른 버전에 대한 기본값은 다음과 같습니다.
- 기본.
100 DUS
- 표준입니다.
100 DUS
- 프리미엄입니다.
125 DTUS 유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Edition
탄력적 풀에 사용되는 Azure SQL 데이터베이스의 에디션을 지정합니다.
이 매개 변수에 대해 허용되는 값은 다음입니다.
- 없음
- 기본
- 표준
- 프리미엄
- DataWarehouse
- 무료
- 스트레치
- GeneralPurpose
- BusinessCritical

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ElasticPoolName
이 cmdlet이 만드는 탄력적 풀의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LicenseType
Azure Sql 데이터베이스에 대한 라이선스 유형입니다.

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

### -MaintenanceConfigurationId
탄력적 풀에 대한 SQL 구성 ID입니다.

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

### -ResourceGroupName
이 cmdlet에서 탄력적 풀을 할당하는 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServerName
탄력적 풀을 호스트하는 서버의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageMB
탄력적 풀에 대한 저장소 제한(메가바이트)을 지정합니다. 이 매개 변수를 지정하지 않으면 이 cmdlet은 *Dtu* 매개 변수의 값에 따라 달라지는 값을 계산합니다.
가능한 [값에 대한 eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 및 저장소 제한을 참조하세요.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tags
이 cmdlet이 탄력적 풀과 연결되는 해시 테이블의 형태로 Key-value 쌍의 사전을 지정합니다. 예: @{key0="value0";key1=$null;key2="value2"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VCore
Sql Azure Elastic Pool에 대한 총 공유 Vcores 수입니다.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Azure Sql Elastic Pool과 연결되는 영역 중복성

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -확인
cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.
cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel

## 참고 사항

## 관련 링크

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[Remove-AzSqlElasticPool](./Remove-AzSqlElasticPool.md)

[Set-AzSqlElasticPool](./Set-AzSqlElasticPool.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
