---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/remove-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Remove-AzMySqlFirewallRule.md
ms.openlocfilehash: 481761efe01646a10118d8ebfd645375caafbfef
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339434"
---
# <span data-ttu-id="2b463-101">Remove-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="2b463-101">Remove-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="2b463-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b463-102">SYNOPSIS</span></span>
<span data-ttu-id="2b463-103">서버 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="2b463-104">구문</span><span class="sxs-lookup"><span data-stu-id="2b463-104">SYNTAX</span></span>

### <span data-ttu-id="2b463-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="2b463-105">Delete (Default)</span></span>
```
Remove-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="2b463-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b463-106">DeleteViaIdentity</span></span>
```
Remove-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b463-107">설명</span><span class="sxs-lookup"><span data-stu-id="2b463-107">DESCRIPTION</span></span>
<span data-ttu-id="2b463-108">서버 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="2b463-109">예제</span><span class="sxs-lookup"><span data-stu-id="2b463-109">EXAMPLES</span></span>

### <span data-ttu-id="2b463-110">예제 1: 이름으로 MySql 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="2b463-110">Example 1: Remove MySql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

```

<span data-ttu-id="2b463-111">이 cmdlet은 이름으로 MySql 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-111">This cmdlet removes MySql Firewall Rule by name.</span></span>

### <span data-ttu-id="2b463-112">예제 2: ID로 MySql 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="2b463-112">Example 2: Remove MySql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Remove-AzMySqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="2b463-113">이러한 cmdlet은 ID에 의해 MySql 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-113">These cmdlets remove MySql Firewall Rule by identity.</span></span>

## <span data-ttu-id="2b463-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b463-114">PARAMETERS</span></span>

### <span data-ttu-id="2b463-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b463-115">-AsJob</span></span>
<span data-ttu-id="2b463-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="2b463-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2b463-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b463-117">-DefaultProfile</span></span>
<span data-ttu-id="2b463-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b463-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b463-119">-InputObject</span></span>
<span data-ttu-id="2b463-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2b463-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b463-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2b463-121">-Name</span></span>
<span data-ttu-id="2b463-122">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-122">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b463-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b463-123">-NoWait</span></span>
<span data-ttu-id="2b463-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="2b463-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b463-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2b463-125">-PassThru</span></span>
<span data-ttu-id="2b463-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2b463-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b463-127">-ResourceGroupName</span></span>
<span data-ttu-id="2b463-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-128">The name of the resource group.</span></span>
<span data-ttu-id="2b463-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b463-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2b463-130">-ServerName</span></span>
<span data-ttu-id="2b463-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b463-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b463-132">-SubscriptionId</span></span>
<span data-ttu-id="2b463-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-133">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b463-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b463-134">-Confirm</span></span>
<span data-ttu-id="2b463-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b463-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b463-136">-WhatIf</span></span>
<span data-ttu-id="2b463-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2b463-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b463-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b463-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b463-139">CommonParameters</span></span>
<span data-ttu-id="2b463-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b463-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b463-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b463-142">입력</span><span class="sxs-lookup"><span data-stu-id="2b463-142">INPUTS</span></span>

### <span data-ttu-id="2b463-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="2b463-143">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="2b463-144">출력</span><span class="sxs-lookup"><span data-stu-id="2b463-144">OUTPUTS</span></span>

### <span data-ttu-id="2b463-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2b463-145">System.Boolean</span></span>

## <span data-ttu-id="2b463-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2b463-146">NOTES</span></span>

<span data-ttu-id="2b463-147">별칭</span><span class="sxs-lookup"><span data-stu-id="2b463-147">ALIASES</span></span>

<span data-ttu-id="2b463-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2b463-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2b463-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b463-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2b463-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2b463-151">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b463-151">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b463-152">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2b463-153">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2b463-154">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2b463-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2b463-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b463-156">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-156">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="2b463-157">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-157">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2b463-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-158">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2b463-159">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-159">The name is case insensitive.</span></span>
  - <span data-ttu-id="2b463-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-160">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2b463-161">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-161">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2b463-162">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-162">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2b463-163">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b463-163">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2b463-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b463-164">RELATED LINKS</span></span>

