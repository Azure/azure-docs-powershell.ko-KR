---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/new-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/New-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 6f1af89c1557739e218506d441e6acb109fcf773
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979803"
---
# <span data-ttu-id="0ef40-101">New-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="0ef40-101">New-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="0ef40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef40-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef40-103">새 데이터베이스를 만들고 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-103">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="0ef40-104">구문</span><span class="sxs-lookup"><span data-stu-id="0ef40-104">SYNTAX</span></span>

### <span data-ttu-id="0ef40-105">CreateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="0ef40-105">CreateExpanded (Default)</span></span>
```
New-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-Charset <String>] [-Collation <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0ef40-106">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0ef40-106">CreateViaIdentityExpanded</span></span>
```
New-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-Charset <String>] [-Collation <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0ef40-107">설명</span><span class="sxs-lookup"><span data-stu-id="0ef40-107">DESCRIPTION</span></span>
<span data-ttu-id="0ef40-108">새 데이터베이스를 만들고 기존 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-108">Creates a new database or updates an existing database.</span></span>

## <span data-ttu-id="0ef40-109">예제</span><span class="sxs-lookup"><span data-stu-id="0ef40-109">EXAMPLES</span></span>

### <span data-ttu-id="0ef40-110">예제 1: 새 MySql 서버 데이터베이스 만들기</span><span class="sxs-lookup"><span data-stu-id="0ef40-110">Example 1: Create a new MySql server database</span></span>
```powershell
PS C:\> New-AzMySqlFlexibleServerDatabase -Name databasetest -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name            Charset     Collation              
----            -------- ------------------
databasetest   latin1   latin1_swedish_ci  
```

<span data-ttu-id="0ef40-111">기본 설정으로 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-111">Create a database with default settings.</span></span>

## <span data-ttu-id="0ef40-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ef40-112">PARAMETERS</span></span>

### <span data-ttu-id="0ef40-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ef40-113">-AsJob</span></span>
<span data-ttu-id="0ef40-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0ef40-115">-Charset</span><span class="sxs-lookup"><span data-stu-id="0ef40-115">-Charset</span></span>
<span data-ttu-id="0ef40-116">데이터베이스의 charset입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-116">The charset of the database.</span></span>

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

### <span data-ttu-id="0ef40-117">-Collation</span><span class="sxs-lookup"><span data-stu-id="0ef40-117">-Collation</span></span>
<span data-ttu-id="0ef40-118">데이터베이스의 데이터 콜리전입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-118">The collation of the database.</span></span>

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

### <span data-ttu-id="0ef40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef40-119">-DefaultProfile</span></span>
<span data-ttu-id="0ef40-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ef40-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ef40-121">-InputObject</span></span>
<span data-ttu-id="0ef40-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0ef40-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef40-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0ef40-123">-Name</span></span>
<span data-ttu-id="0ef40-124">데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-124">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef40-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0ef40-125">-NoWait</span></span>
<span data-ttu-id="0ef40-126">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="0ef40-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0ef40-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef40-127">-ResourceGroupName</span></span>
<span data-ttu-id="0ef40-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-128">The name of the resource group.</span></span>
<span data-ttu-id="0ef40-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef40-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0ef40-130">-ServerName</span></span>
<span data-ttu-id="0ef40-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef40-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ef40-132">-SubscriptionId</span></span>
<span data-ttu-id="0ef40-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef40-134">-확인</span><span class="sxs-lookup"><span data-stu-id="0ef40-134">-Confirm</span></span>
<span data-ttu-id="0ef40-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ef40-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef40-136">-WhatIf</span></span>
<span data-ttu-id="0ef40-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef40-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ef40-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef40-139">CommonParameters</span></span>
<span data-ttu-id="0ef40-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef40-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0ef40-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef40-142">입력</span><span class="sxs-lookup"><span data-stu-id="0ef40-142">INPUTS</span></span>

### <span data-ttu-id="0ef40-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0ef40-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0ef40-144">출력</span><span class="sxs-lookup"><span data-stu-id="0ef40-144">OUTPUTS</span></span>

### <span data-ttu-id="0ef40-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="0ef40-145">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="0ef40-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0ef40-146">NOTES</span></span>

<span data-ttu-id="0ef40-147">별칭</span><span class="sxs-lookup"><span data-stu-id="0ef40-147">ALIASES</span></span>

<span data-ttu-id="0ef40-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0ef40-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0ef40-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ef40-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0ef40-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0ef40-151">INPUTOBJECT <IMySqlIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ef40-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ef40-152">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0ef40-153">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0ef40-154">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0ef40-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0ef40-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ef40-156">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0ef40-157">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0ef40-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0ef40-159">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="0ef40-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0ef40-161">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0ef40-162">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0ef40-163">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef40-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0ef40-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ef40-164">RELATED LINKS</span></span>

