---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloud.md
ms.openlocfilehash: 361ba47486d7cc506e918ea279129110306e415f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215221"
---
# <span data-ttu-id="b9f0a-101">Update-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="b9f0a-101">Update-AzSpringCloud</span></span>

## <span data-ttu-id="b9f0a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9f0a-102">SYNOPSIS</span></span>
<span data-ttu-id="b9f0a-103">종료 하는 서비스를 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-103">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="b9f0a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9f0a-104">SYNTAX</span></span>

### <span data-ttu-id="b9f0a-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9f0a-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b9f0a-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b9f0a-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloud -InputObject <ISpringCloudIdentity> [-GitPropertyUri <String>] [-Location <String>]
 [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>] [-TraceAppInsightInstrumentationKey <String>]
 [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b9f0a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b9f0a-107">DESCRIPTION</span></span>
<span data-ttu-id="b9f0a-108">종료 하는 서비스를 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-108">Operation to update an exiting Service.</span></span>

## <span data-ttu-id="b9f0a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b9f0a-109">EXAMPLES</span></span>

### <span data-ttu-id="b9f0a-110">예제 1: 이름으로 스프링 클라우드 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="b9f0a-110">Example 1: Update Spring Cloud Service by name.</span></span>
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

<span data-ttu-id="b9f0a-111">스프링 클라우드 서비스를 이름으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-111">Update Spring Cloud Service by name.</span></span>

### <span data-ttu-id="b9f0a-112">예제 2: 파이프에서 스프링 클라우드 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="b9f0a-112">Example 2: Update Spring Cloud Service from pipe.</span></span>
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

<span data-ttu-id="b9f0a-113">파이프에서 스프링 클라우드 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-113">Update Spring Cloud Service from pipe.</span></span>

## <span data-ttu-id="b9f0a-114">변수</span><span class="sxs-lookup"><span data-stu-id="b9f0a-114">PARAMETERS</span></span>

### <span data-ttu-id="b9f0a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b9f0a-115">-AsJob</span></span>
<span data-ttu-id="b9f0a-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b9f0a-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b9f0a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9f0a-117">-DefaultProfile</span></span>
<span data-ttu-id="b9f0a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9f0a-119">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="b9f0a-119">-GitPropertyUri</span></span>
<span data-ttu-id="b9f0a-120">리포지토리의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-120">URI of the repository</span></span>

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

### <span data-ttu-id="b9f0a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9f0a-121">-InputObject</span></span>
<span data-ttu-id="b9f0a-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9f0a-123">-위치</span><span class="sxs-lookup"><span data-stu-id="b9f0a-123">-Location</span></span>
<span data-ttu-id="b9f0a-124">리소스의 지리적 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-124">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="b9f0a-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b9f0a-125">-Name</span></span>
<span data-ttu-id="b9f0a-126">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b9f0a-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b9f0a-127">-NoWait</span></span>
<span data-ttu-id="b9f0a-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="b9f0a-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b9f0a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9f0a-129">-ResourceGroupName</span></span>
<span data-ttu-id="b9f0a-130">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b9f0a-131">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b9f0a-132">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="b9f0a-132">-SkuName</span></span>
<span data-ttu-id="b9f0a-133">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="b9f0a-133">Name of the Sku</span></span>

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

### <span data-ttu-id="b9f0a-134">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="b9f0a-134">-SkuTier</span></span>
<span data-ttu-id="b9f0a-135">Sku의 계층</span><span class="sxs-lookup"><span data-stu-id="b9f0a-135">Tier of the Sku</span></span>

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

### <span data-ttu-id="b9f0a-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9f0a-136">-SubscriptionId</span></span>
<span data-ttu-id="b9f0a-137">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-137">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9f0a-138">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9f0a-139">태그</span><span class="sxs-lookup"><span data-stu-id="b9f0a-139">-Tag</span></span>
<span data-ttu-id="b9f0a-140">서비스의 태그로, 리소스를 설명 하는 키 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-140">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="b9f0a-141">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="b9f0a-141">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="b9f0a-142">대상 응용 프로그램 통찰력 계측 키</span><span class="sxs-lookup"><span data-stu-id="b9f0a-142">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="b9f0a-143">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="b9f0a-143">-TraceEnabled</span></span>
<span data-ttu-id="b9f0a-144">추적 기능을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-144">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="b9f0a-145">-확인</span><span class="sxs-lookup"><span data-stu-id="b9f0a-145">-Confirm</span></span>
<span data-ttu-id="b9f0a-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9f0a-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9f0a-147">-WhatIf</span></span>
<span data-ttu-id="b9f0a-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9f0a-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9f0a-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9f0a-150">CommonParameters</span></span>
<span data-ttu-id="b9f0a-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9f0a-152">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9f0a-153">입력</span><span class="sxs-lookup"><span data-stu-id="b9f0a-153">INPUTS</span></span>

### <span data-ttu-id="b9f0a-154">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b9f0a-154">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b9f0a-155">출력</span><span class="sxs-lookup"><span data-stu-id="b9f0a-155">OUTPUTS</span></span>

### <span data-ttu-id="b9f0a-156">SpringCloud. PowerShell. Api20200701. IServiceResource</span><span class="sxs-lookup"><span data-stu-id="b9f0a-156">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="b9f0a-157">상속자</span><span class="sxs-lookup"><span data-stu-id="b9f0a-157">NOTES</span></span>

<span data-ttu-id="b9f0a-158">별칭과</span><span class="sxs-lookup"><span data-stu-id="b9f0a-158">ALIASES</span></span>

<span data-ttu-id="b9f0a-159">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b9f0a-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9f0a-160">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9f0a-161">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9f0a-162">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b9f0a-162">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9f0a-163">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-163">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b9f0a-164">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-164">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b9f0a-165">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-165">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b9f0a-166">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-166">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b9f0a-167">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-167">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b9f0a-168">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b9f0a-168">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9f0a-169">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="b9f0a-169">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b9f0a-170">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-170">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b9f0a-171">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-171">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b9f0a-172">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-172">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b9f0a-173">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-173">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b9f0a-174">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9f0a-174">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b9f0a-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9f0a-175">RELATED LINKS</span></span>

