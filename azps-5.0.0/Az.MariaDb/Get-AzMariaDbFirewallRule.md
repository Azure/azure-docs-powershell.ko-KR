---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbFirewallRule.md
ms.openlocfilehash: 2b2f52d8dc4f9e31a86b666b7ee81981fa6bd18c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218909"
---
# <span data-ttu-id="b7c40-101">Get-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b7c40-101">Get-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="b7c40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7c40-102">SYNOPSIS</span></span>
<span data-ttu-id="b7c40-103">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b7c40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7c40-104">SYNTAX</span></span>

### <span data-ttu-id="b7c40-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7c40-105">List (Default)</span></span>
```
Get-AzMariaDbFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7c40-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b7c40-106">Get</span></span>
```
Get-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7c40-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7c40-107">GetViaIdentity</span></span>
```
Get-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b7c40-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b7c40-108">DESCRIPTION</span></span>
<span data-ttu-id="b7c40-109">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="b7c40-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b7c40-110">EXAMPLES</span></span>

### <span data-ttu-id="b7c40-111">예제 1: 모든 방화벽 규칙을 예, 예 Adb로 나열</span><span class="sxs-lookup"><span data-stu-id="b7c40-111">Example 1: List all firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

Name       Type
----       ----
fr-cfgl3y  Microsoft.DBforMariaDB/servers/firewallRules
fr-usc9na  Microsoft.DBforMariaDB/servers/firewallRules
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="b7c40-112">이 명령은 모든 gid의 벽에 대 한 규칙을 \ n i n m b 아래에 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-112">This command lists all girewall rule under a MariaDB.</span></span>

### <span data-ttu-id="b7c40-113">예제 2: a 2 i 아래에 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="b7c40-113">Example 2: Get a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbFirewallRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig -Name frname-001

Name       Type
----       ----
frname-001 Microsoft.DBforMariaDB/servers/firewallRules
```

<span data-ttu-id="b7c40-114">이 명령은, 그 아래에 있는 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-114">This command gets a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="b7c40-115">변수</span><span class="sxs-lookup"><span data-stu-id="b7c40-115">PARAMETERS</span></span>

### <span data-ttu-id="b7c40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7c40-116">-DefaultProfile</span></span>
<span data-ttu-id="b7c40-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7c40-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7c40-118">-InputObject</span></span>
<span data-ttu-id="b7c40-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7c40-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b7c40-120">-Name</span></span>
<span data-ttu-id="b7c40-121">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-121">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="b7c40-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7c40-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7c40-123">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b7c40-124">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b7c40-125">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b7c40-125">-ServerName</span></span>
<span data-ttu-id="b7c40-126">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-126">The name of the server.</span></span>

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

### <span data-ttu-id="b7c40-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7c40-127">-SubscriptionId</span></span>
<span data-ttu-id="b7c40-128">Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-128">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b7c40-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7c40-129">CommonParameters</span></span>
<span data-ttu-id="b7c40-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7c40-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7c40-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7c40-132">입력</span><span class="sxs-lookup"><span data-stu-id="b7c40-132">INPUTS</span></span>

### <span data-ttu-id="b7c40-133">IMariaDbIdentity (Microsoft. PowerShell. m b.</span><span class="sxs-lookup"><span data-stu-id="b7c40-133">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b7c40-134">출력</span><span class="sxs-lookup"><span data-stu-id="b7c40-134">OUTPUTS</span></span>

### <span data-ttu-id="b7c40-135">Microsoft. Api20180601Preview. IFirewallRule에 대 한. b a r i.</span><span class="sxs-lookup"><span data-stu-id="b7c40-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IFirewallRule</span></span>

## <span data-ttu-id="b7c40-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b7c40-136">NOTES</span></span>

<span data-ttu-id="b7c40-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="b7c40-137">ALIASES</span></span>

<span data-ttu-id="b7c40-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b7c40-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7c40-139">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7c40-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7c40-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7c40-141">INPUTOBJECT <IMariaDbIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7c40-141">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7c40-142">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-142">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b7c40-143">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-143">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b7c40-144">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-144">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b7c40-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b7c40-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7c40-146">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b7c40-147">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-147">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b7c40-148">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-148">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b7c40-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b7c40-150">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b7c40-151">`[SubscriptionId <String>]`: Azure 구독을 식별 하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-151">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b7c40-152">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7c40-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b7c40-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7c40-153">RELATED LINKS</span></span>

