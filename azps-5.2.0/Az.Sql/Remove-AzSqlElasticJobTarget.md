---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368978"
---
# <span data-ttu-id="d028c-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="d028c-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="d028c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d028c-102">SYNOPSIS</span></span>
<span data-ttu-id="d028c-103">대상 그룹에서 대상을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-103">Removes the target from the target group</span></span>

## <span data-ttu-id="d028c-104">구문</span><span class="sxs-lookup"><span data-stu-id="d028c-104">SYNTAX</span></span>

### <span data-ttu-id="d028c-105">SqlDatabase(기본값)</span><span class="sxs-lookup"><span data-stu-id="d028c-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="d028c-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="d028c-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d028c-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d028c-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d028c-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="d028c-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d028c-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d028c-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d028c-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d028c-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d028c-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d028c-114">설명</span><span class="sxs-lookup"><span data-stu-id="d028c-114">DESCRIPTION</span></span>
<span data-ttu-id="d028c-115">Remove-AzSqlElasticJobTarget cmdlet은 대상 그룹에 대한 대상 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="d028c-116">예제</span><span class="sxs-lookup"><span data-stu-id="d028c-116">EXAMPLES</span></span>

### <span data-ttu-id="d028c-117">예제 1: 서버 대상 제거</span><span class="sxs-lookup"><span data-stu-id="d028c-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="d028c-118">예제 2: 데이터베이스 대상 제거</span><span class="sxs-lookup"><span data-stu-id="d028c-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="d028c-119">예제 3: 탄력적 풀 대상 제거</span><span class="sxs-lookup"><span data-stu-id="d028c-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="d028c-120">예제 4: 분리된 맵 대상 제거</span><span class="sxs-lookup"><span data-stu-id="d028c-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="d028c-121">대상 그룹에서 대상(서버, 탄력적 풀, 데이터베이스 및 데이터베이스 맵)을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="d028c-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d028c-122">PARAMETERS</span></span>

### <span data-ttu-id="d028c-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="d028c-123">-AgentName</span></span>
<span data-ttu-id="d028c-124">SQL 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="d028c-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="d028c-125">-AgentServerName</span></span>
<span data-ttu-id="d028c-126">SQL 에이전트 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="d028c-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d028c-127">-DatabaseName</span></span>
<span data-ttu-id="d028c-128">데이터베이스 대상 이름</span><span class="sxs-lookup"><span data-stu-id="d028c-128">Database Target Name</span></span>

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

### <span data-ttu-id="d028c-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d028c-129">-DefaultProfile</span></span>
<span data-ttu-id="d028c-130">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d028c-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d028c-131">-ElasticPoolName</span></span>
<span data-ttu-id="d028c-132">탄력적 풀 대상 이름</span><span class="sxs-lookup"><span data-stu-id="d028c-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="d028c-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d028c-133">-ParentObject</span></span>
<span data-ttu-id="d028c-134">대상 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-134">The target group object.</span></span>

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

### <span data-ttu-id="d028c-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d028c-135">-ParentResourceId</span></span>
<span data-ttu-id="d028c-136">대상 그룹 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-136">The target group resource id.</span></span>

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

### <span data-ttu-id="d028c-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="d028c-137">-RefreshCredentialName</span></span>
<span data-ttu-id="d028c-138">자격 증명 이름 새로 고침</span><span class="sxs-lookup"><span data-stu-id="d028c-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="d028c-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d028c-139">-ResourceGroupName</span></span>
<span data-ttu-id="d028c-140">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d028c-140">Resource Group Name</span></span>

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

### <span data-ttu-id="d028c-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d028c-141">-ServerName</span></span>
<span data-ttu-id="d028c-142">서버 대상 이름</span><span class="sxs-lookup"><span data-stu-id="d028c-142">Server Target Name</span></span>

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

### <span data-ttu-id="d028c-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="d028c-143">-ShardMapName</span></span>
<span data-ttu-id="d028c-144">Shard Map 대상 이름</span><span class="sxs-lookup"><span data-stu-id="d028c-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="d028c-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="d028c-145">-TargetGroupName</span></span>
<span data-ttu-id="d028c-146">SQL 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="d028c-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d028c-147">-Confirm</span></span>
<span data-ttu-id="d028c-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d028c-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d028c-149">-WhatIf</span></span>
<span data-ttu-id="d028c-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d028c-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d028c-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d028c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d028c-152">CommonParameters</span></span>
<span data-ttu-id="d028c-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d028c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d028c-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d028c-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d028c-155">입력</span><span class="sxs-lookup"><span data-stu-id="d028c-155">INPUTS</span></span>

### <span data-ttu-id="d028c-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span><span class="sxs-lookup"><span data-stu-id="d028c-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="d028c-157">출력</span><span class="sxs-lookup"><span data-stu-id="d028c-157">OUTPUTS</span></span>

### <span data-ttu-id="d028c-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span><span class="sxs-lookup"><span data-stu-id="d028c-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="d028c-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d028c-159">NOTES</span></span>

## <span data-ttu-id="d028c-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d028c-160">RELATED LINKS</span></span>
