---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 9c9ec2f2a48d3bc94ef0e0ab72b5b2bf4edd9045
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005344"
---
# <span data-ttu-id="ce526-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="ce526-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="ce526-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce526-102">SYNOPSIS</span></span>
<span data-ttu-id="ce526-103">종료 서비스를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ce526-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce526-104">SYNTAX</span></span>

### <span data-ttu-id="ce526-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce526-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ce526-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="ce526-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ce526-107">설명</span><span class="sxs-lookup"><span data-stu-id="ce526-107">DESCRIPTION</span></span>
<span data-ttu-id="ce526-108">종료 서비스를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="ce526-109">예제</span><span class="sxs-lookup"><span data-stu-id="ce526-109">EXAMPLES</span></span>

### <span data-ttu-id="ce526-110">예제 1: Spring Cloud Service를 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-110">Example 1: Update Spring Cloud Service by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
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

<span data-ttu-id="ce526-111">이름에 의해 Spring Cloud Service를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="ce526-112">예제 2: 파이프에서 Spring Cloud Service 업데이트</span><span class="sxs-lookup"><span data-stu-id="ce526-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloud -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service | Update-AzSpringCloud
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

<span data-ttu-id="ce526-113">파이프에서 Spring Cloud Service를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="ce526-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce526-114">PARAMETERS</span></span>

### <span data-ttu-id="ce526-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce526-115">-AsJob</span></span>
<span data-ttu-id="ce526-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ce526-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce526-117">-DefaultProfile</span></span>
<span data-ttu-id="ce526-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce526-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="ce526-119">-GitPropertyUri</span></span>
<span data-ttu-id="ce526-120">리포지토리의 URI</span><span class="sxs-lookup"><span data-stu-id="ce526-120">URI of the repository</span></span>

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

### <span data-ttu-id="ce526-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce526-121">-InputObject</span></span>
<span data-ttu-id="ce526-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ce526-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce526-123">-Location</span><span class="sxs-lookup"><span data-stu-id="ce526-123">-Location</span></span>
<span data-ttu-id="ce526-124">리소스의 GEO 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="ce526-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ce526-125">-Name</span></span>
<span data-ttu-id="ce526-126">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce526-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ce526-127">-NoWait</span></span>
<span data-ttu-id="ce526-128">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="ce526-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ce526-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce526-129">-ResourceGroupName</span></span>
<span data-ttu-id="ce526-130">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ce526-131">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce526-132">-SkuName</span><span class="sxs-lookup"><span data-stu-id="ce526-132">-SkuName</span></span>
<span data-ttu-id="ce526-133">Sku의 이름</span><span class="sxs-lookup"><span data-stu-id="ce526-133">Name of the Sku</span></span>

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

### <span data-ttu-id="ce526-134">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="ce526-134">-SkuTier</span></span>
<span data-ttu-id="ce526-135">Sku의 계층</span><span class="sxs-lookup"><span data-stu-id="ce526-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="ce526-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ce526-136">-SubscriptionId</span></span>
<span data-ttu-id="ce526-137">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="ce526-138">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-138">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce526-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="ce526-139">-Tag</span></span>
<span data-ttu-id="ce526-140">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce526-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="ce526-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="ce526-142">대상 애플리케이션 인사이트 계측 키</span><span class="sxs-lookup"><span data-stu-id="ce526-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="ce526-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="ce526-143">-TraceEnabled</span></span>
<span data-ttu-id="ce526-144">추적 기능을 사용하도록 설정하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="ce526-145">-확인</span><span class="sxs-lookup"><span data-stu-id="ce526-145">-Confirm</span></span>
<span data-ttu-id="ce526-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce526-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce526-147">-WhatIf</span></span>
<span data-ttu-id="ce526-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce526-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce526-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce526-150">CommonParameters</span></span>
<span data-ttu-id="ce526-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce526-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce526-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce526-153">입력</span><span class="sxs-lookup"><span data-stu-id="ce526-153">INPUTS</span></span>

### <span data-ttu-id="ce526-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="ce526-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="ce526-155">출력</span><span class="sxs-lookup"><span data-stu-id="ce526-155">OUTPUTS</span></span>

### <span data-ttu-id="ce526-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="ce526-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="ce526-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce526-157">NOTES</span></span>

<span data-ttu-id="ce526-158">별칭</span><span class="sxs-lookup"><span data-stu-id="ce526-158">ALIASES</span></span>

<span data-ttu-id="ce526-159">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ce526-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ce526-160">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ce526-161">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ce526-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ce526-162">INPUTOBJECT <ISpringCloudIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce526-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ce526-163">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="ce526-164">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="ce526-165">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="ce526-166">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="ce526-167">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="ce526-168">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ce526-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ce526-169">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="ce526-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="ce526-170">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ce526-171">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ce526-172">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="ce526-173">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="ce526-174">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="ce526-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ce526-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce526-175">RELATED LINKS</span></span>

