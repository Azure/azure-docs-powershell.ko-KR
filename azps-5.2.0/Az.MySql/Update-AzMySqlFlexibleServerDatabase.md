---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 2867c6f57967da64178e798f3e517715b44d07c2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360207"
---
# <span data-ttu-id="8ae7f-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="8ae7f-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="8ae7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ae7f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ae7f-103">새 데이터베이스를 생성하거나 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="8ae7f-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ae7f-104">SYNTAX</span></span>

### <span data-ttu-id="8ae7f-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="8ae7f-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8ae7f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8ae7f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8ae7f-107">설명</span><span class="sxs-lookup"><span data-stu-id="8ae7f-107">DESCRIPTION</span></span>
<span data-ttu-id="8ae7f-108">새 데이터베이스를 생성하거나 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="8ae7f-109">예제</span><span class="sxs-lookup"><span data-stu-id="8ae7f-109">EXAMPLES</span></span>

### <span data-ttu-id="8ae7f-110">예제 1: 이름으로 MySql 서버 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="8ae7f-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="8ae7f-111">리소스 이름으로 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-111">Update a database by resource name.</span></span>

### <span data-ttu-id="8ae7f-112">예제 2: 매개 변수에 따라 MySql 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="8ae7f-113">매개 변수로 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="8ae7f-113">Update a database by parameter</span></span>

## <span data-ttu-id="8ae7f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ae7f-114">PARAMETERS</span></span>

### <span data-ttu-id="8ae7f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ae7f-115">-AsJob</span></span>
<span data-ttu-id="8ae7f-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="8ae7f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8ae7f-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="8ae7f-117">-Charset</span></span>
<span data-ttu-id="8ae7f-118">데이터베이스의 charset입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-118">The charset of the database.</span></span>

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

### <span data-ttu-id="8ae7f-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="8ae7f-119">-Collation</span></span>
<span data-ttu-id="8ae7f-120">데이터베이스의 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-120">The collation of the database.</span></span>

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

### <span data-ttu-id="8ae7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ae7f-121">-DefaultProfile</span></span>
<span data-ttu-id="8ae7f-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8ae7f-123">-InputObject</span></span>
<span data-ttu-id="8ae7f-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8ae7f-125">-Name</span></span>
<span data-ttu-id="8ae7f-126">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-126">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8ae7f-127">-NoWait</span></span>
<span data-ttu-id="8ae7f-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="8ae7f-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8ae7f-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ae7f-129">-ResourceGroupName</span></span>
<span data-ttu-id="8ae7f-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-130">The name of the resource group.</span></span>
<span data-ttu-id="8ae7f-131">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-131">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8ae7f-132">-ServerName</span></span>
<span data-ttu-id="8ae7f-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-133">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8ae7f-134">-SubscriptionId</span></span>
<span data-ttu-id="8ae7f-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-135">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8ae7f-136">-Confirm</span></span>
<span data-ttu-id="8ae7f-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ae7f-138">-WhatIf</span></span>
<span data-ttu-id="8ae7f-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8ae7f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ae7f-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ae7f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ae7f-141">CommonParameters</span></span>
<span data-ttu-id="8ae7f-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ae7f-143">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ae7f-144">입력</span><span class="sxs-lookup"><span data-stu-id="8ae7f-144">INPUTS</span></span>

### <span data-ttu-id="8ae7f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="8ae7f-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="8ae7f-146">출력</span><span class="sxs-lookup"><span data-stu-id="8ae7f-146">OUTPUTS</span></span>

### <span data-ttu-id="8ae7f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="8ae7f-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="8ae7f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ae7f-148">NOTES</span></span>

<span data-ttu-id="8ae7f-149">별칭</span><span class="sxs-lookup"><span data-stu-id="8ae7f-149">ALIASES</span></span>

<span data-ttu-id="8ae7f-150">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="8ae7f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8ae7f-151">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8ae7f-152">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8ae7f-153">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8ae7f-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8ae7f-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="8ae7f-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="8ae7f-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="8ae7f-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="8ae7f-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8ae7f-158">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="8ae7f-159">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="8ae7f-160">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="8ae7f-161">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="8ae7f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="8ae7f-163">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="8ae7f-164">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="8ae7f-165">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ae7f-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="8ae7f-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ae7f-166">RELATED LINKS</span></span>

