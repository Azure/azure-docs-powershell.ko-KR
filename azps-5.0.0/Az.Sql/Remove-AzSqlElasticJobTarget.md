---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/remove-Azsqlelasticjobtarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlElasticJobTarget.md
ms.openlocfilehash: 4bd797528b3656364594f28f72d2b9ce2f7fdfaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218472"
---
# <span data-ttu-id="b1685-101">Remove-AzSqlElasticJobTarget</span><span class="sxs-lookup"><span data-stu-id="b1685-101">Remove-AzSqlElasticJobTarget</span></span>

## <span data-ttu-id="b1685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1685-102">SYNOPSIS</span></span>
<span data-ttu-id="b1685-103">대상 그룹에서 대상을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-103">Removes the target from the target group</span></span>

## <span data-ttu-id="b1685-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1685-104">SYNTAX</span></span>

### <span data-ttu-id="b1685-105">SqlDatabase (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1685-105">SqlDatabase (Default)</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-106">SqlServerOrElasticPool</span><span class="sxs-lookup"><span data-stu-id="b1685-106">SqlServerOrElasticPool</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> [-ElasticPoolName <String>] -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-107">SqlShardMap</span><span class="sxs-lookup"><span data-stu-id="b1685-107">SqlShardMap</span></span>
```
Remove-AzSqlElasticJobTarget [-ResourceGroupName] <String> [-AgentServerName] <String> [-AgentName] <String>
 [-TargetGroupName] <String> -ServerName <String> -ShardMapName <String> -DatabaseName <String>
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1685-108">SqlDatabaseUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b1685-108">SqlDatabaseUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -DatabaseName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-109">SqlServerOrElasticPoolUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b1685-109">SqlServerOrElasticPoolUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 [-ElasticPoolName <String>] -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-110">SqlShardMapUsingParentObject</span><span class="sxs-lookup"><span data-stu-id="b1685-110">SqlShardMapUsingParentObject</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentObject] <AzureSqlElasticJobTargetGroupModel> -ServerName <String>
 -ShardMapName <String> -DatabaseName <String> -RefreshCredentialName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-111">SqlDatabaseUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1685-111">SqlDatabaseUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -DatabaseName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b1685-112">SqlServerOrElasticPoolUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1685-112">SqlServerOrElasticPoolUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> [-ElasticPoolName <String>]
 -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b1685-113">SqlShardMapUsingParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1685-113">SqlShardMapUsingParentResourceId</span></span>
```
Remove-AzSqlElasticJobTarget [-ParentResourceId] <String> -ServerName <String> -ShardMapName <String>
 -DatabaseName <String> -RefreshCredentialName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b1685-114">설명은</span><span class="sxs-lookup"><span data-stu-id="b1685-114">DESCRIPTION</span></span>
<span data-ttu-id="b1685-115">대상 그룹에 대 한 대상 리소스를 제거 Remove-AzSqlElasticJobTarget cmdlet</span><span class="sxs-lookup"><span data-stu-id="b1685-115">The Remove-AzSqlElasticJobTarget cmdlet removes a target resource to a target group</span></span>

## <span data-ttu-id="b1685-116">예제의</span><span class="sxs-lookup"><span data-stu-id="b1685-116">EXAMPLES</span></span>

### <span data-ttu-id="b1685-117">예제 1: 서버 대상 제거</span><span class="sxs-lookup"><span data-stu-id="b1685-117">Example 1: Remove a server target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -RefreshCredentialName cred1

TargetGroupName TargetType TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ---------- ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlServer  s1                                                                           cred1                 Include
```

### <span data-ttu-id="b1685-118">예제 2: 데이터베이스 대상 제거</span><span class="sxs-lookup"><span data-stu-id="b1685-118">Example 2: Remove a database target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -DatabaseName db2

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlDatabase s1               db2                                                                               Include
```

### <span data-ttu-id="b1685-119">예제 3: 탄력적 풀 대상 제거</span><span class="sxs-lookup"><span data-stu-id="b1685-119">Example 3: Remove an elastic pool target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ElasticPoolName ep1 -RefreshCredentialName cred1

TargetGroupName TargetType     TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------     ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlElasticPool s1                                  ep1                                      cred1                 Include
```

### <span data-ttu-id="b1685-120">예제 4: 샤 드 맵 대상 제거</span><span class="sxs-lookup"><span data-stu-id="b1685-120">Example 4: Remove a shard map target</span></span>
```powershell
PS C:\> $tg = Get-AzSqlElasticJobTargetGroup -ResourceGroupName rg -ServerName elasticjobserver -Name tg1
$tg | Remove-AzSqlElasticJobTarget -ServerName s1 -ShardMapName sm1 -DatabaseName db1 -RefreshCredentialName cred1

