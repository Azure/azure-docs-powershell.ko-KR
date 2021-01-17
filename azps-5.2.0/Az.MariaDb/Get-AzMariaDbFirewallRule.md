---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369958"
---
# <span data-ttu-id="0fc2b-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0fc2b-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="0fc2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fc2b-102">SYNOPSIS</span></span>
<span data-ttu-id="0fc2b-103">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0fc2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fc2b-104">SYNTAX</span></span>

### <span data-ttu-id="0fc2b-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="0fc2b-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0fc2b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0fc2b-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0fc2b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0fc2b-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0fc2b-108">설명</span><span class="sxs-lookup"><span data-stu-id="0fc2b-108">DESCRIPTION</span></span>
<span data-ttu-id="0fc2b-109">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="0fc2b-110">예제</span><span class="sxs-lookup"><span data-stu-id="0fc2b-110">EXAMPLES</span></span>

### <span data-ttu-id="0fc2b-111">예제 1: MariaDB 아래에 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="0fc2b-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="0fc2b-112">이 명령은 MariaDB의 모든 girewall 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="0fc2b-113">예제 2: MariaDB에서 방화벽 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="0fc2b-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="0fc2b-114">이 명령은 MariaDB에서 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="0fc2b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fc2b-115">PARAMETERS</span></span>

### <span data-ttu-id="0fc2b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fc2b-116">-DefaultProfile</span></span>
<span data-ttu-id="0fc2b-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fc2b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fc2b-118">-InputObject</span></span>
<span data-ttu-id="0fc2b-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fc2b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0fc2b-120">-Name</span></span>
<span data-ttu-id="0fc2b-121">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0fc2b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fc2b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0fc2b-123">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0fc2b-124">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0fc2b-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fc2b-125">-ServerName</span></span>
<span data-ttu-id="0fc2b-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-126">The name of the server.</span></span>

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

### <span data-ttu-id="0fc2b-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fc2b-127">-SubscriptionId</span></span>
<span data-ttu-id="0fc2b-128">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0fc2b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fc2b-129">CommonParameters</span></span>
<span data-ttu-id="0fc2b-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fc2b-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fc2b-132">입력</span><span class="sxs-lookup"><span data-stu-id="0fc2b-132">INPUTS</span></span>

### <span data-ttu-id="0fc2b-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="0fc2b-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="0fc2b-134">출력</span><span class="sxs-lookup"><span data-stu-id="0fc2b-134">OUTPUTS</span></span>

### <span data-ttu-id="0fc2b-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0fc2b-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="0fc2b-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fc2b-136">NOTES</span></span>

<span data-ttu-id="0fc2b-137">별칭</span><span class="sxs-lookup"><span data-stu-id="0fc2b-137">ALIASES</span></span>

<span data-ttu-id="0fc2b-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="0fc2b-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fc2b-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fc2b-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fc2b-141">INPUTOBJECT: <IMariaDbIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0fc2b-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fc2b-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0fc2b-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0fc2b-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0fc2b-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="0fc2b-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fc2b-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0fc2b-147">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0fc2b-148">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0fc2b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0fc2b-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0fc2b-151">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="0fc2b-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fc2b-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0fc2b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fc2b-153">RELATED LINKS</span></span>

