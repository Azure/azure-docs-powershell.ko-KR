---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: cc8881657c541a15ade44242ab5fb0e84c9bbab8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491608"
---
# <span data-ttu-id="936e5-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="936e5-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="936e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="936e5-102">SYNOPSIS</span></span>
<span data-ttu-id="936e5-103">기존 데이터베이스에 대한 보조 데이터베이스를 만들고 데이터 복제를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="936e5-104">구문</span><span class="sxs-lookup"><span data-stu-id="936e5-104">SYNTAX</span></span>

### <span data-ttu-id="936e5-105">DtuBasedDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="936e5-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="936e5-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="936e5-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="936e5-107">설명</span><span class="sxs-lookup"><span data-stu-id="936e5-107">DESCRIPTION</span></span>
<span data-ttu-id="936e5-108">**New-AzSqlDatabaseSecondary** cmdlet은 데이터베이스에 대한 지역 복제를 설정하는 데 사용할 Start-AzSqlDatabaseCopy cmdlet을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="936e5-109">주 데이터베이스에서 보조 데이터베이스로의 지역 복제 링크 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="936e5-110">예제</span><span class="sxs-lookup"><span data-stu-id="936e5-110">EXAMPLES</span></span>

### <span data-ttu-id="936e5-111">예제 1: 활성 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="936e5-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="936e5-112">예제 2: Active Geo-Replication 설정하고 원본 데이터베이스 이름과 다를 파트너 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="936e5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="936e5-113">PARAMETERS</span></span>

### <span data-ttu-id="936e5-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="936e5-114">-AllowConnections</span></span>
<span data-ttu-id="936e5-115">보조 Azure SQL 데이터베이스의 읽기 의도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="936e5-116">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="936e5-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="936e5-117">아니요</span><span class="sxs-lookup"><span data-stu-id="936e5-117">No</span></span>
- <span data-ttu-id="936e5-118">모두</span><span class="sxs-lookup"><span data-stu-id="936e5-118">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Replication.Model.AllowConnections
Parameter Sets: (All)
Aliases:
Accepted values: No, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="936e5-119">-AsJob</span></span>
<span data-ttu-id="936e5-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="936e5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="936e5-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="936e5-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="936e5-122">SQL 데이터베이스에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="936e5-123">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-123">Options are: Local, Zone and Geo.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Local, Zone, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="936e5-124">-DatabaseName</span></span>
<span data-ttu-id="936e5-125">주 데이터베이스 역할을 할 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-125">Specifies the name of the database to act as primary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936e5-126">-DefaultProfile</span></span>
<span data-ttu-id="936e5-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="936e5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="936e5-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="936e5-128">-LicenseType</span></span>
<span data-ttu-id="936e5-129">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="936e5-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="936e5-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="936e5-131">만들 보조 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="936e5-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936e5-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="936e5-133">이 cmdlet이 보조 데이터베이스를 할당하는 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="936e5-134">-PartnerServerName</span></span>
<span data-ttu-id="936e5-135">보조 역할을 할 Azure SQL 데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936e5-136">-ResourceGroupName</span></span>
<span data-ttu-id="936e5-137">이 cmdlet이 주 데이터베이스를 할당할 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="936e5-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="936e5-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="936e5-139">Azure Sql Database 보조 데이터베이스의 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-139">The compute generation of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedDatabase
Aliases: Family

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="936e5-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="936e5-141">보조 데이터베이스를 넣을 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="936e5-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="936e5-143">보조 데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedDatabase
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="936e5-144">-SecondaryType</span></span>
<span data-ttu-id="936e5-145">보조 데이터베이스인 경우 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="936e5-146">유효한 값은 Geo 및 Named입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-146">Valid values are Geo and Named.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Named, Geo

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="936e5-147">-SecondaryVCore</span></span>
<span data-ttu-id="936e5-148">Azure Sql Database 보조 데이터베이스의 Vcore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedDatabase
Aliases: Capacity

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="936e5-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="936e5-149">-ServerName</span></span>
<span data-ttu-id="936e5-150">기본 SQL Server 데이터베이스의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="936e5-151">-Tags</span><span class="sxs-lookup"><span data-stu-id="936e5-151">-Tags</span></span>
<span data-ttu-id="936e5-152">SQL 데이터베이스 복제 링크와 연결하기 위해 해시 테이블의 형태로 키-값 쌍을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="936e5-153">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="936e5-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="936e5-154">-Confirm</span><span class="sxs-lookup"><span data-stu-id="936e5-154">-Confirm</span></span>
<span data-ttu-id="936e5-155">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="936e5-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="936e5-156">-WhatIf</span></span>
<span data-ttu-id="936e5-157">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="936e5-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="936e5-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="936e5-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936e5-159">CommonParameters</span></span>
<span data-ttu-id="936e5-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="936e5-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936e5-161">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="936e5-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936e5-162">입력</span><span class="sxs-lookup"><span data-stu-id="936e5-162">INPUTS</span></span>

### <span data-ttu-id="936e5-163">System.String</span><span class="sxs-lookup"><span data-stu-id="936e5-163">System.String</span></span>

## <span data-ttu-id="936e5-164">출력</span><span class="sxs-lookup"><span data-stu-id="936e5-164">OUTPUTS</span></span>

### <span data-ttu-id="936e5-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="936e5-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="936e5-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="936e5-166">NOTES</span></span>

## <span data-ttu-id="936e5-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="936e5-167">RELATED LINKS</span></span>

[<span data-ttu-id="936e5-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="936e5-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="936e5-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="936e5-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="936e5-170">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="936e5-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
