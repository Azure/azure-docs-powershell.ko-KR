---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: CED38886-2DC9-450E-91FF-8209602C76CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseCopy.md
ms.openlocfilehash: 29244502e3413950696faf3bbb2ea296cb798883
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360641"
---
# <span data-ttu-id="3cdaf-101">New-AzSqlDatabaseCopy</span><span class="sxs-lookup"><span data-stu-id="3cdaf-101">New-AzSqlDatabaseCopy</span></span>

## <span data-ttu-id="3cdaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cdaf-102">SYNOPSIS</span></span>
<span data-ttu-id="3cdaf-103">현재 시점에 스냅숏을 SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-103">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span>

## <span data-ttu-id="3cdaf-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cdaf-104">SYNTAX</span></span>

### <span data-ttu-id="3cdaf-105">DtuBasedDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="3cdaf-105">DtuBasedDatabase (Default)</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-ServiceObjectiveName <String>] [-ElasticPoolName <String>]
 [-Tags <Hashtable>] [-CopyResourceGroupName <String>] [-CopyServerName <String>] -CopyDatabaseName <String>
 [-AsJob] [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3cdaf-106">VcoreBasedDatabase</span><span class="sxs-lookup"><span data-stu-id="3cdaf-106">VcoreBasedDatabase</span></span>
```
New-AzSqlDatabaseCopy [-DatabaseName] <String> [-Tags <Hashtable>] [-CopyResourceGroupName <String>]
 [-CopyServerName <String>] -CopyDatabaseName <String> [-AsJob] -ComputeGeneration <String> -VCore <Int32>
 [-LicenseType <String>] [-BackupStorageRedundancy <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cdaf-107">설명</span><span class="sxs-lookup"><span data-stu-id="3cdaf-107">DESCRIPTION</span></span>
<span data-ttu-id="3cdaf-108">**New-AzSqlDatabaseCopy** cmdlet은 현재 데이터의 스냅숏을 사용하는 Azure SQL Database의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-108">The **New-AzSqlDatabaseCopy** cmdlet creates a copy of an Azure SQL Database that uses the snapshot of the data at the current time.</span></span> <span data-ttu-id="3cdaf-109">일회성 데이터베이스 복사본을 만들 Start-AzSqlDatabaseCopy cmdlet 대신 이 cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-109">Use this cmdlet instead of the Start-AzSqlDatabaseCopy cmdlet to create a one-time database copy.</span></span> <span data-ttu-id="3cdaf-110">이 cmdlet은 **복사본의 데이터베이스** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-110">This cmdlet returns the **Database** object of the copy.</span></span>
<span data-ttu-id="3cdaf-111">참고: New-AzSqlDatabaseSecondary cmdlet을 사용하여 데이터베이스에 대한 지역 복제를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-111">Note: Use the New-AzSqlDatabaseSecondary cmdlet to configure geo-replication for a database.</span></span>
<span data-ttu-id="3cdaf-112">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="3cdaf-113">예제</span><span class="sxs-lookup"><span data-stu-id="3cdaf-113">EXAMPLES</span></span>

### <span data-ttu-id="3cdaf-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cdaf-114">Example 1</span></span>

<span data-ttu-id="3cdaf-115">현재 시점에 스냅숏을 SQL 데이터베이스의 복사본을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-115">Creates a copy of a SQL Database that uses the snapshot at the current time.</span></span> <span data-ttu-id="3cdaf-116">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="3cdaf-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseCopy -CopyDatabaseName <String> -CopyResourceGroupName <String> -CopyServerName <String> -DatabaseName db1 -ResourceGroupName MyResourceGroup -ServerName s1
```

## <span data-ttu-id="3cdaf-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cdaf-117">PARAMETERS</span></span>

### <span data-ttu-id="3cdaf-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cdaf-118">-AsJob</span></span>
<span data-ttu-id="3cdaf-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3cdaf-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3cdaf-120">-BackupStorageRedundancy</span><span class="sxs-lookup"><span data-stu-id="3cdaf-120">-BackupStorageRedundancy</span></span>
<span data-ttu-id="3cdaf-121">SQL 데이터베이스에 대한 백업을 저장하는 데 사용되는 Backup 저장소 중복성입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-121">The Backup storage redundancy used to store backups for the SQL Database.</span></span> <span data-ttu-id="3cdaf-122">옵션은 로컬, 영역 및 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-122">Options are: Local, Zone and Geo.</span></span>

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

### <span data-ttu-id="3cdaf-123">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="3cdaf-123">-ComputeGeneration</span></span>
<span data-ttu-id="3cdaf-124">새 복사본에 할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-124">The compute generation to assign to the new copy.</span></span>

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

### <span data-ttu-id="3cdaf-125">-CopyDatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-125">-CopyDatabaseName</span></span>
<span data-ttu-id="3cdaf-126">데이터베이스 복사본의 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-126">Specifies the name of the SQL Database copy.</span></span>

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

### <span data-ttu-id="3cdaf-127">-CopyResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-127">-CopyResourceGroupName</span></span>
<span data-ttu-id="3cdaf-128">복사본을 할당할 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-128">Specifies the name of the Azure Resource Group in which to assign the copy.</span></span>

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

### <span data-ttu-id="3cdaf-129">-CopyServerName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-129">-CopyServerName</span></span>
<span data-ttu-id="3cdaf-130">복사본을 호스트하는 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-130">Specifies the name of the SQL Server which hosts the copy.</span></span>

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

### <span data-ttu-id="3cdaf-131">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-131">-DatabaseName</span></span>
<span data-ttu-id="3cdaf-132">복사할 SQL 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-132">Specifies the name of the SQL Database to copy.</span></span>

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

### <span data-ttu-id="3cdaf-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cdaf-133">-DefaultProfile</span></span>
<span data-ttu-id="3cdaf-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3cdaf-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3cdaf-135">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-135">-ElasticPoolName</span></span>
<span data-ttu-id="3cdaf-136">복사본을 할당할 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-136">Specifies the name of the elastic pool in which to assign the copy.</span></span>

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

### <span data-ttu-id="3cdaf-137">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="3cdaf-137">-LicenseType</span></span>
<span data-ttu-id="3cdaf-138">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-138">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="3cdaf-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-139">-ResourceGroupName</span></span>
<span data-ttu-id="3cdaf-140">복사할 데이터베이스가 포함된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-140">Specifies the name of the Resource Group that contains the database to copy.</span></span>

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

### <span data-ttu-id="3cdaf-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-141">-ServerName</span></span>
<span data-ttu-id="3cdaf-142">복사할 데이터베이스가 SQL Server 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-142">Specifies the name of the  SQL Server that contains the database to copy.</span></span>

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

### <span data-ttu-id="3cdaf-143">-ServiceObjectiveName</span><span class="sxs-lookup"><span data-stu-id="3cdaf-143">-ServiceObjectiveName</span></span>
<span data-ttu-id="3cdaf-144">복사본에 할당할 서비스 목표의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-144">Specifies the name of the service objective to assign to the copy.</span></span>

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

### <span data-ttu-id="3cdaf-145">-Tags</span><span class="sxs-lookup"><span data-stu-id="3cdaf-145">-Tags</span></span>
<span data-ttu-id="3cdaf-146">Azure SQL Database 복사본과 연결하기 위한 해시 테이블의 형태로 키-값 쌍을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-146">Specifies the Key-value pairs in the form of a hash table to associate with the Azure SQL Database copy.</span></span> <span data-ttu-id="3cdaf-147">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3cdaf-147">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3cdaf-148">-VCore</span><span class="sxs-lookup"><span data-stu-id="3cdaf-148">-VCore</span></span>
<span data-ttu-id="3cdaf-149">Azure Sql Database 복사본의 Vcore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-149">The Vcore numbers of the Azure Sql Database copy.</span></span>

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

### <span data-ttu-id="3cdaf-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cdaf-150">-Confirm</span></span>
<span data-ttu-id="3cdaf-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cdaf-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cdaf-152">-WhatIf</span></span>
<span data-ttu-id="3cdaf-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3cdaf-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cdaf-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cdaf-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cdaf-155">CommonParameters</span></span>
<span data-ttu-id="3cdaf-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cdaf-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cdaf-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cdaf-158">입력</span><span class="sxs-lookup"><span data-stu-id="3cdaf-158">INPUTS</span></span>

### <span data-ttu-id="3cdaf-159">System.String</span><span class="sxs-lookup"><span data-stu-id="3cdaf-159">System.String</span></span>

## <span data-ttu-id="3cdaf-160">출력</span><span class="sxs-lookup"><span data-stu-id="3cdaf-160">OUTPUTS</span></span>

### <span data-ttu-id="3cdaf-161">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span><span class="sxs-lookup"><span data-stu-id="3cdaf-161">Microsoft.Azure.Commands.Sql.Replication.Model.AzureSqlDatabaseCopyModel</span></span>

## <span data-ttu-id="3cdaf-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cdaf-162">NOTES</span></span>

## <span data-ttu-id="3cdaf-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cdaf-163">RELATED LINKS</span></span>

[<span data-ttu-id="3cdaf-164">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="3cdaf-164">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="3cdaf-165">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="3cdaf-165">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)