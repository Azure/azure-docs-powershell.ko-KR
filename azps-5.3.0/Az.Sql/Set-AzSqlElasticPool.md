---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492156"
---
# Set-AzSqlElasticPool

## SYNOPSIS
Azure SQL Database에서 탄력적 데이터베이스 풀의 속성을 수정합니다.

## 구문

### DtuBasedPool(기본값)
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### VcoreBasedPool
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명
**Set-AzSqlElasticPool** cmdlet은 Azure SQL Database의 탄력적 풀에 대한 속성을 설정합니다. 이 cmdlet은 풀당 *eDTU(Dtu),* 풀당 저장소 최대 *크기(StorageMB),* 데이터베이스당 최대 *eDTU(DatabaseDtuMax)* 및 데이터베이스당 최소 eDTU(DatabaseDtuMin)를 수정할 수 있습니다.
여러 매개 *변수(-Dtu, -DatabaseDtuMin 및 -DatabaseDtuMax)에는* 해당 매개 변수에 대한 유효한 값 목록에서 설정되는 값이 필요합니다. 예를 들어 표준 100 eDTU 풀에 대한 -DatabaseDtuMax는 10, 20, 50 또는 100으로만 설정할 수 있습니다.  유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)

## 예제

### 예제 1: 탄력적 풀에 대한 속성 수정
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

이 명령은 elasticpool01이라는 탄력적 풀에 대한 속성을 수정합니다. 이 명령은 탄력적 풀의 D2 수를 1000으로 설정하고 최소 및 최대 D2를 설정합니다.

### 예제 2: 탄력적 풀의 저장소 최대 크기 수정
```powershell
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

이 명령은 elasticpool01이라는 탄력적 풀에 대한 속성을 수정합니다. 이 명령은 탄력적 풀에 대한 최대 저장소를 2 TB로 설정합니다.

### 예제 3

Azure SQL Database에서 탄력적 데이터베이스 풀의 속성을 수정합니다. (자동Generated)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## PARAMETERS

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
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DatabaseDtuMax
풀의 단일 데이터베이스가 사용할 수 있는 최대 D2 수를 지정합니다.
유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
다른 버전에 대한 기본값은 다음과 같습니다.
- 기본.  5DUS
- 표준. 100 D2
- 프리미엄. 125DUS

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
탄력적 풀이 풀의 모든 데이터베이스에 보장하는 최소 D2 수를 지정합니다.
유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
기본값은 0입니다.

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
SqlAzure 데이터베이스가 풀에서 사용할 수 있는 최대 VCore 수입니다.

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
SqlAzure 데이터베이스가 풀에서 사용할 수 있는 최소 VCore 수입니다.

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
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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
탄력적 풀에 대한 공유 D2의 총 수를 지정합니다.
유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)
다른 버전에 대한 기본값은 다음과 같습니다.
- 기본. 100 D2
- 표준. 100 D2
- 프리미엄. 125DUS

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
탄력적 풀에 대한 Azure SQL 데이터베이스의 에디션을 지정합니다. 버전은 변경할 수 없습니다. 이 매개 변수에 허용되는 값은
- 없음
- 기본
- 표준
- 프리미엄
- DataWarehouse
- 무료
- Stretch
- GeneralPurpose
- BusinessCritical

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

### -ElasticPoolName
탄력적 풀의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ResourceGroupName
탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.

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
탄력적 풀에 대한 저장소 제한(메가바이트)을 지정합니다. 자세한 내용은 다음 cmdlet을 New-AzSqlElasticPool 참조하세요.

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
이 cmdlet이 해시 테이블의 형태로 탄력적 풀과 연결되는 키-값 쌍의 사전을 지정합니다. 예를 들어: `@{key0="value0";"key 1"=$null;key2="value2"}`

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
Sql Azure 탄력적 풀에 대한 총 공유 Vcore 수입니다.

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ZoneRedundant
Azure Sql 탄력적 풀과 연결하기 위해 영역 중복

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel

## 참고 사항

## 관련 링크

[Get-AzSqlElasticPool](./Get-AzSqlElasticPool.md)

[Get-AzSqlElasticPoolActivity](./Get-AzSqlElasticPoolActivity.md)

[Get-AzSqlElasticPoolDatabase](./Get-AzSqlElasticPoolDatabase.md)

[New-AzSqlElasticPool](./New-AzSqlElasticPool.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)
