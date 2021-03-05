---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/new-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/New-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: cfbbfd9472d18d75dea3da68cb4d2e06cf54c9a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970571"
---
# <span data-ttu-id="79027-101">New-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="79027-101">New-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="79027-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79027-102">SYNOPSIS</span></span>
<span data-ttu-id="79027-103">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="79027-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="79027-104">구문</span><span class="sxs-lookup"><span data-stu-id="79027-104">SYNTAX</span></span>

```
New-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="79027-105">설명</span><span class="sxs-lookup"><span data-stu-id="79027-105">DESCRIPTION</span></span>
<span data-ttu-id="79027-106">기존 가상 네트워크 규칙을 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="79027-106">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="79027-107">예제</span><span class="sxs-lookup"><span data-stu-id="79027-107">EXAMPLES</span></span>

### <span data-ttu-id="79027-108">예제 1: MariaDB에 대한 가상 네트워크 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="79027-108">Example 1: Create a virtual network rule for a MariaDB</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> New-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnet-001 -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name     Type
----     ----
vnet-001 Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="79027-109">이 명령은 MariaDB에 대한 가상 네트워크 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79027-109">This command creates a virtual network rule for a MariaDB.</span></span>

## <span data-ttu-id="79027-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="79027-110">PARAMETERS</span></span>

### <span data-ttu-id="79027-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79027-111">-AsJob</span></span>
<span data-ttu-id="79027-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="79027-112">Run the command as a job</span></span>

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

### <span data-ttu-id="79027-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79027-113">-DefaultProfile</span></span>
<span data-ttu-id="79027-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79027-115">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="79027-115">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="79027-116">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만드기</span><span class="sxs-lookup"><span data-stu-id="79027-116">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="79027-117">-Name</span><span class="sxs-lookup"><span data-stu-id="79027-117">-Name</span></span>
<span data-ttu-id="79027-118">가상 네트워크 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-118">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="79027-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="79027-119">-NoWait</span></span>
<span data-ttu-id="79027-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="79027-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="79027-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79027-121">-PassThru</span></span>
<span data-ttu-id="79027-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="79027-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="79027-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79027-123">-ResourceGroupName</span></span>
<span data-ttu-id="79027-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="79027-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79027-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="79027-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="79027-126">-ServerName</span></span>
<span data-ttu-id="79027-127">서버의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-127">The name of the server.</span></span>

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

### <span data-ttu-id="79027-128">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="79027-128">-SubnetId</span></span>
<span data-ttu-id="79027-129">가상 ARM 서브넷의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-129">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="79027-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="79027-130">-SubscriptionId</span></span>
<span data-ttu-id="79027-131">Azure 구독을 식별하는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79027-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="79027-132">-확인</span><span class="sxs-lookup"><span data-stu-id="79027-132">-Confirm</span></span>
<span data-ttu-id="79027-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79027-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79027-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79027-134">-WhatIf</span></span>
<span data-ttu-id="79027-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="79027-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79027-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79027-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79027-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79027-137">CommonParameters</span></span>
<span data-ttu-id="79027-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79027-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79027-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79027-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79027-140">입력</span><span class="sxs-lookup"><span data-stu-id="79027-140">INPUTS</span></span>

## <span data-ttu-id="79027-141">출력</span><span class="sxs-lookup"><span data-stu-id="79027-141">OUTPUTS</span></span>

### <span data-ttu-id="79027-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="79027-142">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="79027-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79027-143">NOTES</span></span>

<span data-ttu-id="79027-144">별칭</span><span class="sxs-lookup"><span data-stu-id="79027-144">ALIASES</span></span>

## <span data-ttu-id="79027-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79027-145">RELATED LINKS</span></span>

