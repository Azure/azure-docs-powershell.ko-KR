---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/new-azspringcloud
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloud.md
ms.openlocfilehash: d5b8d521c72b553143f75b0911cb9b933b0795e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328509"
---
# <span data-ttu-id="d01f2-101">New-AzSpringCloud</span><span class="sxs-lookup"><span data-stu-id="d01f2-101">New-AzSpringCloud</span></span>

## <span data-ttu-id="d01f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d01f2-102">SYNOPSIS</span></span>
<span data-ttu-id="d01f2-103">새 서비스를 만들거나 종료 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-103">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="d01f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="d01f2-104">SYNTAX</span></span>

```
New-AzSpringCloud -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-GitPropertyUri <String>] [-Location <String>] [-SkuName <String>] [-SkuTier <String>] [-Tag <Hashtable>]
 [-TraceAppInsightInstrumentationKey <String>] [-TraceEnabled] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d01f2-105">설명</span><span class="sxs-lookup"><span data-stu-id="d01f2-105">DESCRIPTION</span></span>
<span data-ttu-id="d01f2-106">새 서비스를 만들거나 종료 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-106">Create a new Service or update an exiting Service.</span></span>

## <span data-ttu-id="d01f2-107">예제</span><span class="sxs-lookup"><span data-stu-id="d01f2-107">EXAMPLES</span></span>

### <span data-ttu-id="d01f2-108">예제 1: Spring 클라우드 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="d01f2-108">Example 1: Create a spring cloud service.</span></span>
```powershell
PS C:\> New-AzSpringCloud -ResourceGroupName spring-cloud-rp -name spring-cloud-service -Location eastus

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

<span data-ttu-id="d01f2-109">Spring Cloud 서비스를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-109">Create a spring cloud service.</span></span>

## <span data-ttu-id="d01f2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d01f2-110">PARAMETERS</span></span>

### <span data-ttu-id="d01f2-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d01f2-111">-AsJob</span></span>
<span data-ttu-id="d01f2-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d01f2-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d01f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d01f2-113">-DefaultProfile</span></span>
<span data-ttu-id="d01f2-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d01f2-115">-GitPropertyUri</span><span class="sxs-lookup"><span data-stu-id="d01f2-115">-GitPropertyUri</span></span>
<span data-ttu-id="d01f2-116">리포지토리의 URI</span><span class="sxs-lookup"><span data-stu-id="d01f2-116">URI of the repository</span></span>

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

### <span data-ttu-id="d01f2-117">-Location</span><span class="sxs-lookup"><span data-stu-id="d01f2-117">-Location</span></span>
<span data-ttu-id="d01f2-118">리소스의 GEO 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-118">The GEO location of the resource.</span></span>

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

### <span data-ttu-id="d01f2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d01f2-119">-Name</span></span>
<span data-ttu-id="d01f2-120">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-120">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d01f2-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d01f2-121">-NoWait</span></span>
<span data-ttu-id="d01f2-122">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="d01f2-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d01f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d01f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="d01f2-124">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d01f2-125">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d01f2-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="d01f2-126">-SkuName</span></span>
<span data-ttu-id="d01f2-127">SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="d01f2-127">Name of the Sku</span></span>

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

### <span data-ttu-id="d01f2-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="d01f2-128">-SkuTier</span></span>
<span data-ttu-id="d01f2-129">SKU의 계층</span><span class="sxs-lookup"><span data-stu-id="d01f2-129">Tier of the Sku</span></span>

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

### <span data-ttu-id="d01f2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d01f2-130">-SubscriptionId</span></span>
<span data-ttu-id="d01f2-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d01f2-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d01f2-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="d01f2-133">-Tag</span></span>
<span data-ttu-id="d01f2-134">리소스를 설명하는 키 값 쌍의 목록인 서비스의 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-134">Tags of the service which is a list of key value pairs that describe the resource.</span></span>

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

### <span data-ttu-id="d01f2-135">-TraceAppInsightInstrumentationKey</span><span class="sxs-lookup"><span data-stu-id="d01f2-135">-TraceAppInsightInstrumentationKey</span></span>
<span data-ttu-id="d01f2-136">대상 Application Insight 계측 키</span><span class="sxs-lookup"><span data-stu-id="d01f2-136">Target application insight instrumentation key</span></span>

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

### <span data-ttu-id="d01f2-137">-TraceEnabled</span><span class="sxs-lookup"><span data-stu-id="d01f2-137">-TraceEnabled</span></span>
<span data-ttu-id="d01f2-138">추적 기능을 사용하도록 설정하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-138">Indicates whether enable the tracing functionality</span></span>

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

### <span data-ttu-id="d01f2-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d01f2-139">-Confirm</span></span>
<span data-ttu-id="d01f2-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d01f2-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d01f2-141">-WhatIf</span></span>
<span data-ttu-id="d01f2-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d01f2-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d01f2-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d01f2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d01f2-144">CommonParameters</span></span>
<span data-ttu-id="d01f2-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d01f2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d01f2-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d01f2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d01f2-147">입력</span><span class="sxs-lookup"><span data-stu-id="d01f2-147">INPUTS</span></span>

## <span data-ttu-id="d01f2-148">출력</span><span class="sxs-lookup"><span data-stu-id="d01f2-148">OUTPUTS</span></span>

### <span data-ttu-id="d01f2-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span><span class="sxs-lookup"><span data-stu-id="d01f2-149">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IServiceResource</span></span>

## <span data-ttu-id="d01f2-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d01f2-150">NOTES</span></span>

<span data-ttu-id="d01f2-151">별칭</span><span class="sxs-lookup"><span data-stu-id="d01f2-151">ALIASES</span></span>

## <span data-ttu-id="d01f2-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d01f2-152">RELATED LINKS</span></span>

