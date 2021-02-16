---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/register-azstackhci
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Register-AzStackHCI.md
ms.openlocfilehash: a96ca28b750628eef1b0395e5867bb7f7341fba0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183209"
---
# <span data-ttu-id="684b6-101">Register-AzStackHCI</span><span class="sxs-lookup"><span data-stu-id="684b6-101">Register-AzStackHCI</span></span>

## <span data-ttu-id="684b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684b6-102">SYNOPSIS</span></span>
<span data-ttu-id="684b6-103">Register-AzStackHCI 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 만들고 Azure에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-103">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="684b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="684b6-104">SYNTAX</span></span>

```
Register-AzStackHCI [-SubscriptionId] <String> [[-Region] <String>] [[-ResourceName] <String>]
 [[-TenantId] <String>] [[-ResourceGroupName] <String>] [[-ArmAccessToken] <String>]
 [[-GraphAccessToken] <String>] [[-AccountId] <String>] [[-EnvironmentName] <String>]
 [[-ComputerName] <String>] [[-CertificateThumbprint] <String>] [-RepairRegistration]
 [-UseDeviceAuthentication] [[-Credential] <PSCredential>] [<CommonParameters>]
```

## <span data-ttu-id="684b6-105">설명</span><span class="sxs-lookup"><span data-stu-id="684b6-105">DESCRIPTION</span></span>
<span data-ttu-id="684b6-106">Register-AzStackHCI 클러스터를 나타내는 Microsoft.AzureStackHCI 클라우드 리소스를 만들고 Azure에 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-106">Register-AzStackHCI creates a Microsoft.AzureStackHCI cloud resource representing the on-premise cluster and registers the on-premise cluster with Azure.</span></span>

## <span data-ttu-id="684b6-107">예제</span><span class="sxs-lookup"><span data-stu-id="684b6-107">EXAMPLES</span></span>

