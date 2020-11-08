---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlFirewallRule.md
ms.openlocfilehash: a5691b1d8181d210770802c8d3aa4526b6bd72f2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204940"
---
# <span data-ttu-id="9a241-101">Get-AzPostgreSqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9a241-101">Get-AzPostgreSqlFirewallRule</span></span>

## <span data-ttu-id="9a241-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a241-102">SYNOPSIS</span></span>
<span data-ttu-id="9a241-103">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="9a241-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a241-104">SYNTAX</span></span>

### <span data-ttu-id="9a241-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a241-105">List (Default)</span></span>
```
Get-AzPostgreSqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9a241-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9a241-106">Get</span></span>
```
Get-AzPostgreSqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9a241-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a241-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlFirewallRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a241-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a241-108">DESCRIPTION</span></span>
<span data-ttu-id="9a241-109">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="9a241-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9a241-110">EXAMPLES</span></span>

### <span data-ttu-id="9a241-111">예제 1: 지정 된 PostgreSql server의 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="9a241-111">Example 1: Lists all the Firewall Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="9a241-112">이 cmdlet에는 지정 된 PostgreSql server의 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-112">This cmdlet lists all the Firewall Rule in specified PostgreSql server.</span></span>

### <span data-ttu-id="9a241-113">예제 2: 이름별로 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a241-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlFirewallRule -Name rule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="9a241-114">이 cmdlet은 이름별로 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="9a241-115">예제 3: id 별 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="9a241-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/firewallRules/rule"
PS C:\> Get-AzPostgreSqlFirewallRule -InputObject $ID

Name StartIPAddress EndIPAddress
---- -------------- ------------
rule 0.0.0.0        0.0.0.1
```

<span data-ttu-id="9a241-116">이 cmdlet은 id 별 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="9a241-117">변수</span><span class="sxs-lookup"><span data-stu-id="9a241-117">PARAMETERS</span></span>

### <span data-ttu-id="9a241-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a241-118">-DefaultProfile</span></span>
<span data-ttu-id="9a241-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a241-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a241-120">-InputObject</span></span>
<span data-ttu-id="9a241-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9a241-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9a241-122">-Name</span></span>
<span data-ttu-id="9a241-123">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9a241-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a241-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a241-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-125">The name of the resource group.</span></span>
<span data-ttu-id="9a241-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9a241-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9a241-127">-ServerName</span></span>
<span data-ttu-id="9a241-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-128">The name of the server.</span></span>

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

### <span data-ttu-id="9a241-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a241-129">-SubscriptionId</span></span>
<span data-ttu-id="9a241-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9a241-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a241-131">CommonParameters</span></span>
<span data-ttu-id="9a241-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a241-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a241-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a241-134">입력</span><span class="sxs-lookup"><span data-stu-id="9a241-134">INPUTS</span></span>

### <span data-ttu-id="9a241-135">PostgreSql. IPostgreSqlIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a241-135">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9a241-136">출력</span><span class="sxs-lookup"><span data-stu-id="9a241-136">OUTPUTS</span></span>

### <span data-ttu-id="9a241-137">PostgreSql. Api20171201. IFirewallRule에 대 한</span><span class="sxs-lookup"><span data-stu-id="9a241-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="9a241-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9a241-138">NOTES</span></span>

<span data-ttu-id="9a241-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="9a241-139">ALIASES</span></span>

<span data-ttu-id="9a241-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9a241-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a241-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a241-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a241-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a241-143">INPUTOBJECT <IPostgreSqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9a241-143">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a241-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9a241-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9a241-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9a241-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9a241-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a241-148">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9a241-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9a241-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="9a241-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9a241-152">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9a241-153">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9a241-154">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a241-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9a241-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a241-155">RELATED LINKS</span></span>

