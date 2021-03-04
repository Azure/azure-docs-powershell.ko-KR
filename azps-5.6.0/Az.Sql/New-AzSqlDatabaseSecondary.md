---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: 983291eda139793b2cc5d0fe5cd213b5d8cd69a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982027"
---
# <span data-ttu-id="22e28-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="22e28-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="22e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22e28-102">SYNOPSIS</span></span>
<span data-ttu-id="22e28-103">기존 데이터베이스에 대한 보조 데이터베이스를 만들고 데이터 복제를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="22e28-104">구문</span><span class="sxs-lookup"><span data-stu-id="22e28-104">SYNTAX</span></span>

### <span data-ttu-id="22e28-105">DtuBasedDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="22e28-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22e28-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="22e28-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>]
 [-BackupStorageRedundancy <String>] [-SecondaryType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22e28-107">설명</span><span class="sxs-lookup"><span data-stu-id="22e28-107">DESCRIPTION</span></span>
<span data-ttu-id="22e28-108">**New-AzSqlDatabaseSecondary** cmdlet은 데이터베이스의 지역 복제를 설정하는 데 Start-AzSqlDatabaseCopy cmdlet을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="22e28-109">기본 데이터베이스에서 보조 데이터베이스로 지역 복제 링크 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="22e28-110">예제</span><span class="sxs-lookup"><span data-stu-id="22e28-110">EXAMPLES</span></span>

### <span data-ttu-id="22e28-111">예제 1: 활성 Geo-Replication</span><span class="sxs-lookup"><span data-stu-id="22e28-111">Example 1: Establish Active Geo-Replication</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="22e28-112">예제 2: 활성 Geo-Replication 설정하고 파트너 데이터베이스 이름을 원본 데이터베이스 이름과 다르게 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-112">Example 2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="22e28-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="22e28-113">PARAMETERS</span></span>

### <span data-ttu-id="22e28-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="22e28-114">-AllowConnections</span></span>
<span data-ttu-id="22e28-115">보조 Azure 데이터베이스 데이터베이스의 읽기 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="22e28-116">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="22e28-117">아니요</span><span class="sxs-lookup"><span data-stu-id="22e28-117">No</span></span>
- <span data-ttu-id="22e28-118">모두</span><span class="sxs-lookup"><span data-stu-id="22e28-118">All</span></span>

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

### <span data-ttu-id="22e28-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22e28-119">-AsJob</span></span>
<span data-ttu-id="22e28-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="22e28-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22e28-121">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="22e28-121">-BackupStorageRedundancy</span></span>
<span data-ttu-id="22e28-122">백업 데이터베이스에 대한 백업을 저장하는 데 SQL 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-122">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="22e28-123">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-123">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="22e28-124">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="22e28-124">-DatabaseName</span></span>
<span data-ttu-id="22e28-125">기본 역할을 할 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-125">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="22e28-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22e28-126">-DefaultProfile</span></span>
<span data-ttu-id="22e28-127">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="22e28-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22e28-128">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="22e28-128">-LicenseType</span></span>
<span data-ttu-id="22e28-129">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-129">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="22e28-130">-PartnerDatabaseName</span><span class="sxs-lookup"><span data-stu-id="22e28-130">-PartnerDatabaseName</span></span>
<span data-ttu-id="22e28-131">만들 보조 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-131">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="22e28-132">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e28-132">-PartnerResourceGroupName</span></span>
<span data-ttu-id="22e28-133">이 cmdlet에서 보조 데이터베이스를 할당하는 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-133">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="22e28-134">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="22e28-134">-PartnerServerName</span></span>
<span data-ttu-id="22e28-135">보조 역할을 할 Azure SQL 데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-135">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="22e28-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22e28-136">-ResourceGroupName</span></span>
<span data-ttu-id="22e28-137">이 cmdlet에서 기본 데이터베이스를 할당하는 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-137">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="22e28-138">-SecondaryComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="22e28-138">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="22e28-139">Azure Sql Database 보조 컴퓨팅 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-139">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="22e28-140">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="22e28-140">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="22e28-141">보조 데이터베이스를 넣을 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-141">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="22e28-142">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="22e28-142">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="22e28-143">보조 데이터베이스에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-143">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="22e28-144">-SecondaryType</span><span class="sxs-lookup"><span data-stu-id="22e28-144">-SecondaryType</span></span>
<span data-ttu-id="22e28-145">보조 데이터베이스의 보조 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-145">The secondary type of the database if it is a secondary.</span></span>  <span data-ttu-id="22e28-146">유효한 값은 지역 및 명명입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-146">Valid values are Geo and Named.</span></span>

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

### <span data-ttu-id="22e28-147">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="22e28-147">-SecondaryVCore</span></span>
<span data-ttu-id="22e28-148">Azure Sql Database 보조의 Vcore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-148">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="22e28-149">-ServerName</span><span class="sxs-lookup"><span data-stu-id="22e28-149">-ServerName</span></span>
<span data-ttu-id="22e28-150">기본 데이터베이스의 SQL Server 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-150">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="22e28-151">-Tags</span><span class="sxs-lookup"><span data-stu-id="22e28-151">-Tags</span></span>
<span data-ttu-id="22e28-152">데이터베이스 복제 링크와 연결하기 위해 해시 테이블의 형태로 key-value 쌍을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-152">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="22e28-153">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="22e28-153">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22e28-154">-확인</span><span class="sxs-lookup"><span data-stu-id="22e28-154">-Confirm</span></span>
<span data-ttu-id="22e28-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22e28-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22e28-156">-WhatIf</span></span>
<span data-ttu-id="22e28-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22e28-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22e28-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22e28-159">CommonParameters</span></span>
<span data-ttu-id="22e28-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22e28-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22e28-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22e28-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22e28-162">입력</span><span class="sxs-lookup"><span data-stu-id="22e28-162">INPUTS</span></span>

### <span data-ttu-id="22e28-163">System.String</span><span class="sxs-lookup"><span data-stu-id="22e28-163">System.String</span></span>

## <span data-ttu-id="22e28-164">출력</span><span class="sxs-lookup"><span data-stu-id="22e28-164">OUTPUTS</span></span>

### <span data-ttu-id="22e28-165">Microsoft.Azure.Commands.Sql.복제.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="22e28-165">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="22e28-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22e28-166">NOTES</span></span>

## <span data-ttu-id="22e28-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22e28-167">RELATED LINKS</span></span>

[<span data-ttu-id="22e28-168">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="22e28-168">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="22e28-169">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="22e28-169">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="22e28-170">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="22e28-170">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
