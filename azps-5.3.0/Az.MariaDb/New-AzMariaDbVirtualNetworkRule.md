---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 77a89dec96e0e9b7ca7bd003f8368274edf6acdf
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492823"
---
# <span data-ttu-id="cc5e2-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cc5e2-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="cc5e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc5e2-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5e2-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cc5e2-104">구문</span><span class="sxs-lookup"><span data-stu-id="cc5e2-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc5e2-105">설명</span><span class="sxs-lookup"><span data-stu-id="cc5e2-105">DESCRIPTION</span></span>
<span data-ttu-id="cc5e2-106">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="cc5e2-107">예제</span><span class="sxs-lookup"><span data-stu-id="cc5e2-107">EXAMPLES</span></span>

### <span data-ttu-id="cc5e2-108">예제 1: MariaDB에 대한 가상 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="cc5e2-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="cc5e2-109">이 명령은 MariaDB에 대한 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="cc5e2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc5e2-110">PARAMETERS</span></span>

### <span data-ttu-id="cc5e2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc5e2-111">-AsJob</span></span>
<span data-ttu-id="cc5e2-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="cc5e2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="cc5e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5e2-113">-DefaultProfile</span></span>
<span data-ttu-id="cc5e2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5e2-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="cc5e2-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="cc5e2-116">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="cc5e2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cc5e2-117">-Name</span></span>
<span data-ttu-id="cc5e2-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-118">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5e2-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc5e2-119">-NoWait</span></span>
<span data-ttu-id="cc5e2-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="cc5e2-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc5e2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc5e2-121">-PassThru</span></span>
<span data-ttu-id="cc5e2-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc5e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="cc5e2-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cc5e2-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5e2-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cc5e2-126">-ServerName</span></span>
<span data-ttu-id="cc5e2-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-127">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5e2-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="cc5e2-128">-SubnetId</span></span>
<span data-ttu-id="cc5e2-129">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-129">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5e2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc5e2-130">-SubscriptionId</span></span>
<span data-ttu-id="cc5e2-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5e2-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc5e2-132">-Confirm</span></span>
<span data-ttu-id="cc5e2-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc5e2-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5e2-134">-WhatIf</span></span>
<span data-ttu-id="cc5e2-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cc5e2-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5e2-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc5e2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5e2-137">CommonParameters</span></span>
<span data-ttu-id="cc5e2-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5e2-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cc5e2-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5e2-140">입력</span><span class="sxs-lookup"><span data-stu-id="cc5e2-140">INPUTS</span></span>

## <span data-ttu-id="cc5e2-141">출력</span><span class="sxs-lookup"><span data-stu-id="cc5e2-141">OUTPUTS</span></span>

### <span data-ttu-id="cc5e2-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="cc5e2-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="cc5e2-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cc5e2-143">NOTES</span></span>

<span data-ttu-id="cc5e2-144">별칭</span><span class="sxs-lookup"><span data-stu-id="cc5e2-144">ALIASES</span></span>

## <span data-ttu-id="cc5e2-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cc5e2-145">RELATED LINKS</span></span>

