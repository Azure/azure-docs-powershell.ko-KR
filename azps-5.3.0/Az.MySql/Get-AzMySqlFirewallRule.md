---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: f750718c4bd380b579dff0897b53a68ae4f45b95
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490067"
---
# <span data-ttu-id="87331-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87331-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="87331-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87331-102">SYNOPSIS</span></span>
<span data-ttu-id="87331-103">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87331-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="87331-104">구문</span><span class="sxs-lookup"><span data-stu-id="87331-104">SYNTAX</span></span>

### <span data-ttu-id="87331-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="87331-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87331-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="87331-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="87331-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="87331-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="87331-108">설명</span><span class="sxs-lookup"><span data-stu-id="87331-108">DESCRIPTION</span></span>
<span data-ttu-id="87331-109">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87331-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="87331-110">예제</span><span class="sxs-lookup"><span data-stu-id="87331-110">EXAMPLES</span></span>

### <span data-ttu-id="87331-111">예제 1: 지정된 MySql 서버의 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="87331-112">이 cmdlet은 지정된 MySql 서버의 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="87331-113">예제 2: 이름에 의해 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="87331-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="87331-114">이 cmdlet은 이름으로 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87331-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="87331-115">예제 3: ID로 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="87331-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="87331-116">이 cmdlet은 ID에 의해 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="87331-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="87331-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="87331-117">PARAMETERS</span></span>

### <span data-ttu-id="87331-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87331-118">-DefaultProfile</span></span>
<span data-ttu-id="87331-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87331-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87331-120">-InputObject</span></span>
<span data-ttu-id="87331-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="87331-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="87331-122">-Name</span><span class="sxs-lookup"><span data-stu-id="87331-122">-Name</span></span>
<span data-ttu-id="87331-123">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-123">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87331-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87331-124">-ResourceGroupName</span></span>
<span data-ttu-id="87331-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-125">The name of the resource group.</span></span>
<span data-ttu-id="87331-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-126">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87331-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="87331-127">-ServerName</span></span>
<span data-ttu-id="87331-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-128">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87331-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="87331-129">-SubscriptionId</span></span>
<span data-ttu-id="87331-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87331-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87331-131">CommonParameters</span></span>
<span data-ttu-id="87331-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87331-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="87331-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87331-134">입력</span><span class="sxs-lookup"><span data-stu-id="87331-134">INPUTS</span></span>

### <span data-ttu-id="87331-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="87331-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="87331-136">출력</span><span class="sxs-lookup"><span data-stu-id="87331-136">OUTPUTS</span></span>

### <span data-ttu-id="87331-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="87331-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="87331-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="87331-138">NOTES</span></span>

<span data-ttu-id="87331-139">별칭</span><span class="sxs-lookup"><span data-stu-id="87331-139">ALIASES</span></span>

<span data-ttu-id="87331-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="87331-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="87331-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="87331-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="87331-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="87331-143">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="87331-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="87331-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="87331-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="87331-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="87331-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="87331-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="87331-148">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="87331-149">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="87331-150">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="87331-151">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="87331-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="87331-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="87331-153">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="87331-154">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="87331-155">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87331-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="87331-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87331-156">RELATED LINKS</span></span>

