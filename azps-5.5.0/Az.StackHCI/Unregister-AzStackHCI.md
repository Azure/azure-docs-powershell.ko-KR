---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: e5ff59889b2b786d07699a5b9d46937372c0662f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176665"
---
# <span data-ttu-id="48653-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="48653-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="48653-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48653-102">SYNOPSIS</span></span>
<span data-ttu-id="48653-103">Unregister-AzStackHCI 프레미스 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 삭제하고 Azure를 사용하여 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48653-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="48653-104">매개 변수가 전달되지 않은 경우 클러스터에서 사용할 수 있는 등록된 정보를 사용하여 클러스터를 등록을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="48653-105">구문</span><span class="sxs-lookup"><span data-stu-id="48653-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>] [-UseDeviceAuthentication]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48653-106">설명</span><span class="sxs-lookup"><span data-stu-id="48653-106">DESCRIPTION</span></span>
<span data-ttu-id="48653-107">Unregister-AzStackHCI 프레미스 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 삭제하고 Azure를 사용하여 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48653-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="48653-108">매개 변수가 전달되지 않은 경우 클러스터에서 사용할 수 있는 등록된 정보를 사용하여 클러스터를 등록을 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="48653-109">예제</span><span class="sxs-lookup"><span data-stu-id="48653-109">EXAMPLES</span></span>

### <span data-ttu-id="48653-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="48653-110">EXAMPLE 1</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI
Result: Success
```
<span data-ttu-id="48653-111">클러스터 노드 중 하나에서 호출</span><span class="sxs-lookup"><span data-stu-id="48653-111">Invoking on one of the cluster node</span></span>

### <span data-ttu-id="48653-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="48653-112">EXAMPLE 2</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1
Result: Success
```
<span data-ttu-id="48653-113">관리 노드에서 호출</span><span class="sxs-lookup"><span data-stu-id="48653-113">Invoking from the management node</span></span>

### <span data-ttu-id="48653-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="48653-114">EXAMPLE 3</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False
Result: Success
```
<span data-ttu-id="48653-115">WAC에서 호출</span><span class="sxs-lookup"><span data-stu-id="48653-115">Invoking from WAC</span></span>

### <span data-ttu-id="48653-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="48653-116">EXAMPLE 4</span></span>
```powershell
C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
```
<span data-ttu-id="48653-117">모든 매개 변수를 사용하여 호출</span><span class="sxs-lookup"><span data-stu-id="48653-117">Invoking with all the parameters</span></span>

## <span data-ttu-id="48653-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48653-118">PARAMETERS</span></span>

### <span data-ttu-id="48653-119">-AccountId</span><span class="sxs-lookup"><span data-stu-id="48653-119">-AccountId</span></span>
<span data-ttu-id="48653-120">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-120">Specifies the ARM access token.</span></span>
<span data-ttu-id="48653-121">ArmAccessToken 및 GraphAccessToken과 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-121">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="48653-122">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="48653-122">-ArmAccessToken</span></span>
<span data-ttu-id="48653-123">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-123">Specifies the ARM access token.</span></span>
<span data-ttu-id="48653-124">GraphAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-124">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="48653-125">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="48653-125">-ComputerName</span></span>
<span data-ttu-id="48653-126">Azure에 등록되는 클러스터의 클러스터 노드 중 하나를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-126">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="48653-127">-Credential</span><span class="sxs-lookup"><span data-stu-id="48653-127">-Credential</span></span>
<span data-ttu-id="48653-128">ComputerName의 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-128">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="48653-129">기본값은 Cmdlet을 실행하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="48653-129">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="48653-130">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="48653-130">-EnvironmentName</span></span>
<span data-ttu-id="48653-131">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-131">Specifies the Azure Environment.</span></span>
<span data-ttu-id="48653-132">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="48653-132">Default is AzureCloud.</span></span>
<span data-ttu-id="48653-133">유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="48653-133">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="48653-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="48653-134">-GraphAccessToken</span></span>
<span data-ttu-id="48653-135">Graph 액세스 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="48653-136">ArmAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="48653-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48653-137">-ResourceGroupName</span></span>
<span data-ttu-id="48653-138">Azure 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-138">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="48653-139">지정하지 않으면 \<LocalClusterName\> -rg가 리소스 그룹 이름으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-139">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="48653-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="48653-140">-ResourceName</span></span>
<span data-ttu-id="48653-141">Azure에서 만든 리소스의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-141">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="48653-142">지정하지 않으면, 프레미스 클러스터 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-142">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="48653-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="48653-143">-SubscriptionId</span></span>
<span data-ttu-id="48653-144">리소스를 만들 Azure 구독을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-144">Specifies the Azure Subscription to create the resource</span></span>

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

### <span data-ttu-id="48653-145">-TenantId</span><span class="sxs-lookup"><span data-stu-id="48653-145">-TenantId</span></span>
<span data-ttu-id="48653-146">Azure TenantId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-146">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="48653-147">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="48653-147">-UseDeviceAuthentication</span></span>
<span data-ttu-id="48653-148">대화형 브라우저 프롬프트 대신 디바이스 코드 인증을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-148">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="48653-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48653-149">-Confirm</span></span>
<span data-ttu-id="48653-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48653-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48653-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48653-151">-WhatIf</span></span>
<span data-ttu-id="48653-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="48653-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48653-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48653-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48653-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48653-154">CommonParameters</span></span>
<span data-ttu-id="48653-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48653-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48653-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48653-157">입력</span><span class="sxs-lookup"><span data-stu-id="48653-157">INPUTS</span></span>

## <span data-ttu-id="48653-158">출력</span><span class="sxs-lookup"><span data-stu-id="48653-158">OUTPUTS</span></span>

### <span data-ttu-id="48653-159">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="48653-159">PSCustomObject.</span></span> <span data-ttu-id="48653-160">PSCustomObject에서 다음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48653-160">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="48653-161">결과: 성공 또는 실패 또는 취소.</span><span class="sxs-lookup"><span data-stu-id="48653-161">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="48653-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48653-162">NOTES</span></span>

## <span data-ttu-id="48653-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48653-163">RELATED LINKS</span></span>
