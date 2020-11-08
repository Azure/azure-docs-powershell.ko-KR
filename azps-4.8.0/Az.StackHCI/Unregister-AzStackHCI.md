---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/unregister-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Unregister-AzStackHCI.md
ms.openlocfilehash: cc887fb8e41fd9464914144e7cbed5a332948228
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213190"
---
# <span data-ttu-id="0a44f-101">Unregister-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="0a44f-101">Unregister-AzStackHCI</span></span>

## <span data-ttu-id="0a44f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a44f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a44f-103">Unregister-AzStackHCI 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 삭제 하 고 Azure를 사용 하 여 온-프레미스 클러스터의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-103">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="0a44f-104">클러스터에서 사용 가능한 등록 된 정보는 매개 변수가 전달 되지 않은 경우 클러스터의 등록을 취소 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-104">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="0a44f-105">구문과</span><span class="sxs-lookup"><span data-stu-id="0a44f-105">SYNTAX</span></span>

```
Unregister-AzStackHCI [[-SubscriptionId] <String>] [[-ResourceName] <String>] [[-TenantId] <String>]
 [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>] [[-GraphAccessToken] <String>]
 [[-AccountId] <String>] [[-EnvironmentName] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a44f-106">설명은</span><span class="sxs-lookup"><span data-stu-id="0a44f-106">DESCRIPTION</span></span>
<span data-ttu-id="0a44f-107">Unregister-AzStackHCI 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 삭제 하 고 Azure를 사용 하 여 온-프레미스 클러스터의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-107">Unregister-AzStackHCI deletes the Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and unregisters the on-premise cluster with Azure.</span></span>
<span data-ttu-id="0a44f-108">클러스터에서 사용 가능한 등록 된 정보는 매개 변수가 전달 되지 않은 경우 클러스터의 등록을 취소 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-108">The registered information available on the cluster is used to unregister the cluster if no parameters are passed.</span></span>

## <span data-ttu-id="0a44f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a44f-109">EXAMPLES</span></span>

### <span data-ttu-id="0a44f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0a44f-110">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node
```

<span data-ttu-id="0a44f-111">C:\PS \> 등록 취소-AzStackHCI 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="0a44f-111">C:\PS\>Unregister-AzStackHCI Result: Success</span></span>

### <span data-ttu-id="0a44f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="0a44f-112">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="0a44f-113">C:\PS \> 등록 취소-AzStackHCI-ComputerName ClusterNode1 Result: 성공</span><span class="sxs-lookup"><span data-stu-id="0a44f-113">C:\PS\>Unregister-AzStackHCI -ComputerName ClusterNode1 Result: Success</span></span>

### <span data-ttu-id="0a44f-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="0a44f-114">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="0a44f-115">C:\PS \> 등록 취소-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -Context.resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG-확인: $False 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="0a44f-115">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG -Confirm:$False Result: Success</span></span>

### <span data-ttu-id="0a44f-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="0a44f-116">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="0a44f-117">C:\PS \> 등록 취소-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Context.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer. ere =-GraphAccessToken acee. rerrer-AccountId user1@corp1.com -환경 이름 AzureCloud-ComputerName node1hci-자격 증명 Get-Credential 결과: 성공</span><span class="sxs-lookup"><span data-stu-id="0a44f-117">C:\PS\>Unregister-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success</span></span>

## <span data-ttu-id="0a44f-118">변수</span><span class="sxs-lookup"><span data-stu-id="0a44f-118">PARAMETERS</span></span>

### <span data-ttu-id="0a44f-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a44f-119">-SubscriptionId</span></span>
<span data-ttu-id="0a44f-120">리소스를 만들기 위한 Azure 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-120">Specifies the Azure Subscription to create the resource</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-121">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="0a44f-121">-ResourceName</span></span>
<span data-ttu-id="0a44f-122">Azure에서 만든 자원의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-122">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="0a44f-123">지정 하지 않은 경우 온-프레미스 클러스터 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-123">If not specified, on-premise cluster name is used.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-124">-TenantId</span><span class="sxs-lookup"><span data-stu-id="0a44f-124">-TenantId</span></span>
<span data-ttu-id="0a44f-125">Azure TenantId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-125">Specifies the Azure TenantId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a44f-126">-ResourceGroupName</span></span>
<span data-ttu-id="0a44f-127">Azure 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-127">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="0a44f-128">지정 하지 않으면 \<LocalClusterName\> rg가 리소스 그룹 이름으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-128">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-129">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="0a44f-129">-ArmAccessToken</span></span>
<span data-ttu-id="0a44f-130">ARM 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-130">Specifies the ARM access token.</span></span>
<span data-ttu-id="0a44f-131">GraphAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-131">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-132">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="0a44f-132">-GraphAccessToken</span></span>
<span data-ttu-id="0a44f-133">그래프 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-133">Specifies the Graph access token.</span></span>
<span data-ttu-id="0a44f-134">ArmAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-134">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-135">-AccountId</span><span class="sxs-lookup"><span data-stu-id="0a44f-135">-AccountId</span></span>
<span data-ttu-id="0a44f-136">ARM 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-136">Specifies the ARM access token.</span></span>
<span data-ttu-id="0a44f-137">ArmAccessToken 및 GraphAccessToken와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-137">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-138">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="0a44f-138">-EnvironmentName</span></span>
<span data-ttu-id="0a44f-139">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-139">Specifies the Azure Environment.</span></span>
<span data-ttu-id="0a44f-140">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-140">Default is AzureCloud.</span></span>
<span data-ttu-id="0a44f-141">유효한 값은 AzureCloud, AzureChinaCloud, Azureus정부, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-141">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-142">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="0a44f-142">-ComputerName</span></span>
<span data-ttu-id="0a44f-143">Azure에 등록 되는 온-프레미스 클러스터의 클러스터 노드 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-143">Specifies one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-144">-Credential</span><span class="sxs-lookup"><span data-stu-id="0a44f-144">-Credential</span></span>
<span data-ttu-id="0a44f-145">ComputerName에 대 한 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-145">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="0a44f-146">기본값은 Cmdlet을 실행 하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-146">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a44f-147">-WhatIf</span></span>
<span data-ttu-id="0a44f-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a44f-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-150">-확인</span><span class="sxs-lookup"><span data-stu-id="0a44f-150">-Confirm</span></span>
<span data-ttu-id="0a44f-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a44f-152">CommonParameters</span></span>
<span data-ttu-id="0a44f-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a44f-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0a44f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a44f-155">입력</span><span class="sxs-lookup"><span data-stu-id="0a44f-155">INPUTS</span></span>

## <span data-ttu-id="0a44f-156">출력</span><span class="sxs-lookup"><span data-stu-id="0a44f-156">OUTPUTS</span></span>

### <span data-ttu-id="0a44f-157">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="0a44f-157">PSCustomObject.</span></span> <span data-ttu-id="0a44f-158">PSCustomObject의 다음 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44f-158">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="0a44f-159">결과: 성공 또는 실패 또는 취소 됨.</span><span class="sxs-lookup"><span data-stu-id="0a44f-159">Result: Success or Failed or Cancelled.</span></span>
## <span data-ttu-id="0a44f-160">상속자</span><span class="sxs-lookup"><span data-stu-id="0a44f-160">NOTES</span></span>

## <span data-ttu-id="0a44f-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a44f-161">RELATED LINKS</span></span>
