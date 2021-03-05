---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 7d356bc977ce02d998230ad755f43479e09f0a66
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968779"
---
# <span data-ttu-id="29461-101">Update-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="29461-101">Update-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="29461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29461-102">SYNOPSIS</span></span>
<span data-ttu-id="29461-103">새 데이터베이스를 만들고 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="29461-104">구문</span><span class="sxs-lookup"><span data-stu-id="29461-104">SYNTAX</span></span>

### <span data-ttu-id="29461-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="29461-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="29461-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="29461-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="29461-107">설명</span><span class="sxs-lookup"><span data-stu-id="29461-107">DESCRIPTION</span></span>
<span data-ttu-id="29461-108">새 데이터베이스를 만들고 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="29461-109">예제</span><span class="sxs-lookup"><span data-stu-id="29461-109">EXAMPLES</span></span>

### <span data-ttu-id="29461-110">예제 1: 이름에 따라 MySql 서버 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="29461-110">Example 1: Update a MySql server database by name</span></span>
```powershell
PS C:\> Update-AzMySqlFlexibleServerDatabase -Name database-test -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="29461-111">리소스 이름으로 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-111">Update a database by resource name.</span></span>

### <span data-ttu-id="29461-112">예제 2: 매개 변수에 따라 MySql 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-112">Example 2: Update MySql database by parameter.</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/servers/mysql-test/databases/databasetest"
PS C:\> Update-AzMySqlFlexibleServerDatabase -Parameter $ID -Charset utf8

Name            Charset     Collation              
----            -------- ------------------
databasetest   utf8      latin1_swedish_ci  
```

<span data-ttu-id="29461-113">매개 변수에 따라 데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="29461-113">Update a database by parameter</span></span>

## <span data-ttu-id="29461-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="29461-114">PARAMETERS</span></span>

### <span data-ttu-id="29461-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29461-115">-AsJob</span></span>
<span data-ttu-id="29461-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-116">Run the command as a job</span></span>

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

### <span data-ttu-id="29461-117">-Charset</span><span class="sxs-lookup"><span data-stu-id="29461-117">-Charset</span></span>
<span data-ttu-id="29461-118">데이터베이스의 charset입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-118">The charset of the database.</span></span>

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

### <span data-ttu-id="29461-119">-Collation</span><span class="sxs-lookup"><span data-stu-id="29461-119">-Collation</span></span>
<span data-ttu-id="29461-120">데이터베이스의 데이터 콜리전입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-120">The collation of the database.</span></span>

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

### <span data-ttu-id="29461-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29461-121">-DefaultProfile</span></span>
<span data-ttu-id="29461-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29461-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29461-123">-InputObject</span></span>
<span data-ttu-id="29461-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="29461-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="29461-125">-Name</span><span class="sxs-lookup"><span data-stu-id="29461-125">-Name</span></span>
<span data-ttu-id="29461-126">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-126">The name of the database.</span></span>

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

### <span data-ttu-id="29461-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="29461-127">-NoWait</span></span>
<span data-ttu-id="29461-128">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="29461-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="29461-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29461-129">-ResourceGroupName</span></span>
<span data-ttu-id="29461-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-130">The name of the resource group.</span></span>
<span data-ttu-id="29461-131">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="29461-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="29461-132">-ServerName</span></span>
<span data-ttu-id="29461-133">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-133">The name of the server.</span></span>

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

### <span data-ttu-id="29461-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="29461-134">-SubscriptionId</span></span>
<span data-ttu-id="29461-135">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-135">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="29461-136">-확인</span><span class="sxs-lookup"><span data-stu-id="29461-136">-Confirm</span></span>
<span data-ttu-id="29461-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="29461-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29461-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29461-138">-WhatIf</span></span>
<span data-ttu-id="29461-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="29461-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29461-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="29461-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29461-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29461-141">CommonParameters</span></span>
<span data-ttu-id="29461-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29461-143">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29461-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29461-144">입력</span><span class="sxs-lookup"><span data-stu-id="29461-144">INPUTS</span></span>

### <span data-ttu-id="29461-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="29461-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="29461-146">출력</span><span class="sxs-lookup"><span data-stu-id="29461-146">OUTPUTS</span></span>

### <span data-ttu-id="29461-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="29461-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="29461-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="29461-148">NOTES</span></span>

<span data-ttu-id="29461-149">별칭</span><span class="sxs-lookup"><span data-stu-id="29461-149">ALIASES</span></span>

<span data-ttu-id="29461-150">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="29461-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="29461-151">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="29461-152">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="29461-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="29461-153">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="29461-153">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="29461-154">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="29461-155">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="29461-156">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="29461-157">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="29461-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="29461-158">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-158">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="29461-159">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-159">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="29461-160">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-160">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="29461-161">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="29461-161">The name is case insensitive.</span></span>
  - <span data-ttu-id="29461-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-162">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="29461-163">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-163">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="29461-164">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-164">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="29461-165">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="29461-165">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="29461-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="29461-166">RELATED LINKS</span></span>

