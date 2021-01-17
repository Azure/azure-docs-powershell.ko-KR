---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlElasticJobTarget.md
ms.openlocfilehash: cdf50079a08a4ac021e78e210ae574aa978674fe
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375586"
---
# <span data-ttu-id="79a83-101">Add-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="79a83-101">Add-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="79a83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a83-102">SYNOPSIS</span></span>
<span data-ttu-id="79a83-103">대상 그룹에 대상 추가</span><span class="sxs-lookup"><span data-stu-id="79a83-103">Adds a target to a target group</span></span>

## <span data-ttu-id="79a83-104">구문</span><span class="sxs-lookup"><span data-stu-id="79a83-104">SYNTAX</span></span>

### <span data-ttu-id="79a83-105">SqlDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="79a83-105">SqlDatabase (Default)</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="79a83-106">SqlServerOrElasticPool</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79a83-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="79a83-107">SqlShardMap</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ResourceGroupName] <String> [-AgentServerName] <String>
 [-AgentName] <String> [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="79a83-108">SqlDatabaseUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="79a83-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="79a83-110">SqlShardMapUsingParentObject</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79a83-111">SqlDatabaseUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79a83-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79a83-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79a83-113">SqlShardMapUsingParentResourceId</span></span>
```
Add-AzSqlElasticJobTarget [-Exclude] [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79a83-114">설명</span><span class="sxs-lookup"><span data-stu-id="79a83-114">DESCRIPTION</span></span>
<span data-ttu-id="79a83-115">Add-AzSqlElasticJobTarget cmdlet은 대상 그룹에 대상 리소스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-115">The Add-AzSqlElasticJobTarget cmdlet adds a target resource to a target group</span></span>

## <span data-ttu-id="79a83-116">예제</span><span class="sxs-lookup"><span data-stu-id="79a83-116">EXAMPLES</span></span>

### <span data-ttu-id="79a83-117">예제 1: 서버 대상 추가</span><span class="sxs-lookup"><span data-stu-id="79a83-117">Example 1: Add a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="79a83-118">예제 2: 데이터베이스 대상 추가</span><span class="sxs-lookup"><span data-stu-id="79a83-118">Example 2: Add a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="79a83-119">예제 3: 탄력적 풀 대상 추가</span><span class="sxs-lookup"><span data-stu-id="79a83-119">Example 3: Add an elastic pool target</span></span>
```powershell
PS C:\> $tg | Add-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="79a83-120">예제 4: Shard Map 대상 추가</span><span class="sxs-lookup"><span data-stu-id="79a83-120">Example 4: Add a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Add-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="79a83-121">대상 그룹에 대상(서버, 탄력적 풀, 데이터베이스 및 데이터베이스 맵)을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-121">Adds a target (server, elastic pool, database, and shard map) to a target group</span></span>

## <span data-ttu-id="79a83-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79a83-122">PARAMETERS</span></span>

### <span data-ttu-id="79a83-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="79a83-123">-AgentName</span></span>
<span data-ttu-id="79a83-124">에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-124">The agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="79a83-125">-AgentServerName</span></span>
<span data-ttu-id="79a83-126">서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-126">The server name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="79a83-127">-DatabaseName</span></span>
<span data-ttu-id="79a83-128">데이터베이스 대상 이름</span><span class="sxs-lookup"><span data-stu-id="79a83-128">Database Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a83-129">-DefaultProfile</span></span>
<span data-ttu-id="79a83-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79a83-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="79a83-131">-ElasticPoolName</span></span>
<span data-ttu-id="79a83-132">탄력적 풀 대상 이름</span><span class="sxs-lookup"><span data-stu-id="79a83-132">Elastic Pool Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlServerOrElasticPoolUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-133">-Exclude</span><span class="sxs-lookup"><span data-stu-id="79a83-133">-Exclude</span></span>
<span data-ttu-id="79a83-134">대상을 제외합니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-134">Excludes a target.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-135">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="79a83-135">-ParentObject</span></span>
<span data-ttu-id="79a83-136">대상 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-136">The target group object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel
Parameter Sets: SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-137">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="79a83-137">-ParentResourceId</span></span>
<span data-ttu-id="79a83-138">대상 그룹 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-138">The target group resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-139">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="79a83-139">-RefreshCredentialName</span></span>
<span data-ttu-id="79a83-140">자격 증명 이름 새로 고침</span><span class="sxs-lookup"><span data-stu-id="79a83-140">Refresh Credential Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool, SqlShardMap, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79a83-141">-ResourceGroupName</span></span>
<span data-ttu-id="79a83-142">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="79a83-142">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-143">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79a83-143">-ServerName</span></span>
<span data-ttu-id="79a83-144">서버 대상 이름</span><span class="sxs-lookup"><span data-stu-id="79a83-144">Server Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlShardMap, SqlDatabaseUsingParentObject, SqlServerOrElasticPoolUsingParentObject, SqlShardMapUsingParentObject, SqlDatabaseUsingParentResourceId, SqlServerOrElasticPoolUsingParentResourceId, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SqlServerOrElasticPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-145">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="79a83-145">-ShardMapName</span></span>
<span data-ttu-id="79a83-146">Shard Map 대상 이름</span><span class="sxs-lookup"><span data-stu-id="79a83-146">Shard Map Target Name</span></span>

```yaml
Type: System.String
Parameter Sets: SqlShardMap, SqlShardMapUsingParentObject, SqlShardMapUsingParentResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-147">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="79a83-147">-TargetGroupName</span></span>
<span data-ttu-id="79a83-148">대상 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-148">The target group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlDatabase, SqlServerOrElasticPool, SqlShardMap
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a83-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79a83-149">-Confirm</span></span>
<span data-ttu-id="79a83-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79a83-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79a83-151">-WhatIf</span></span>
<span data-ttu-id="79a83-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="79a83-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79a83-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79a83-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a83-154">CommonParameters</span></span>
<span data-ttu-id="79a83-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79a83-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a83-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79a83-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a83-157">입력</span><span class="sxs-lookup"><span data-stu-id="79a83-157">INPUTS</span></span>

### <span data-ttu-id="79a83-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="79a83-158">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="79a83-159">출력</span><span class="sxs-lookup"><span data-stu-id="79a83-159">OUTPUTS</span></span>

### <span data-ttu-id="79a83-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="79a83-160">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="79a83-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79a83-161">NOTES</span></span>

## <span data-ttu-id="79a83-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79a83-162">RELATED LINKS</span></span>
