---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: c09c4b4c8d71d90bbbac0771c75ea3ea51ee05dc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213191"
---
# <span data-ttu-id="531a6-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="531a6-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="531a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="531a6-102">SYNOPSIS</span></span>
<span data-ttu-id="531a6-103">Register-AzStackHCI는 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 만들고 Azure를 사용 하 여 온-프레미스 클러스터를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="531a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="531a6-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="531a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="531a6-105">DESCRIPTION</span></span>
<span data-ttu-id="531a6-106">Register-AzStackHCI는 온-프레미스 클러스터를 나타내는 Microsoft AzureStackHCI cloud 리소스를 만들고 Azure를 사용 하 여 온-프레미스 클러스터를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="531a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="531a6-107">EXAMPLES</span></span>

### <span data-ttu-id="531a6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="531a6-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="531a6-109">C:\PS \> 레지스터-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="531a6-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="531a6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="531a6-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="531a6-111">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ComputerName ClusterNode1 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="531a6-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="531a6-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="531a6-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="531a6-113">C:\PS \> Register-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-ArmAccessToken etyer. ere =-GraphAccessToken acyee.. rerrer-AccountId user1@corp1.com -지역 westus-Context.resourcename DemoHCICluster3-ResourceGroupName DemoHCIRG Result: Pendingforadminforresourceid:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="531a6-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="531a6-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="531a6-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="531a6-115">C:\PS \> 레지스터-AzStackHCI-SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd"-Region westus-Context.resourcename HciCluster1-TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557"-ResourceGroupName HciClusterRG-ArmAccessToken eerrer. ere =-GraphAccessToken acee. rerrer-AccountId user1@corp1.com -환경 이름 AzureCloud-ComputerName node1hci-자격 증명 Get-Credential 결과: 성공 ResourceId:/Subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="531a6-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="531a6-116">변수</span><span class="sxs-lookup"><span data-stu-id="531a6-116">PARAMETERS</span></span>

### <span data-ttu-id="531a6-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="531a6-117">-SubscriptionId</span></span>
<span data-ttu-id="531a6-118">리소스를 만들기 위한 Azure 구독을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-118">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="531a6-119">이것은 유일한 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-119">This is the only Mandatory parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531a6-120">-지역</span><span class="sxs-lookup"><span data-stu-id="531a6-120">-Region</span></span>
<span data-ttu-id="531a6-121">리소스를 만들 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-121">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="531a6-122">기본값은 미국입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-122">Default is EastUS.</span></span>

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

### <span data-ttu-id="531a6-123">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="531a6-123">-ResourceName</span></span>
<span data-ttu-id="531a6-124">Azure에서 만든 자원의 리소스 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-124">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="531a6-125">지정 하지 않은 경우 온-프레미스 클러스터 이름을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-125">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="531a6-126">-TenantId</span><span class="sxs-lookup"><span data-stu-id="531a6-126">-TenantId</span></span>
<span data-ttu-id="531a6-127">Azure TenantId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-127">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="531a6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="531a6-128">-ResourceGroupName</span></span>
<span data-ttu-id="531a6-129">Azure 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-129">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="531a6-130">지정 하지 않으면 \<LocalClusterName\> rg가 리소스 그룹 이름으로 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-130">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="531a6-131">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="531a6-131">-ArmAccessToken</span></span>
<span data-ttu-id="531a6-132">ARM 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-132">Specifies the ARM access token.</span></span>
<span data-ttu-id="531a6-133">GraphAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-133">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="531a6-134">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="531a6-134">-GraphAccessToken</span></span>
<span data-ttu-id="531a6-135">그래프 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-135">Specifies the Graph access token.</span></span>
<span data-ttu-id="531a6-136">ArmAccessToken 및 AccountId와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-136">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="531a6-137">-AccountId</span><span class="sxs-lookup"><span data-stu-id="531a6-137">-AccountId</span></span>
<span data-ttu-id="531a6-138">ARM 액세스 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-138">Specifies the ARM access token.</span></span>
<span data-ttu-id="531a6-139">ArmAccessToken 및 GraphAccessToken와 함께이를 지정 하면 Azure 대화형 로그온이 방지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-139">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531a6-140">-환경 이름</span><span class="sxs-lookup"><span data-stu-id="531a6-140">-EnvironmentName</span></span>
<span data-ttu-id="531a6-141">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-141">Specifies the Azure Environment.</span></span>
<span data-ttu-id="531a6-142">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-142">Default is AzureCloud.</span></span>
<span data-ttu-id="531a6-143">유효한 값은 AzureCloud, AzureChinaCloud, Azureus정부, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-143">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531a6-144">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="531a6-144">-ComputerName</span></span>
<span data-ttu-id="531a6-145">클러스터 이름 또는 Azure에 등록 되는 온-프레미스 클러스터의 클러스터 노드 중 하나를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-145">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531a6-146">-Credential</span><span class="sxs-lookup"><span data-stu-id="531a6-146">-Credential</span></span>
<span data-ttu-id="531a6-147">ComputerName에 대 한 자격 증명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-147">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="531a6-148">기본값은 Cmdlet을 실행 하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-148">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="531a6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="531a6-149">CommonParameters</span></span>
<span data-ttu-id="531a6-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="531a6-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="531a6-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="531a6-152">입력</span><span class="sxs-lookup"><span data-stu-id="531a6-152">INPUTS</span></span>

## <span data-ttu-id="531a6-153">출력</span><span class="sxs-lookup"><span data-stu-id="531a6-153">OUTPUTS</span></span>

### <span data-ttu-id="531a6-154">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="531a6-154">PSCustomObject.</span></span> <span data-ttu-id="531a6-155">PSCustomObject의 다음 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-155">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="531a6-156">결과: 성공 또는 실패 또는 PendingForAdminConsent 또는 취소 됨.</span><span class="sxs-lookup"><span data-stu-id="531a6-156">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="531a6-157">ResourceId: Azure에서 만든 자원의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-157">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="531a6-158">PortalResourceURL: Azure 포털 리소스 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-158">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="531a6-159">PortalAADAppPermissionsURL: AAD 앱 사용 권한 페이지의 Azure 포털 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="531a6-159">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="531a6-160">상속자</span><span class="sxs-lookup"><span data-stu-id="531a6-160">NOTES</span></span>

## <span data-ttu-id="531a6-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="531a6-161">RELATED LINKS</span></span>
