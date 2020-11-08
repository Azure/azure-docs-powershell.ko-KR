---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BEE99039-35F7-4E9D-9308-090EAE68292D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseSecondary.md
ms.openlocfilehash: f7dbffffe9a51d35ced8861894373322898fd0f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042468"
---
# <span data-ttu-id="8d4b5-101">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d4b5-101">New-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="8d4b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="8d4b5-103">기존 데이터베이스에 대 한 보조 데이터베이스를 만들고 데이터 복제를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-103">Creates a secondary database for an existing database and starts data replication.</span></span>

## <span data-ttu-id="8d4b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8d4b5-104">SYNTAX</span></span>

### <span data-ttu-id="8d4b5-105">DtuBasedDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="8d4b5-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-SecondaryServiceObjectiveName <String>]
 [-SecondaryElasticPoolName <String>] [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 [-LicenseType <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d4b5-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="8d4b5-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseSecondary [-DatabaseName] <String> [-Tags <Hashtable>] -PartnerResourceGroupName <String>
 -PartnerServerName <String> [-PartnerDatabaseName <String>] [-AllowConnections <AllowConnections>] [-AsJob]
 -SecondaryComputeGeneration <String> -SecondaryVCore <Int32> [-LicenseType <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8d4b5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8d4b5-107">DESCRIPTION</span></span>
<span data-ttu-id="8d4b5-108">데이터베이스에 대 한 지리적 복제를 설정 하는 데 사용 되는 **AzSqlDatabaseSecondary** cmdlet은 Start-AzSqlDatabaseCopy cmdlet을 대체 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-108">The **New-AzSqlDatabaseSecondary** cmdlet replaces the Start-AzSqlDatabaseCopy cmdlet when used for setting up geo-replication for a database.</span></span> <span data-ttu-id="8d4b5-109">기본 데이터베이스에서 보조 데이터베이스로 지역 복제 링크 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-109">It returns the geo-replication link object from the primary to the secondary database.</span></span>

## <span data-ttu-id="8d4b5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8d4b5-110">EXAMPLES</span></span>

### <span data-ttu-id="8d4b5-111">1: 활성 Geo-Replication 설정</span><span class="sxs-lookup"><span data-stu-id="8d4b5-111">1: Establish Active Geo-Replication</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -AllowConnections "All"
```

### <span data-ttu-id="8d4b5-112">2: 활성 Geo-Replication 설정 하 고 원본 데이터베이스 이름과 다른 파트너 데이터베이스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-112">2: Establish Active Geo-Replication and specify the partner database name to be different than the source database name</span></span>
```
$database = Get-AzSqlDatabase -DatabaseName $databasename -ResourceGroupName $primaryresourcegroupname -ServerName $primaryservername
$database | New-AzSqlDatabaseSecondary -PartnerResourceGroupName $secondaryresourcegroupname -PartnerServerName $secondaryservername -PartnerDatabaseName $secondarydatabasename -AllowConnections "All"
```

## <span data-ttu-id="8d4b5-113">변수</span><span class="sxs-lookup"><span data-stu-id="8d4b5-113">PARAMETERS</span></span>

### <span data-ttu-id="8d4b5-114">-AllowConnections</span><span class="sxs-lookup"><span data-stu-id="8d4b5-114">-AllowConnections</span></span>
<span data-ttu-id="8d4b5-115">보조 Azure SQL 데이터베이스의 읽기 의도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-115">Specifies the read intent of the secondary Azure SQL Database.</span></span>
<span data-ttu-id="8d4b5-116">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8d4b5-117">아니요</span><span class="sxs-lookup"><span data-stu-id="8d4b5-117">No</span></span>
- <span data-ttu-id="8d4b5-118">모든</span><span class="sxs-lookup"><span data-stu-id="8d4b5-118">All</span></span>

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

### <span data-ttu-id="8d4b5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d4b5-119">-AsJob</span></span>
<span data-ttu-id="8d4b5-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8d4b5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8d4b5-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-121">-DatabaseName</span></span>
<span data-ttu-id="8d4b5-122">기본 역할을 할 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-122">Specifies the name of the database to act as primary.</span></span>

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

### <span data-ttu-id="8d4b5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d4b5-123">-DefaultProfile</span></span>
<span data-ttu-id="8d4b5-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8d4b5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8d4b5-125">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="8d4b5-125">-LicenseType</span></span>
<span data-ttu-id="8d4b5-126">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-126">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="8d4b5-127">-단일 Databasename</span><span class="sxs-lookup"><span data-stu-id="8d4b5-127">-PartnerDatabaseName</span></span>
<span data-ttu-id="8d4b5-128">만들 보조 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-128">The name of the secondary database to create.</span></span>

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

### <span data-ttu-id="8d4b5-129">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-129">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8d4b5-130">이 cmdlet이 보조 데이터베이스를 할당 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-130">Specifies the name of the Azure Resource Group to which this cmdlet assigns the secondary database.</span></span>

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

### <span data-ttu-id="8d4b5-131">-(-)-(서버 이름)</span><span class="sxs-lookup"><span data-stu-id="8d4b5-131">-PartnerServerName</span></span>
<span data-ttu-id="8d4b5-132">보조 역할을 할 Azure SQL 데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-132">Specifies the name of the Azure SQL database server to act as secondary.</span></span>

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

### <span data-ttu-id="8d4b5-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-133">-ResourceGroupName</span></span>
<span data-ttu-id="8d4b5-134">이 cmdlet이 기본 데이터베이스를 할당 하는 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-134">Specifies the name of the Azure Resource Group to which this cmdlet assigns the primary database.</span></span>

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

### <span data-ttu-id="8d4b5-135">-Secondary고 Egeneration</span><span class="sxs-lookup"><span data-stu-id="8d4b5-135">-SecondaryComputeGeneration</span></span>
<span data-ttu-id="8d4b5-136">Azure Sql 데이터베이스 보조의 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-136">The compute generation of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="8d4b5-137">-SecondaryElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-137">-SecondaryElasticPoolName</span></span>
<span data-ttu-id="8d4b5-138">보조 데이터베이스를 추가할 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-138">Specifies the name of the elastic pool in which to put the secondary database.</span></span>

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

### <span data-ttu-id="8d4b5-139">-SecondaryServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-139">-SecondaryServiceObjectiveName</span></span>
<span data-ttu-id="8d4b5-140">보조 데이터베이스에 할당할 서비스 목표의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-140">Specifies the name of the service objective to assign to the secondary database.</span></span>

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

### <span data-ttu-id="8d4b5-141">-SecondaryVCore</span><span class="sxs-lookup"><span data-stu-id="8d4b5-141">-SecondaryVCore</span></span>
<span data-ttu-id="8d4b5-142">Azure Sql 데이터베이스 보조의 Vcore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-142">The Vcore numbers of the Azure Sql Database secondary.</span></span>

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

### <span data-ttu-id="8d4b5-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8d4b5-143">-ServerName</span></span>
<span data-ttu-id="8d4b5-144">기본 SQL 데이터베이스의 SQL Server 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-144">Specifies the name of the SQL Server of the primary  SQL Database.</span></span>

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

### <span data-ttu-id="8d4b5-145">태그</span><span class="sxs-lookup"><span data-stu-id="8d4b5-145">-Tags</span></span>
<span data-ttu-id="8d4b5-146">SQL 데이터베이스 복제 링크와 연결할 해시 테이블 형태의 키-값 쌍을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-146">Specifies the Key-value pairs in the form of a hash table to associate with the SQL Database replication link.</span></span> <span data-ttu-id="8d4b5-147">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="8d4b5-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="8d4b5-148">-확인</span><span class="sxs-lookup"><span data-stu-id="8d4b5-148">-Confirm</span></span>
<span data-ttu-id="8d4b5-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d4b5-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d4b5-150">-WhatIf</span></span>
<span data-ttu-id="8d4b5-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d4b5-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d4b5-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d4b5-153">CommonParameters</span></span>
<span data-ttu-id="8d4b5-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d4b5-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d4b5-156">입력</span><span class="sxs-lookup"><span data-stu-id="8d4b5-156">INPUTS</span></span>

### <span data-ttu-id="8d4b5-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8d4b5-157">System.String</span></span>

## <span data-ttu-id="8d4b5-158">출력</span><span class="sxs-lookup"><span data-stu-id="8d4b5-158">OUTPUTS</span></span>

### <span data-ttu-id="8d4b5-159">AzureReplicationLinkModel를 통해 서의.</span><span class="sxs-lookup"><span data-stu-id="8d4b5-159">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="8d4b5-160">상속자</span><span class="sxs-lookup"><span data-stu-id="8d4b5-160">NOTES</span></span>

## <span data-ttu-id="8d4b5-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d4b5-161">RELATED LINKS</span></span>

[<span data-ttu-id="8d4b5-162">제거-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d4b5-162">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="8d4b5-163">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="8d4b5-163">Set-AzSqlDatabaseSecondary</span></span>](./Set-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="8d4b5-164">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8d4b5-164">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
