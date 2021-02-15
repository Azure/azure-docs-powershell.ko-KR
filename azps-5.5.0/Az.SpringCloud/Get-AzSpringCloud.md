---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloud.md
ms.openlocfilehash: 39324dc0f85ca4d6f9c3498fae92c340e2113dad
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189020"
---
# <span data-ttu-id="d68a7-101">Get-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="d68a7-101">Get-AzSpringCloud</span></span>

## <span data-ttu-id="d68a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d68a7-102">SYNOPSIS</span></span>
<span data-ttu-id="d68a7-103">서비스 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-103">Get a Service and its properties.</span></span>

## <span data-ttu-id="d68a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="d68a7-104">SYNTAX</span></span>

### <span data-ttu-id="d68a7-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="d68a7-105">List (Default)</span></span>
```
Get-AzSpringCloud [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d68a7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d68a7-106">Get</span></span>
```
Get-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d68a7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d68a7-107">GetViaIdentity</span></span>
```
Get-AzSpringCloud -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d68a7-108">List1</span><span class="sxs-lookup"><span data-stu-id="d68a7-108">List1</span></span>
```
Get-AzSpringCloud -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d68a7-109">설명</span><span class="sxs-lookup"><span data-stu-id="d68a7-109">DESCRIPTION</span></span>
<span data-ttu-id="d68a7-110">서비스 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-110">Get a Service and its properties.</span></span>

## <span data-ttu-id="d68a7-111">예제</span><span class="sxs-lookup"><span data-stu-id="d68a7-111">EXAMPLES</span></span>

### <span data-ttu-id="d68a7-112">예제 1: 이름으로 Spring Cloud Service를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-112">Example 1: Get Spring Cloud Service by name</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
ConfigServerPropertiesErrorCode                  :
ConfigServerPropertiesErrorMessage               :
ConfigServerPropertyState                        : Succeeded
GitPropertyHostKey                               :
GitPropertyHostKeyAlgorithm                      :
GitPropertyLabel                                 :
GitPropertyPassword                              :
GitPropertyPrivateKey                            :
GitPropertyRepository                            :
GitPropertySearchPath                            :
GitPropertyStrictHostKeyChecking                 :
GitPropertyUri                                   :
GitPropertyUsername                              :
Id                                               : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service
Location                                         : eastus
Name                                             : spring-cloud-service
NetworkProfileAppNetworkResourceGroup            :
NetworkProfileAppSubnetId                        :
NetworkProfileServiceCidr                        :
NetworkProfileServiceRuntimeNetworkResourceGroup :
NetworkProfileServiceRuntimeSubnetId             :
ProvisioningState                                : Succeeded
ServiceId                                        : e5e964885b4146b1a91e9bfc17971ee5
SkuCapacity                                      :
SkuName                                          : S0
SkuTier                                          : Standard
Tag                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TrackedResourceTags
TraceAppInsightInstrumentationKey                :
TraceEnabled                                     : False
TraceErrorCode                                   :
TraceErrorMessage                                :
TraceState                                       : Succeeded
Type                                             : Microsoft.AppPlatform/Spring
Version                                          : 2
ConfigServerGitProperty                          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerGitProperty
ConfigServerProperty                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerProperties
ConfigServerPropertyConfigServer                 : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ConfigServerSettings
ConfigServerPropertyError                        : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
NetworkProfile                                   : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.NetworkProfile
Property                                         : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ClusterResourceProperties
Sku                                              : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Sku
Trace                                            : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TraceProperties
TraceError                                       : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.Error
```

<span data-ttu-id="d68a7-113">이름으로 Spring Cloud Service를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-113">Get Spring Cloud Service by name</span></span>

### <span data-ttu-id="d68a7-114">예제 2: 리소스 그룹 아래에 모든 Spring 클라우드 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-114">Example 2: List all the spring cloud service under the resource group.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg
Location Name                Type
-------- ----                ----
eastus   spring-cloud-rg Microsoft.AppPlatform/Spring
```

<span data-ttu-id="d68a7-115">리소스 그룹 아래에 모든 Spring Cloud 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-115">List all the spring cloud service under the resource group.</span></span>

## <span data-ttu-id="d68a7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d68a7-116">PARAMETERS</span></span>

### <span data-ttu-id="d68a7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d68a7-117">-DefaultProfile</span></span>
<span data-ttu-id="d68a7-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d68a7-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d68a7-119">-InputObject</span></span>
<span data-ttu-id="d68a7-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d68a7-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d68a7-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d68a7-121">-Name</span></span>
<span data-ttu-id="d68a7-122">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-122">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d68a7-123">-ResourceGroupName</span></span>
<span data-ttu-id="d68a7-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d68a7-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a7-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d68a7-126">-SubscriptionId</span></span>
<span data-ttu-id="d68a7-127">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-127">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d68a7-128">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-128">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d68a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d68a7-129">CommonParameters</span></span>
<span data-ttu-id="d68a7-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d68a7-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d68a7-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d68a7-132">입력</span><span class="sxs-lookup"><span data-stu-id="d68a7-132">INPUTS</span></span>

### <span data-ttu-id="d68a7-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="d68a7-133">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="d68a7-134">출력</span><span class="sxs-lookup"><span data-stu-id="d68a7-134">OUTPUTS</span></span>

### <span data-ttu-id="d68a7-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="d68a7-135">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="d68a7-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d68a7-136">NOTES</span></span>

<span data-ttu-id="d68a7-137">별칭</span><span class="sxs-lookup"><span data-stu-id="d68a7-137">ALIASES</span></span>

<span data-ttu-id="d68a7-138">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d68a7-138">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d68a7-139">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-139">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d68a7-140">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d68a7-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d68a7-141">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d68a7-141">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d68a7-142">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-142">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="d68a7-143">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-143">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="d68a7-144">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-144">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="d68a7-145">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-145">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="d68a7-146">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-146">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="d68a7-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d68a7-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d68a7-148">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="d68a7-148">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="d68a7-149">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d68a7-150">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d68a7-151">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-151">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="d68a7-152">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-152">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="d68a7-153">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d68a7-153">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d68a7-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d68a7-154">RELATED LINKS</span></span>

