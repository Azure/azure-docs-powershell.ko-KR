---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: 27f03ba80a01997d61bc50f6a644b4e3c4cffb7b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331190"
---
# <span data-ttu-id="297d2-101">Remove-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="297d2-101">Remove-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="297d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="297d2-102">SYNOPSIS</span></span>
<span data-ttu-id="297d2-103">서버 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="297d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="297d2-104">SYNTAX</span></span>

### <span data-ttu-id="297d2-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="297d2-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="297d2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="297d2-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="297d2-107">설명</span><span class="sxs-lookup"><span data-stu-id="297d2-107">DESCRIPTION</span></span>
<span data-ttu-id="297d2-108">서버 방화벽 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="297d2-109">예제</span><span class="sxs-lookup"><span data-stu-id="297d2-109">EXAMPLES</span></span>

### <span data-ttu-id="297d2-110">예제 1: 이름으로 PostgreSql 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="297d2-110">Example 1: Remove PostgreSql Firewall Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="297d2-111">이 cmdlet은 이름으로 PostgreSql 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-111">This cmdlet removes PostgreSql Firewall Rule by name.</span></span>

### <span data-ttu-id="297d2-112">예제 2: ID로 PostgreSql 방화벽 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="297d2-112">Example 2: Remove PostgreSql Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Remove-AzPostgreSqlFirewallRule -InputObject $ID
 
```

<span data-ttu-id="297d2-113">이러한 cmdlet은 ID에 의해 PostgreSql 방화벽 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-113">These cmdlets remove PostgreSql Firewall Rule by identity.</span></span>

## <span data-ttu-id="297d2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="297d2-114">PARAMETERS</span></span>

### <span data-ttu-id="297d2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="297d2-115">-AsJob</span></span>
<span data-ttu-id="297d2-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="297d2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="297d2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297d2-117">-DefaultProfile</span></span>
<span data-ttu-id="297d2-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297d2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="297d2-119">-InputObject</span></span>
<span data-ttu-id="297d2-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="297d2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="297d2-121">-Name</span><span class="sxs-lookup"><span data-stu-id="297d2-121">-Name</span></span>
<span data-ttu-id="297d2-122">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-122">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="297d2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="297d2-123">-NoWait</span></span>
<span data-ttu-id="297d2-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="297d2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="297d2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="297d2-125">-PassThru</span></span>
<span data-ttu-id="297d2-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="297d2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297d2-127">-ResourceGroupName</span></span>
<span data-ttu-id="297d2-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-128">The name of the resource group.</span></span>
<span data-ttu-id="297d2-129">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="297d2-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="297d2-130">-ServerName</span></span>
<span data-ttu-id="297d2-131">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-131">The name of the server.</span></span>

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

### <span data-ttu-id="297d2-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="297d2-132">-SubscriptionId</span></span>
<span data-ttu-id="297d2-133">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="297d2-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="297d2-134">-Confirm</span></span>
<span data-ttu-id="297d2-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297d2-136">-WhatIf</span></span>
<span data-ttu-id="297d2-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="297d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="297d2-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297d2-139">CommonParameters</span></span>
<span data-ttu-id="297d2-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297d2-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="297d2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297d2-142">입력</span><span class="sxs-lookup"><span data-stu-id="297d2-142">INPUTS</span></span>

### <span data-ttu-id="297d2-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="297d2-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="297d2-144">출력</span><span class="sxs-lookup"><span data-stu-id="297d2-144">OUTPUTS</span></span>

### <span data-ttu-id="297d2-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="297d2-145">System.Boolean</span></span>

## <span data-ttu-id="297d2-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="297d2-146">NOTES</span></span>

<span data-ttu-id="297d2-147">별칭</span><span class="sxs-lookup"><span data-stu-id="297d2-147">ALIASES</span></span>

<span data-ttu-id="297d2-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="297d2-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="297d2-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="297d2-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="297d2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="297d2-151">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="297d2-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="297d2-152">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="297d2-153">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="297d2-154">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="297d2-155">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="297d2-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="297d2-156">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="297d2-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="297d2-158">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="297d2-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="297d2-160">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="297d2-161">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="297d2-162">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="297d2-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="297d2-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="297d2-163">RELATED LINKS</span></span>

