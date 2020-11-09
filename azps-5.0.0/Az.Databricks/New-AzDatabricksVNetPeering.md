---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/new-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/New-AzDatabricksVNetPeering.md
ms.openlocfilehash: f1af71bd2c05f2b1219a3ad7f1f09eb2f9560ad4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305075"
---
# <span data-ttu-id="d0710-101">New-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="d0710-101">New-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="d0710-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0710-102">SYNOPSIS</span></span>
<span data-ttu-id="d0710-103">작업 영역에 대 한 vNet 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-103">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="d0710-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d0710-104">SYNTAX</span></span>

```
New-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic] [-AllowGatewayTransit] [-AllowVirtualNetworkAccess]
 [-DatabricksAddressSpacePrefix <String[]>] [-DatabricksVirtualNetworkId <String>]
 [-RemoteAddressSpacePrefix <String[]>] [-RemoteVirtualNetworkId <String>] [-UseRemoteGateway]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d0710-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d0710-105">DESCRIPTION</span></span>
<span data-ttu-id="d0710-106">작업 영역에 대 한 vNet 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-106">Creates vNet Peering for workspace.</span></span>

## <span data-ttu-id="d0710-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d0710-107">EXAMPLES</span></span>

### <span data-ttu-id="d0710-108">예제 1: databricks 용 vnet 피어 링 만들기</span><span class="sxs-lookup"><span data-stu-id="d0710-108">Example 1: Create a vnet peering for databricks</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t01 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxxx-xxxx-xxx-xxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test01'

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="d0710-109">이 명령은 databricks에 대 한 vnet 피어 링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-109">This command creates a vnet peering for databricks.</span></span>

## <span data-ttu-id="d0710-110">변수</span><span class="sxs-lookup"><span data-stu-id="d0710-110">PARAMETERS</span></span>

### <span data-ttu-id="d0710-111">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="d0710-111">-AllowForwardedTraffic</span></span>
<span data-ttu-id="d0710-112">원격 가상 네트워크에서 로컬 가상 네트워크의 Vm 으로부터 전달 된 트래픽을 허용/허용 하지 않을 지 여부</span><span class="sxs-lookup"><span data-stu-id="d0710-112">Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="d0710-113">-Allow게이트웨이 전송</span><span class="sxs-lookup"><span data-stu-id="d0710-113">-AllowGatewayTransit</span></span>
<span data-ttu-id="d0710-114">원격 가상 네트워킹에서 게이트웨이 링크를 사용 하 여이 가상 네트워크에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-114">If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="d0710-115">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d0710-115">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="d0710-116">로컬 가상 네트워크 공간의 Vm이 원격 가상 네트워크 공간의 Vm에 액세스할 수 있는지 여부</span><span class="sxs-lookup"><span data-stu-id="d0710-116">Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="d0710-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0710-117">-AsJob</span></span>
<span data-ttu-id="d0710-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0710-118">Run the command as a job</span></span>

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

### <span data-ttu-id="d0710-119">-DatabricksAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="d0710-119">-DatabricksAddressSpacePrefix</span></span>
<span data-ttu-id="d0710-120">이 가상 네트워크에 대해 CIDR 표기법으로 예약 된 주소 블록 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-120">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="d0710-121">-DatabricksVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d0710-121">-DatabricksVirtualNetworkId</span></span>
<span data-ttu-id="d0710-122">Databricks 가상 네트워크의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-122">The Id of the databricks virtual network.</span></span>

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

### <span data-ttu-id="d0710-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0710-123">-DefaultProfile</span></span>
<span data-ttu-id="d0710-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0710-125">-이름</span><span class="sxs-lookup"><span data-stu-id="d0710-125">-Name</span></span>
<span data-ttu-id="d0710-126">작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-126">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="d0710-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d0710-127">-NoWait</span></span>
<span data-ttu-id="d0710-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d0710-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d0710-129">-RemoteAddressSpacePrefix</span><span class="sxs-lookup"><span data-stu-id="d0710-129">-RemoteAddressSpacePrefix</span></span>
<span data-ttu-id="d0710-130">이 가상 네트워크에 대해 CIDR 표기법으로 예약 된 주소 블록 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-130">A list of address blocks reserved for this virtual network in CIDR notation.</span></span>

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

### <span data-ttu-id="d0710-131">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d0710-131">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="d0710-132">원격 가상 네트워크의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-132">The Id of the remote virtual network.</span></span>

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

### <span data-ttu-id="d0710-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0710-133">-ResourceGroupName</span></span>
<span data-ttu-id="d0710-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-134">The name of the resource group.</span></span>
<span data-ttu-id="d0710-135">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-135">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d0710-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d0710-136">-SubscriptionId</span></span>
<span data-ttu-id="d0710-137">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d0710-138">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="d0710-138">-UseRemoteGateway</span></span>
<span data-ttu-id="d0710-139">이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="d0710-139">If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="d0710-140">플래그를 true로 설정 하 고 원격 피어 링에 대 한 Allow네트워크도 참이 면 가상 네트워크는 전송에 원격 가상 네트워크 게이트웨이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-140">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="d0710-141">한 번만 피어 링이이 플래그를 true로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-141">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="d0710-142">가상 네트워크에 이미 게이트웨이가 있는 경우이 플래그를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-142">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="d0710-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d0710-143">-WorkspaceName</span></span>
<span data-ttu-id="d0710-144">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-144">The name of the workspace.</span></span>

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

### <span data-ttu-id="d0710-145">-확인</span><span class="sxs-lookup"><span data-stu-id="d0710-145">-Confirm</span></span>
<span data-ttu-id="d0710-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0710-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0710-147">-WhatIf</span></span>
<span data-ttu-id="d0710-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0710-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0710-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0710-150">CommonParameters</span></span>
<span data-ttu-id="d0710-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d0710-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0710-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d0710-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0710-153">입력</span><span class="sxs-lookup"><span data-stu-id="d0710-153">INPUTS</span></span>

## <span data-ttu-id="d0710-154">출력</span><span class="sxs-lookup"><span data-stu-id="d0710-154">OUTPUTS</span></span>

### <span data-ttu-id="d0710-155">Databricks. Api20180401. IVirtualNetworkPeering에 대 한</span><span class="sxs-lookup"><span data-stu-id="d0710-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="d0710-156">상속자</span><span class="sxs-lookup"><span data-stu-id="d0710-156">NOTES</span></span>

<span data-ttu-id="d0710-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="d0710-157">ALIASES</span></span>

## <span data-ttu-id="d0710-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d0710-158">RELATED LINKS</span></span>

