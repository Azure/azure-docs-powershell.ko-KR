---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189377"
---
# <span data-ttu-id="d3fa1-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3fa1-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="d3fa1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3fa1-102">SYNOPSIS</span></span>
<span data-ttu-id="d3fa1-103">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d3fa1-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3fa1-104">SYNTAX</span></span>

### <span data-ttu-id="d3fa1-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3fa1-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3fa1-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d3fa1-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3fa1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3fa1-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3fa1-108">설명</span><span class="sxs-lookup"><span data-stu-id="d3fa1-108">DESCRIPTION</span></span>
<span data-ttu-id="d3fa1-109">서버 방화벽 규칙에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="d3fa1-110">예제</span><span class="sxs-lookup"><span data-stu-id="d3fa1-110">EXAMPLES</span></span>

### <span data-ttu-id="d3fa1-111">예제 1: 지정된 PostgreSql 서버의 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d3fa1-112">이 cmdlet은 지정된 PostgreSql 서버의 모든 방화벽 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="d3fa1-113">예제 2: 이름에 의해 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="d3fa1-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d3fa1-114">이 cmdlet은 이름으로 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="d3fa1-115">예제 3: ID로 방화벽 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="d3fa1-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="d3fa1-116">이 cmdlet은 ID에 의해 방화벽 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="d3fa1-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3fa1-117">PARAMETERS</span></span>

### <span data-ttu-id="d3fa1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3fa1-118">-DefaultProfile</span></span>
<span data-ttu-id="d3fa1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3fa1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3fa1-120">-InputObject</span></span>
<span data-ttu-id="d3fa1-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3fa1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d3fa1-122">-Name</span></span>
<span data-ttu-id="d3fa1-123">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="d3fa1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3fa1-124">-ResourceGroupName</span></span>
<span data-ttu-id="d3fa1-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-125">The name of the resource group.</span></span>
<span data-ttu-id="d3fa1-126">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d3fa1-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d3fa1-127">-ServerName</span></span>
<span data-ttu-id="d3fa1-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-128">The name of the server.</span></span>

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

### <span data-ttu-id="d3fa1-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3fa1-129">-SubscriptionId</span></span>
<span data-ttu-id="d3fa1-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d3fa1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3fa1-131">CommonParameters</span></span>
<span data-ttu-id="d3fa1-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3fa1-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3fa1-134">입력</span><span class="sxs-lookup"><span data-stu-id="d3fa1-134">INPUTS</span></span>

### <span data-ttu-id="d3fa1-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d3fa1-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="d3fa1-136">출력</span><span class="sxs-lookup"><span data-stu-id="d3fa1-136">OUTPUTS</span></span>

### <span data-ttu-id="d3fa1-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span><span class="sxs-lookup"><span data-stu-id="d3fa1-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="d3fa1-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3fa1-138">NOTES</span></span>

<span data-ttu-id="d3fa1-139">별칭</span><span class="sxs-lookup"><span data-stu-id="d3fa1-139">ALIASES</span></span>

<span data-ttu-id="d3fa1-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d3fa1-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d3fa1-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3fa1-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d3fa1-143">INPUTOBJECT: <IPostgreSqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3fa1-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3fa1-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d3fa1-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d3fa1-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d3fa1-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d3fa1-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3fa1-148">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d3fa1-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d3fa1-150">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="d3fa1-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d3fa1-152">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d3fa1-153">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d3fa1-154">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3fa1-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d3fa1-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3fa1-155">RELATED LINKS</span></span>