### <span data-ttu-id="684b6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="684b6-108">EXAMPLE 1</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" 
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster1-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77826/isMSAApp/
```

<span data-ttu-id="684b6-109">클러스터 노드 중 하나에서 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-109">Invoking on one of the cluster node.</span></span>

### <span data-ttu-id="684b6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="684b6-110">EXAMPLE 2</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ComputerName ClusterNode1
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCICluster2-rg/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster2/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/950be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="684b6-111">관리 노드에서 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-111">Invoking from the management node.</span></span>

### <span data-ttu-id="684b6-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="684b6-112">EXAMPLE 3</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -ArmAccessToken etyer..ere= -GraphAccessToken acyee..rerrer -AccountId user1@corp1.com -Region westus -ResourceName DemoHCICluster3 -ResourceGroupName DemoHCIRG 
Result: PendingForAdminConsent
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/DemoHCIRG/providers/Microsoft.AzureStackHCI/clusters/DemoHCICluster3/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/980be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="684b6-113">WAC에서 호출.</span><span class="sxs-lookup"><span data-stu-id="684b6-113">Invoking from WAC.</span></span>

### <span data-ttu-id="684b6-114">예제 4</span><span class="sxs-lookup"><span data-stu-id="684b6-114">EXAMPLE 4</span></span>
```powershell
C:\PS\>Register-AzStackHCI -SubscriptionId "12a0f531-56cb-4340-9501-257726d741fd" -Region westus -ResourceName HciCluster1 -TenantId "c31c0dbb-ce27-4c78-ad26-a5f717c14557" -ResourceGroupName HciClusterRG -ArmAccessToken eerrer..ere= -GraphAccessToken acee..rerrer -AccountId user1@corp1.com -EnvironmentName AzureCloud -ComputerName node1hci -Credential Get-Credential
Result: Success
ResourceId: /subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1
PortalResourceURL: https://portal.azure.com/#@c31c0dbb-ce27-4c78-ad26-a5f717c14557/resource/subscriptions/12a0f531-56cb-4340-9501-257726d741fd/resourceGroups/HciClusterRG/providers/Microsoft.AzureStackHCI/clusters/HciCluster1/overview
PortalAADAppPermissionsURL: https://portal.azure.com/#blade/Microsoft_AAD_RegisteredApps/ApplicationMenuBlade/CallAnAPI/appId/990be58d-578c-4cff-b4cd-43e9c3a77866/isMSAApp/
```

<span data-ttu-id="684b6-115">모든 매개 변수를 사용하여 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-115">Invoking with all the parameters.</span></span>

## <span data-ttu-id="684b6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="684b6-116">PARAMETERS</span></span>

### <span data-ttu-id="684b6-117">-AccountId</span><span class="sxs-lookup"><span data-stu-id="684b6-117">-AccountId</span></span>
<span data-ttu-id="684b6-118">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-118">Specifies the ARM access token.</span></span>
<span data-ttu-id="684b6-119">ArmAccessToken 및 GraphAccessToken과 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-119">Specifying this along with ArmAccessToken and GraphAccessToken will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="684b6-120">-ArmAccessToken</span><span class="sxs-lookup"><span data-stu-id="684b6-120">-ArmAccessToken</span></span>
<span data-ttu-id="684b6-121">액세스 토큰의 ARM 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-121">Specifies the ARM access token.</span></span>
<span data-ttu-id="684b6-122">GraphAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-122">Specifying this along with GraphAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="684b6-123">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="684b6-123">-CertificateThumbprint</span></span>
<span data-ttu-id="684b6-124">모든 노드에서 사용할 수 있는 인증서의 지문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-124">Specifies the thumbprint of the certificate available on all the nodes.</span></span> <span data-ttu-id="684b6-125">사용자는 인증서를 관리할 책임이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-125">User is responsible for managing the certificate.</span></span>

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

### <span data-ttu-id="684b6-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="684b6-126">-ComputerName</span></span>
<span data-ttu-id="684b6-127">Azure에 등록되는 클러스터 이름 또는 클러스터 노드 중 하나를 Azure에 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-127">Specifies the cluster name or one of the cluster node in on-premise cluster that is being registered to Azure.</span></span>

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

### <span data-ttu-id="684b6-128">-Credential</span><span class="sxs-lookup"><span data-stu-id="684b6-128">-Credential</span></span>
<span data-ttu-id="684b6-129">ComputerName의 자격 증명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-129">Specifies the credential for the ComputerName.</span></span>
<span data-ttu-id="684b6-130">기본값은 Cmdlet을 실행하는 현재 사용자입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-130">Default is the current user executing the Cmdlet.</span></span>

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

### <span data-ttu-id="684b6-131">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="684b6-131">-EnvironmentName</span></span>
<span data-ttu-id="684b6-132">Azure 환경을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-132">Specifies the Azure Environment.</span></span>
<span data-ttu-id="684b6-133">기본값은 AzureCloud입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-133">Default is AzureCloud.</span></span>
<span data-ttu-id="684b6-134">유효한 값은 AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-134">Valid values are AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE</span></span>

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

### <span data-ttu-id="684b6-135">-GraphAccessToken</span><span class="sxs-lookup"><span data-stu-id="684b6-135">-GraphAccessToken</span></span>
<span data-ttu-id="684b6-136">Graph 액세스 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-136">Specifies the Graph access token.</span></span>
<span data-ttu-id="684b6-137">ArmAccessToken 및 AccountId와 함께 이를 지정하면 Azure 대화형 로그온이 방지됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-137">Specifying this along with ArmAccessToken and AccountId will avoid Azure interactive logon.</span></span>

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

### <span data-ttu-id="684b6-138">-Region</span><span class="sxs-lookup"><span data-stu-id="684b6-138">-Region</span></span>
<span data-ttu-id="684b6-139">리소스를 만들 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-139">Specifies the Region to create the resource.</span></span>
<span data-ttu-id="684b6-140">기본값은 EastUS입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-140">Default is EastUS.</span></span>

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

### <span data-ttu-id="684b6-141">-RepairRegistration</span><span class="sxs-lookup"><span data-stu-id="684b6-141">-RepairRegistration</span></span>
<span data-ttu-id="684b6-142">클라우드를 사용하여 현재 Azure Stack HCI 등록을 복구합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-142">Repair the current Azure Stack HCI registration with the cloud.</span></span> <span data-ttu-id="684b6-143">이 cmdlet은 클러스터형 노드의 로컬 인증서와 클라우드의 Azure AD 애플리케이션에서 원격 인증서를 삭제하고 둘 다에 대한 새 대체 인증서를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-143">This cmdlet deletes the local certificates on the clustered nodes and the remote certificates in the Azure AD application in the cloud and generates new replacement certificates for both.</span></span> <span data-ttu-id="684b6-144">리소스 그룹, 리소스 이름 및 기타 등록 선택이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-144">The resource group, resource name, and other registration choices are preserved.</span></span>

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

### <span data-ttu-id="684b6-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684b6-145">-ResourceGroupName</span></span>
<span data-ttu-id="684b6-146">Azure 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-146">Specifies the Azure Resource Group name.</span></span>
<span data-ttu-id="684b6-147">지정하지 않으면 \<LocalClusterName\> -rg가 리소스 그룹 이름으로 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-147">If not specified \<LocalClusterName\>-rg will be used as resource group name.</span></span>

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

### <span data-ttu-id="684b6-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="684b6-148">-ResourceName</span></span>
<span data-ttu-id="684b6-149">Azure에서 만든 리소스의 리소스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-149">Specifies the resource name of the resource created in Azure.</span></span>
<span data-ttu-id="684b6-150">지정하지 않으면, 프레미스 클러스터 이름이 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-150">If not specified, on-premise cluster name is used.</span></span>

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

### <span data-ttu-id="684b6-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="684b6-151">-SubscriptionId</span></span>
<span data-ttu-id="684b6-152">리소스를 만들 Azure 구독을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-152">Specifies the Azure Subscription to create the resource.</span></span>
<span data-ttu-id="684b6-153">유일한 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-153">This is the only Mandatory parameter.</span></span>

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

### <span data-ttu-id="684b6-154">-TenantId</span><span class="sxs-lookup"><span data-stu-id="684b6-154">-TenantId</span></span>
<span data-ttu-id="684b6-155">Azure TenantId를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-155">Specifies the Azure TenantId.</span></span>

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

### <span data-ttu-id="684b6-156">-UseDeviceAuthentication</span><span class="sxs-lookup"><span data-stu-id="684b6-156">-UseDeviceAuthentication</span></span>
<span data-ttu-id="684b6-157">대화형 브라우저 프롬프트 대신 디바이스 코드 인증을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-157">Use device code authentication instead of an interactive browser prompt.</span></span>

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

### <span data-ttu-id="684b6-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684b6-158">CommonParameters</span></span>
<span data-ttu-id="684b6-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684b6-160">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="684b6-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684b6-161">입력</span><span class="sxs-lookup"><span data-stu-id="684b6-161">INPUTS</span></span>

## <span data-ttu-id="684b6-162">출력</span><span class="sxs-lookup"><span data-stu-id="684b6-162">OUTPUTS</span></span>

### <span data-ttu-id="684b6-163">PSCustomObject.</span><span class="sxs-lookup"><span data-stu-id="684b6-163">PSCustomObject.</span></span> <span data-ttu-id="684b6-164">PSCustomObject에서 다음 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-164">Returns following Properties in PSCustomObject</span></span>
### <span data-ttu-id="684b6-165">결과: 성공 또는 실패 또는 PendingForAdminConsent 또는 Cancelled입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-165">Result: Success or Failed or PendingForAdminConsent or Cancelled.</span></span>
### <span data-ttu-id="684b6-166">ResourceId: Azure에서 만든 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-166">ResourceId: Resource ID of the resource created in Azure.</span></span>
### <span data-ttu-id="684b6-167">PortalResourceURL: Azure Portal 리소스 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-167">PortalResourceURL: Azure Portal Resource URL.</span></span>
### <span data-ttu-id="684b6-168">PortalAADAppPermissionsURL: AAD 앱 사용 권한 페이지에 대한 Azure Portal URL입니다.</span><span class="sxs-lookup"><span data-stu-id="684b6-168">PortalAADAppPermissionsURL: Azure Portal URL for AAD App permissions page.</span></span>
## <span data-ttu-id="684b6-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="684b6-169">NOTES</span></span>

## <span data-ttu-id="684b6-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="684b6-170">RELATED LINKS</span></span>
