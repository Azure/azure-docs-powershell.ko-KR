---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e063af1a489c9e68845f087e339f42de65281501
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374193"
---
# <span data-ttu-id="19271-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="19271-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="19271-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19271-102">SYNOPSIS</span></span>
<span data-ttu-id="19271-103">Unregister-AzStackHCI 프레미스 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 삭제하고 Azure를 사용하여 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19271-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="19271-104">매개 변수가 전달되지 않은 경우 클러스터에서 사용할 수 있는 등록된 정보를 사용하여 클러스터를 등록을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="19271-105">구문</span><span class="sxs-lookup"><span data-stu-id="19271-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19271-106">설명</span><span class="sxs-lookup"><span data-stu-id="19271-106">DESCRIPTION</span></span>
<span data-ttu-id="19271-107">Unregister-AzStackHCI 프레미스 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 삭제하고 Azure를 사용하여 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19271-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="19271-108">매개 변수가 전달되지 않은 경우 클러스터에서 사용할 수 있는 등록된 정보를 사용하여 클러스터를 등록을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="19271-109">예제</span><span class="sxs-lookup"><span data-stu-id="19271-109">EXAMPLES</span></span>

### <span data-ttu-id="19271-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="19271-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="19271-111">C:\PS \> Unregister-AzStackHCI 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="19271-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="19271-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="19271-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="19271-113">C:\PS \> Unregister-AzStackHCI -ComputerName ClusterNode1 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="19271-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="19271-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="19271-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="19271-115">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span><span class="sxs-lookup"><span data-stu-id="19271-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="19271-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="19271-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="19271-117">C:\PS \> Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span><span class="sxs-lookup"><span data-stu-id="19271-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="19271-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19271-118">PARAMETERS</span></span>

### <span data-ttu-id="19271-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="19271-119">-AccountId</span></span>
<span data-ttu-id="19271-120">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="19271-121">ArmAccessToken 및 GraphAccessToken과 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="19271-122">-ArmAccessToken</span></span>
<span data-ttu-id="19271-123">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="19271-124">GraphAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="19271-125">-ComputerName</span></span>
<span data-ttu-id="19271-126">Azure에 등록되는 클러스터의 클러스터 노드 중 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="19271-127">-Credential</span></span>
<span data-ttu-id="19271-128">ComputerName의 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="19271-129">기본값은 Cmdlet을 실행하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="19271-129">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="19271-130">-EnvironmentName</span></span>
<span data-ttu-id="19271-131">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="19271-132">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="19271-132">Default is AzureCloud.</span></span>
<span data-ttu-id="19271-133">유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="19271-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="19271-134">-GraphAccessToken</span></span>
<span data-ttu-id="19271-135">Graph 액세스 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="19271-136">ArmAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19271-137">-ResourceGroupName</span></span>
<span data-ttu-id="19271-138">Azure 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="19271-139">지정하지 않으면 \<LocalClusterName\> -rg가 리소스 그룹 이름으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="19271-140">-ResourceName</span></span>
<span data-ttu-id="19271-141">Azure에서 만든 리소스의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="19271-142">지정하지 않으면, 프레미스 클러스터 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-142">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="19271-143">-SubscriptionId</span></span>
<span data-ttu-id="19271-144">리소스를 만들 Azure 구독을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-144">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="19271-145">-TenantId</span></span>
<span data-ttu-id="19271-146">Azure TenantId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-146">Specifies the Azure TenantId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="19271-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="19271-148">대화형 브라우저 프롬프트 대신 디바이스 코드 인증을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-148">Use device code authentication instead of an interactive browser prompt.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19271-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19271-149">-Confirm</span></span>
<span data-ttu-id="19271-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19271-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19271-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19271-151">-WhatIf</span></span>
<span data-ttu-id="19271-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="19271-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19271-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19271-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19271-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19271-154">CommonParameters</span></span>
<span data-ttu-id="19271-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19271-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19271-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19271-157">입력</span><span class="sxs-lookup"><span data-stu-id="19271-157">INPUTS</span></span>

## <span data-ttu-id="19271-158">출력</span><span class="sxs-lookup"><span data-stu-id="19271-158">OUTPUTS</span></span>

### <span data-ttu-id="19271-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="19271-159">PSCustomObject.</span></span> <span data-ttu-id="19271-160">PSCustomObject에서 다음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="19271-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="19271-161">결과: 성공 또는 실패 또는 취소.</span><span class="sxs-lookup"><span data-stu-id="19271-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="19271-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19271-162">NOTES</span></span>

## <span data-ttu-id="19271-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19271-163">RELATED LINKS</span></span>