TargetGroupName TargetType  TargetServerName TargetDatabaseName TargetElasticPoolName TargetShardMapName RefreshCredentialName MembershipType
--------------- ----------  ---------------- ------------------ --------------------- ------------------ --------------------- --------------
tg1             SqlShardMap s1               db1                                      sm1                cred1                 Include
```

<span data-ttu-id="b1685-121">대상 그룹에서 대상 (서버, 탄력적 풀, 데이터베이스 및 샤 드 맵)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-121">Removes a target (server, elastic pool, database, and shard map) from a target group</span></span>

## <span data-ttu-id="b1685-122">변수</span><span class="sxs-lookup"><span data-stu-id="b1685-122">PARAMETERS</span></span>

### <span data-ttu-id="b1685-123">-AgentName</span><span class="sxs-lookup"><span data-stu-id="b1685-123">-AgentName</span></span>
<span data-ttu-id="b1685-124">SQL 데이터베이스 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-124">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="b1685-125">-AgentServerName</span><span class="sxs-lookup"><span data-stu-id="b1685-125">-AgentServerName</span></span>
<span data-ttu-id="b1685-126">SQL 데이터베이스 에이전트 서버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-126">SQL Database Agent Server Name.</span></span>

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

### <span data-ttu-id="b1685-127">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="b1685-127">-DatabaseName</span></span>
<span data-ttu-id="b1685-128">데이터베이스 대상 이름</span><span class="sxs-lookup"><span data-stu-id="b1685-128">Database Target Name</span></span>

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

### <span data-ttu-id="b1685-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1685-129">-DefaultProfile</span></span>
<span data-ttu-id="b1685-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1685-131">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="b1685-131">-ElasticPoolName</span></span>
<span data-ttu-id="b1685-132">탄력적 풀 대상 이름</span><span class="sxs-lookup"><span data-stu-id="b1685-132">Elastic Pool Target Name</span></span>

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

### <span data-ttu-id="b1685-133">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b1685-133">-ParentObject</span></span>
<span data-ttu-id="b1685-134">대상 그룹 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-134">The target group object.</span></span>

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

### <span data-ttu-id="b1685-135">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b1685-135">-ParentResourceId</span></span>
<span data-ttu-id="b1685-136">대상 그룹 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-136">The target group resource id.</span></span>

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

### <span data-ttu-id="b1685-137">-RefreshCredentialName</span><span class="sxs-lookup"><span data-stu-id="b1685-137">-RefreshCredentialName</span></span>
<span data-ttu-id="b1685-138">자격 증명 이름 새로 고침</span><span class="sxs-lookup"><span data-stu-id="b1685-138">Refresh Credential Name</span></span>

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

### <span data-ttu-id="b1685-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1685-139">-ResourceGroupName</span></span>
<span data-ttu-id="b1685-140">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b1685-140">Resource Group Name</span></span>

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

### <span data-ttu-id="b1685-141">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b1685-141">-ServerName</span></span>
<span data-ttu-id="b1685-142">서버 대상 이름</span><span class="sxs-lookup"><span data-stu-id="b1685-142">Server Target Name</span></span>

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

### <span data-ttu-id="b1685-143">-ShardMapName</span><span class="sxs-lookup"><span data-stu-id="b1685-143">-ShardMapName</span></span>
<span data-ttu-id="b1685-144">샤 드 맵 대상 이름</span><span class="sxs-lookup"><span data-stu-id="b1685-144">Shard Map Target Name</span></span>

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

### <span data-ttu-id="b1685-145">-TargetGroupName</span><span class="sxs-lookup"><span data-stu-id="b1685-145">-TargetGroupName</span></span>
<span data-ttu-id="b1685-146">SQL 데이터베이스 에이전트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-146">SQL Database Agent Name.</span></span>

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

### <span data-ttu-id="b1685-147">-확인</span><span class="sxs-lookup"><span data-stu-id="b1685-147">-Confirm</span></span>
<span data-ttu-id="b1685-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1685-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1685-149">-WhatIf</span></span>
<span data-ttu-id="b1685-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1685-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1685-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1685-152">CommonParameters</span></span>
<span data-ttu-id="b1685-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1685-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1685-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b1685-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1685-155">입력</span><span class="sxs-lookup"><span data-stu-id="b1685-155">INPUTS</span></span>

### <span data-ttu-id="b1685-156">ElasticJobs. AzureSqlElasticJobTargetGroupModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="b1685-156">Microsoft.Azure.Commands.Sql.ElasticJobs.Model.AzureSqlElasticJobTargetGroupModel</span></span>

## <span data-ttu-id="b1685-157">출력</span><span class="sxs-lookup"><span data-stu-id="b1685-157">OUTPUTS</span></span>

### <span data-ttu-id="b1685-158">Microsoft. Azure. 관리 대상</span><span class="sxs-lookup"><span data-stu-id="b1685-158">Microsoft.Azure.Management.Sql.Models.JobTarget</span></span>

## <span data-ttu-id="b1685-159">상속자</span><span class="sxs-lookup"><span data-stu-id="b1685-159">NOTES</span></span>

## <span data-ttu-id="b1685-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1685-160">RELATED LINKS</span></span>
