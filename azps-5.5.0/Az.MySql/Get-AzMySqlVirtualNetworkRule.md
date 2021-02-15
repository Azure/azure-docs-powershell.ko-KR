---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184900"
---
# <span data-ttu-id="7f2d6-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7f2d6-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="7f2d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="7f2d6-103">가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="7f2d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="7f2d6-104">SYNTAX</span></span>

### <span data-ttu-id="7f2d6-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="7f2d6-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7f2d6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="7f2d6-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7f2d6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7f2d6-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="7f2d6-108">설명</span><span class="sxs-lookup"><span data-stu-id="7f2d6-108">DESCRIPTION</span></span>
<span data-ttu-id="7f2d6-109">가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="7f2d6-110">예제</span><span class="sxs-lookup"><span data-stu-id="7f2d6-110">EXAMPLES</span></span>

### <span data-ttu-id="7f2d6-111">예제 1: 지정된 MySql 서버의 모든 Virtual Network 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="7f2d6-112">이 cmdlet은 지정된 MySql 서버의 모든 Virtual Network 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="7f2d6-113">예제 2: 이름으로 Virtual Network 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="7f2d6-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="7f2d6-114">이 cmdlet은 이름으로 Virtual Network 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="7f2d6-115">예제 3: ID로 Virtual Network 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="7f2d6-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="7f2d6-116">이 cmdlet은 ID에 의해 Virtual Network 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="7f2d6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f2d6-117">PARAMETERS</span></span>

### <span data-ttu-id="7f2d6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f2d6-118">-DefaultProfile</span></span>
<span data-ttu-id="7f2d6-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f2d6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f2d6-120">-InputObject</span></span>
<span data-ttu-id="7f2d6-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7f2d6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7f2d6-122">-Name</span></span>
<span data-ttu-id="7f2d6-123">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f2d6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7f2d6-124">-PassThru</span></span>
<span data-ttu-id="7f2d6-125">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7f2d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f2d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="7f2d6-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-127">The name of the resource group.</span></span>
<span data-ttu-id="7f2d6-128">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="7f2d6-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7f2d6-129">-ServerName</span></span>
<span data-ttu-id="7f2d6-130">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-130">The name of the server.</span></span>

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

### <span data-ttu-id="7f2d6-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7f2d6-131">-SubscriptionId</span></span>
<span data-ttu-id="7f2d6-132">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="7f2d6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f2d6-133">CommonParameters</span></span>
<span data-ttu-id="7f2d6-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f2d6-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f2d6-136">입력</span><span class="sxs-lookup"><span data-stu-id="7f2d6-136">INPUTS</span></span>

### <span data-ttu-id="7f2d6-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="7f2d6-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="7f2d6-138">출력</span><span class="sxs-lookup"><span data-stu-id="7f2d6-138">OUTPUTS</span></span>

### <span data-ttu-id="7f2d6-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="7f2d6-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="7f2d6-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f2d6-140">NOTES</span></span>

<span data-ttu-id="7f2d6-141">별칭</span><span class="sxs-lookup"><span data-stu-id="7f2d6-141">ALIASES</span></span>

<span data-ttu-id="7f2d6-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="7f2d6-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7f2d6-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7f2d6-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7f2d6-145">INPUTOBJECT: <IMySqlIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="7f2d6-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7f2d6-146">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="7f2d6-147">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="7f2d6-148">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="7f2d6-149">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="7f2d6-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7f2d6-150">`[KeyName <String>]`: 서버 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="7f2d6-151">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="7f2d6-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="7f2d6-153">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="7f2d6-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="7f2d6-155">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="7f2d6-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="7f2d6-157">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f2d6-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="7f2d6-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f2d6-158">RELATED LINKS</span></span>

