---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494620"
---
# <span data-ttu-id="6ebcd-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="6ebcd-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="6ebcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ebcd-102">SYNOPSIS</span></span>
<span data-ttu-id="6ebcd-103">작업 영역의 vNet 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="6ebcd-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ebcd-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6ebcd-105">설명</span><span class="sxs-lookup"><span data-stu-id="6ebcd-105">DESCRIPTION</span></span>
<span data-ttu-id="6ebcd-106">작업 영역의 vNet 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="6ebcd-107">예제</span><span class="sxs-lookup"><span data-stu-id="6ebcd-107">EXAMPLES</span></span>

### <span data-ttu-id="6ebcd-108">예제 1: databricks에 대한 vnet 피어링 만들기</span><span class="sxs-lookup"><span data-stu-id="6ebcd-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="6ebcd-109">이 명령은 databricks에 대한 vnet 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="6ebcd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ebcd-110">PARAMETERS</span></span>

### <span data-ttu-id="6ebcd-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="6ebcd-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="6ebcd-112">로컬 가상 네트워크의 VM에서 전달된 트래픽이 원격 가상 네트워크에서 허용/허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="6ebcd-113">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="6ebcd-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="6ebcd-114">게이트웨이 링크를 원격 가상 네트워킹에서 사용하여 이 가상 네트워크에 연결하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="6ebcd-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="6ebcd-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="6ebcd-116">로컬 가상 네트워크 공간의 VM이 원격 가상 네트워크 공간의 VM에 액세스할 수 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="6ebcd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ebcd-117">-AsJob</span></span>
<span data-ttu-id="6ebcd-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="6ebcd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="6ebcd-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="6ebcd-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="6ebcd-120">CIDR 표시로 이 가상 네트워크에 예약된 주소 블록 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebcd-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ebcd-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="6ebcd-122">databricks 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="6ebcd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ebcd-123">-DefaultProfile</span></span>
<span data-ttu-id="6ebcd-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ebcd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ebcd-125">-Name</span></span>
<span data-ttu-id="6ebcd-126">작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="6ebcd-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="6ebcd-127">-NoWait</span></span>
<span data-ttu-id="6ebcd-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="6ebcd-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6ebcd-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="6ebcd-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="6ebcd-130">CIDR 표시로 이 가상 네트워크에 예약된 주소 블록 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ebcd-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ebcd-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="6ebcd-132">원격 가상 네트워크의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="6ebcd-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ebcd-133">-ResourceGroupName</span></span>
<span data-ttu-id="6ebcd-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-134">The name of the resource group.</span></span>
<span data-ttu-id="6ebcd-135">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6ebcd-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ebcd-136">-SubscriptionId</span></span>
<span data-ttu-id="6ebcd-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6ebcd-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="6ebcd-138">-UseRemoteGateway</span></span>
<span data-ttu-id="6ebcd-139">이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="6ebcd-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="6ebcd-140">플래그가 true로 설정되어 있으며 원격 피어링의 allowGatewayTransit도 true이면 가상 네트워크는 전송을 위해 원격 가상 네트워크의 게이트웨이를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="6ebcd-141">한 피어링만 이 플래그를 true로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="6ebcd-142">가상 네트워크에 게이트웨이가 이미 있는 경우 이 플래그를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="6ebcd-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6ebcd-143">-WorkspaceName</span></span>
<span data-ttu-id="6ebcd-144">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="6ebcd-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ebcd-145">-Confirm</span></span>
<span data-ttu-id="6ebcd-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ebcd-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ebcd-147">-WhatIf</span></span>
<span data-ttu-id="6ebcd-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ebcd-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ebcd-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ebcd-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ebcd-150">CommonParameters</span></span>
<span data-ttu-id="6ebcd-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ebcd-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ebcd-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ebcd-153">입력</span><span class="sxs-lookup"><span data-stu-id="6ebcd-153">INPUTS</span></span>

## <span data-ttu-id="6ebcd-154">출력</span><span class="sxs-lookup"><span data-stu-id="6ebcd-154">OUTPUTS</span></span>

### <span data-ttu-id="6ebcd-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="6ebcd-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="6ebcd-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ebcd-156">NOTES</span></span>

<span data-ttu-id="6ebcd-157">별칭</span><span class="sxs-lookup"><span data-stu-id="6ebcd-157">ALIASES</span></span>

## <span data-ttu-id="6ebcd-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ebcd-158">RELATED LINKS</span></span>

