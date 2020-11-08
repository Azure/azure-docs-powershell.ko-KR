---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFirewallRule.md
ms.openlocfilehash: 11278c1d317f6f4e0171513a4503c5681506f1ac
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218595"
---
# <span data-ttu-id="9415d-101">Get-AzMySqlFirewallRule</span><span class="sxs-lookup"><span data-stu-id="9415d-101">Get-AzMySqlFirewallRule</span></span>

## <span data-ttu-id="9415d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9415d-102">SYNOPSIS</span></span>
<span data-ttu-id="9415d-103">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-103">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="9415d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9415d-104">SYNTAX</span></span>

### <span data-ttu-id="9415d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9415d-105">List (Default)</span></span>
```
Get-AzMySqlFirewallRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9415d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="9415d-106">Get</span></span>
```
Get-AzMySqlFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9415d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9415d-107">GetViaIdentity</span></span>
```
Get-AzMySqlFirewallRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="9415d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9415d-108">DESCRIPTION</span></span>
<span data-ttu-id="9415d-109">서버 방화벽 규칙에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-109">Gets information about a server firewall rule.</span></span>

## <span data-ttu-id="9415d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9415d-110">EXAMPLES</span></span>

### <span data-ttu-id="9415d-111">예제 1: 지정 된 MySql 서버의 모든 방화벽 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="9415d-111">Example 1: Lists all the Firewall Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="9415d-112">이 cmdlet에는 지정 된 MySql 서버의 모든 방화벽 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-112">This cmdlet lists all the Firewall Rule in specified MySql server.</span></span>

### <span data-ttu-id="9415d-113">예제 2: 이름별로 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="9415d-113">Example 2: Get Firewall Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlFirewallRule -Name rule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="9415d-114">이 cmdlet은 이름별로 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-114">This cmdlet gets Firewall Rule by name.</span></span>

### <span data-ttu-id="9415d-115">예제 3: id 별 방화벽 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="9415d-115">Example 3: Get Firewall Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/firewallRules/rule"
PS C:\> Get-AzMySqlFirewallRule -InputObject $ID

Name Type
---- ----
rule Microsoft.DBforMySQL/servers/firewallRules
```

<span data-ttu-id="9415d-116">이 cmdlet은 id 별 방화벽 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-116">This cmdlet gets Firewall Rule by identity.</span></span>

## <span data-ttu-id="9415d-117">변수</span><span class="sxs-lookup"><span data-stu-id="9415d-117">PARAMETERS</span></span>

### <span data-ttu-id="9415d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9415d-118">-DefaultProfile</span></span>
<span data-ttu-id="9415d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9415d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9415d-120">-InputObject</span></span>
<span data-ttu-id="9415d-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9415d-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9415d-122">-Name</span></span>
<span data-ttu-id="9415d-123">서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-123">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="9415d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9415d-124">-ResourceGroupName</span></span>
<span data-ttu-id="9415d-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-125">The name of the resource group.</span></span>
<span data-ttu-id="9415d-126">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9415d-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9415d-127">-ServerName</span></span>
<span data-ttu-id="9415d-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-128">The name of the server.</span></span>

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

### <span data-ttu-id="9415d-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9415d-129">-SubscriptionId</span></span>
<span data-ttu-id="9415d-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9415d-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9415d-131">CommonParameters</span></span>
<span data-ttu-id="9415d-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9415d-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9415d-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9415d-134">입력</span><span class="sxs-lookup"><span data-stu-id="9415d-134">INPUTS</span></span>

### <span data-ttu-id="9415d-135">IMySqlIdentity (Microsoft. PowerShell)</span><span class="sxs-lookup"><span data-stu-id="9415d-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="9415d-136">출력</span><span class="sxs-lookup"><span data-stu-id="9415d-136">OUTPUTS</span></span>

### <span data-ttu-id="9415d-137">Api20171201. IFirewallRule에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9415d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IFirewallRule</span></span>

## <span data-ttu-id="9415d-138">상속자</span><span class="sxs-lookup"><span data-stu-id="9415d-138">NOTES</span></span>

<span data-ttu-id="9415d-139">별칭과</span><span class="sxs-lookup"><span data-stu-id="9415d-139">ALIASES</span></span>

<span data-ttu-id="9415d-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="9415d-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9415d-141">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9415d-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9415d-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9415d-143">INPUTOBJECT <IMySqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9415d-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9415d-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9415d-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9415d-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9415d-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9415d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9415d-148">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9415d-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9415d-150">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-150">The name is case insensitive.</span></span>
  - <span data-ttu-id="9415d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9415d-152">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9415d-153">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-153">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9415d-154">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9415d-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9415d-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9415d-155">RELATED LINKS</span></span>

