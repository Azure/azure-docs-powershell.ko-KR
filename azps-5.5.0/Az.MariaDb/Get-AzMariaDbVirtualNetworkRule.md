---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190241"
---
# <span data-ttu-id="4b21e-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b21e-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="4b21e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b21e-102">SYNOPSIS</span></span>
<span data-ttu-id="4b21e-103">가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4b21e-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b21e-104">SYNTAX</span></span>

### <span data-ttu-id="4b21e-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b21e-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4b21e-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="4b21e-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="4b21e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4b21e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="4b21e-108">설명</span><span class="sxs-lookup"><span data-stu-id="4b21e-108">DESCRIPTION</span></span>
<span data-ttu-id="4b21e-109">가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="4b21e-110">예제</span><span class="sxs-lookup"><span data-stu-id="4b21e-110">EXAMPLES</span></span>

### <span data-ttu-id="4b21e-111">예제 1: MariaDB 아래에 모든 가상 네트워크 규칙 나열</span><span class="sxs-lookup"><span data-stu-id="4b21e-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="4b21e-112">이 명령은 MariaDB의 모든 가상 네트워크 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="4b21e-113">예제 2: MariaDB에서 가상 네트워크 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="4b21e-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="4b21e-114">이 명령은 MariaDB에서 가상 네트워크 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="4b21e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b21e-115">PARAMETERS</span></span>

### <span data-ttu-id="4b21e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b21e-116">-DefaultProfile</span></span>
<span data-ttu-id="4b21e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b21e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b21e-118">-InputObject</span></span>
<span data-ttu-id="4b21e-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="4b21e-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4b21e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4b21e-120">-Name</span></span>
<span data-ttu-id="4b21e-121">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="4b21e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b21e-122">-PassThru</span></span>
<span data-ttu-id="4b21e-123">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4b21e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b21e-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b21e-125">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4b21e-126">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4b21e-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4b21e-127">-ServerName</span></span>
<span data-ttu-id="4b21e-128">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-128">The name of the server.</span></span>

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

### <span data-ttu-id="4b21e-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4b21e-129">-SubscriptionId</span></span>
<span data-ttu-id="4b21e-130">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4b21e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b21e-131">CommonParameters</span></span>
<span data-ttu-id="4b21e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b21e-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b21e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b21e-134">입력</span><span class="sxs-lookup"><span data-stu-id="4b21e-134">INPUTS</span></span>

### <span data-ttu-id="4b21e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4b21e-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4b21e-136">출력</span><span class="sxs-lookup"><span data-stu-id="4b21e-136">OUTPUTS</span></span>

### <span data-ttu-id="4b21e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4b21e-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4b21e-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b21e-138">NOTES</span></span>

<span data-ttu-id="4b21e-139">별칭</span><span class="sxs-lookup"><span data-stu-id="4b21e-139">ALIASES</span></span>

<span data-ttu-id="4b21e-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="4b21e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4b21e-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4b21e-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4b21e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4b21e-143">INPUTOBJECT: <IMariaDbIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b21e-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4b21e-144">`[ConfigurationName <String>]`: 서버 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4b21e-145">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4b21e-146">`[FirewallRuleName <String>]`: 서버 방화벽 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4b21e-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="4b21e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4b21e-148">`[LocationName <String>]`: 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4b21e-149">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4b21e-150">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4b21e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: 보안 경고 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4b21e-152">`[ServerName <String>]`: 서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4b21e-153">`[SubscriptionId <String>]`: Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4b21e-154">`[VirtualNetworkRuleName <String>]`: 가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4b21e-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4b21e-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b21e-155">RELATED LINKS</span></span>

