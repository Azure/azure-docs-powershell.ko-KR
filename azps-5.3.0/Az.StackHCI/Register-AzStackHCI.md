---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: ad9c09118252499f99708ae99d36ee9ba2418ff2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491544"
---
# <span data-ttu-id="047b4-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="047b4-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="047b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="047b4-102">SYNOPSIS</span></span>
<span data-ttu-id="047b4-103">Register-AzStackHCI 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 만들고 Azure에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="047b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="047b4-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="047b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="047b4-105">DESCRIPTION</span></span>
<span data-ttu-id="047b4-106">Register-AzStackHCI 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 만들고 Azure에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="047b4-107">예제</span><span class="sxs-lookup"><span data-stu-id="047b4-107">EXAMPLES</span></span>

### <span data-ttu-id="047b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="047b4-108">EXAMPLE 1</span></span>
```
Invoking on one of the cluster node.
```

<span data-ttu-id="047b4-109">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="047b4-109">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/</span></span>

### <span data-ttu-id="047b4-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="047b4-110">EXAMPLE 2</span></span>
```
Invoking from the management node
```

<span data-ttu-id="047b4-111">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531- 56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="047b4-111">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1 Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="047b4-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="047b4-112">EXAMPLE 3</span></span>
```
Invoking from WAC
```

<span data-ttu-id="047b4-113">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer.. ere= -GraphAccessToken acyee.. rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="047b4-113">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG Result: PendingForAdminConsent ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

### <span data-ttu-id="047b4-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="047b4-114">EXAMPLE 4</span></span>
```
Invoking with all the parameters
```

<span data-ttu-id="047b4-115">C:\PS \> Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciClu -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer.. ere= -GraphAccessToken acee.. rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span><span class="sxs-lookup"><span data-stu-id="047b4-115">C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential Result: Success ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1 PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/</span></span>

## <span data-ttu-id="047b4-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="047b4-116">PARAMETERS</span></span>

### <span data-ttu-id="047b4-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="047b4-117">-AccountId</span></span>
<span data-ttu-id="047b4-118">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="047b4-119">ArmAccessToken 및 GraphAccessToken과 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="047b4-120">-ArmAccessToken</span></span>
<span data-ttu-id="047b4-121">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="047b4-122">GraphAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="047b4-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="047b4-123">-CertificateThumbprint</span></span>
<span data-ttu-id="047b4-124">모든 노드에서 사용할 수 있는 인증서의 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="047b4-125">사용자는 인증서를 관리할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-125">User is responsible for managing the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="047b4-126">-ComputerName</span></span>
<span data-ttu-id="047b4-127">Azure에 등록되는 클러스터 이름 또는 클러스터 노드 중 하나를 Azure에 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="047b4-128">-Credential</span></span>
<span data-ttu-id="047b4-129">ComputerName의 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="047b4-130">기본값은 Cmdlet을 실행하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-130">Default is the current user executing the Cmdlet.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 12
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="047b4-131">-EnvironmentName</span></span>
<span data-ttu-id="047b4-132">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="047b4-133">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-133">Default is AzureCloud.</span></span>
<span data-ttu-id="047b4-134">유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="047b4-135">-GraphAccessToken</span></span>
<span data-ttu-id="047b4-136">Graph 액세스 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="047b4-137">ArmAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="047b4-138">-Region</span><span class="sxs-lookup"><span data-stu-id="047b4-138">-Region</span></span>
<span data-ttu-id="047b4-139">리소스를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="047b4-140">기본값은 EastUS입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="047b4-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="047b4-141">-RepairRegistration</span></span>
<span data-ttu-id="047b4-142">클라우드로 현재 Azure Stack HCI 등록을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="047b4-143">이 cmdlet은 클러스터형 노드의 로컬 인증서와 클라우드의 Azure AD 애플리케이션에서 원격 인증서를 삭제하고 둘 다에 대한 새 대체 인증서를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="047b4-144">리소스 그룹, 리소스 이름 및 기타 등록 선택이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="047b4-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="047b4-145">-ResourceGroupName</span></span>
<span data-ttu-id="047b4-146">Azure 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="047b4-147">지정하지 않으면 \<LocalClusterName\> -rg가 리소스 그룹 이름으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="047b4-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="047b4-148">-ResourceName</span></span>
<span data-ttu-id="047b4-149">Azure에서 만든 리소스의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="047b4-150">지정하지 않으면, 프레미스 클러스터 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="047b4-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="047b4-151">-SubscriptionId</span></span>
<span data-ttu-id="047b4-152">리소스를 만들 Azure 구독을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="047b4-153">유일한 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-153">This is the only Mandatory parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="047b4-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="047b4-154">-TenantId</span></span>
<span data-ttu-id="047b4-155">Azure TenantId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="047b4-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="047b4-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="047b4-157">대화형 브라우저 프롬프트 대신 디바이스 코드 인증을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="047b4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047b4-158">CommonParameters</span></span>
<span data-ttu-id="047b4-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047b4-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="047b4-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047b4-161">입력</span><span class="sxs-lookup"><span data-stu-id="047b4-161">INPUTS</span></span>

## <span data-ttu-id="047b4-162">출력</span><span class="sxs-lookup"><span data-stu-id="047b4-162">OUTPUTS</span></span>

### <span data-ttu-id="047b4-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="047b4-163">PSCustomObject.</span></span> <span data-ttu-id="047b4-164">PSCustomObject에서 다음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="047b4-165">결과: 성공 또는 실패 또는 PendingForAdminConsent 또는 Cancelled입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="047b4-166">ResourceId: Azure에서 만든 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="047b4-167">PortalResourceURL: Azure Portal 리소스 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="047b4-168">PortalAADAppPermissionsURL: AAD 앱 사용 권한 페이지에 대한 Azure Portal URL입니다.</span><span class="sxs-lookup"><span data-stu-id="047b4-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="047b4-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="047b4-169">NOTES</span></span>

## <span data-ttu-id="047b4-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="047b4-170">RELATED LINKS</span></span>
