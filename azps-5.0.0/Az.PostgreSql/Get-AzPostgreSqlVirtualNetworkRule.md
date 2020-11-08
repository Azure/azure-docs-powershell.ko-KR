---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94219182"
---
# <span data-ttu-id="880e1-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="880e1-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="880e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="880e1-102">SYNOPSIS</span></span>
<span data-ttu-id="880e1-103">가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="880e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="880e1-104">SYNTAX</span></span>

### <span data-ttu-id="880e1-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="880e1-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="880e1-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="880e1-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="880e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="880e1-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="880e1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="880e1-108">DESCRIPTION</span></span>
<span data-ttu-id="880e1-109">가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="880e1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="880e1-110">EXAMPLES</span></span>

### <span data-ttu-id="880e1-111">예제 1: 지정 된 PostgreSql server의 모든 가상 네트워크 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="880e1-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="880e1-112">이 cmdlet에는 지정 된 PostgreSql server의 모든 가상 네트워크 규칙이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="880e1-113">예제 2: 이름별로 가상 네트워크 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="880e1-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="880e1-114">이 cmdlet은 이름을 기준으로 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="880e1-115">예제 3: id를 기준으로 가상 네트워크 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="880e1-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="880e1-116">이 cmdlet은 id를 기준으로 가상 네트워크 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="880e1-117">변수</span><span class="sxs-lookup"><span data-stu-id="880e1-117">PARAMETERS</span></span>

### <span data-ttu-id="880e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="880e1-118">-DefaultProfile</span></span>
<span data-ttu-id="880e1-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="880e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="880e1-120">-InputObject</span></span>
<span data-ttu-id="880e1-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="880e1-122">-이름</span><span class="sxs-lookup"><span data-stu-id="880e1-122">-Name</span></span>
<span data-ttu-id="880e1-123">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="880e1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="880e1-124">-PassThru</span></span>
<span data-ttu-id="880e1-125">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="880e1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="880e1-126">-ResourceGroupName</span></span>
<span data-ttu-id="880e1-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-127">The name of the resource group.</span></span>
<span data-ttu-id="880e1-128">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="880e1-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="880e1-129">-ServerName</span></span>
<span data-ttu-id="880e1-130">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-130">The name of the server.</span></span>

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

### <span data-ttu-id="880e1-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="880e1-131">-SubscriptionId</span></span>
<span data-ttu-id="880e1-132">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="880e1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="880e1-133">CommonParameters</span></span>
<span data-ttu-id="880e1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="880e1-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="880e1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="880e1-136">입력</span><span class="sxs-lookup"><span data-stu-id="880e1-136">INPUTS</span></span>

### <span data-ttu-id="880e1-137">PostgreSql. IPostgreSqlIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="880e1-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="880e1-138">출력</span><span class="sxs-lookup"><span data-stu-id="880e1-138">OUTPUTS</span></span>

### <span data-ttu-id="880e1-139">PostgreSql. Api20171201. IVirtualNetworkRule에 대 한</span><span class="sxs-lookup"><span data-stu-id="880e1-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="880e1-140">상속자</span><span class="sxs-lookup"><span data-stu-id="880e1-140">NOTES</span></span>

<span data-ttu-id="880e1-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="880e1-141">ALIASES</span></span>

<span data-ttu-id="880e1-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="880e1-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="880e1-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="880e1-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="880e1-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="880e1-145">INPUTOBJECT <IPostgreSqlIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="880e1-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="880e1-146">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="880e1-147">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="880e1-148">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="880e1-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="880e1-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="880e1-150">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="880e1-151">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="880e1-152">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="880e1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="880e1-154">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="880e1-155">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="880e1-156">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="880e1-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="880e1-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="880e1-157">RELATED LINKS</span></span>

