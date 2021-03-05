---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: 2ea144ec36830286919f9cb512ccec01008428a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005323"
---
# <span data-ttu-id="e4c31-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="e4c31-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="e4c31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4c31-102">SYNOPSIS</span></span>
<span data-ttu-id="e4c31-103">종료 앱을 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="e4c31-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4c31-104">SYNTAX</span></span>

### <span data-ttu-id="e4c31-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e4c31-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e4c31-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e4c31-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e4c31-107">설명</span><span class="sxs-lookup"><span data-stu-id="e4c31-107">DESCRIPTION</span></span>
<span data-ttu-id="e4c31-108">종료 앱을 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="e4c31-109">예제</span><span class="sxs-lookup"><span data-stu-id="e4c31-109">EXAMPLES</span></span>

### <span data-ttu-id="e4c31-110">예제 1: Spring Cloud App을 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-110">Example 1: Update Spring Cloud App by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="e4c31-111">이름에 의해 Spring Cloud App을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="e4c31-112">예제 2: 파이프에서 Spring Cloud App 업데이트</span><span class="sxs-lookup"><span data-stu-id="e4c31-112">Example 2: Update Spring Cloud App from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway | Update-AzSpringCloudApp -ActiveDeploymentName default
ActiveDeploymentName    : default
CreatedTime             : 2020-08-08 15:37:43
Fqdn                    : spring-cloud-service.azuremicroservices.io
HttpsOnly               : False
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway
IdentityPrincipalId     :
IdentityTenantId        :
IdentityType            :
Location                : eastus
Name                    : gateway
PersistentDiskMountPath : /persistent
PersistentDiskSizeInGb  : 0
PersistentDiskUsedInGb  :
ProvisioningState       : Succeeded
Public                  : False
TemporaryDiskMountPath  : /tmp
TemporaryDiskSizeInGb   : 5
Type                    : Microsoft.AppPlatform/Spring/apps
Url                     :
Identity                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.ManagedIdentityProperties
PersistentDisk          : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.PersistentDisk
Property                : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.AppResourceProperties
TemporaryDisk           : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.TemporaryDisk
```

<span data-ttu-id="e4c31-113">파이프에서 Spring Cloud App을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="e4c31-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4c31-114">PARAMETERS</span></span>

### <span data-ttu-id="e4c31-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="e4c31-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="e4c31-116">앱의 활성 배포 이름</span><span class="sxs-lookup"><span data-stu-id="e4c31-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="e4c31-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4c31-117">-AsJob</span></span>
<span data-ttu-id="e4c31-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-118">Run the command as a job</span></span>

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

### <span data-ttu-id="e4c31-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4c31-119">-DefaultProfile</span></span>
<span data-ttu-id="e4c31-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4c31-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="e4c31-121">-Fqdn</span></span>
<span data-ttu-id="e4c31-122">전체 자격을 갖춘 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="e4c31-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="e4c31-123">-HttpsOnly</span></span>
<span data-ttu-id="e4c31-124">https만 허용되는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="e4c31-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4c31-125">-InputObject</span></span>
<span data-ttu-id="e4c31-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e4c31-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e4c31-127">-Location</span><span class="sxs-lookup"><span data-stu-id="e4c31-127">-Location</span></span>
<span data-ttu-id="e4c31-128">애플리케이션의 GEO 위치(항상 상위 리소스와 동일)</span><span class="sxs-lookup"><span data-stu-id="e4c31-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="e4c31-129">-Name</span><span class="sxs-lookup"><span data-stu-id="e4c31-129">-Name</span></span>
<span data-ttu-id="e4c31-130">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-130">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c31-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e4c31-131">-NoWait</span></span>
<span data-ttu-id="e4c31-132">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="e4c31-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e4c31-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="e4c31-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="e4c31-134">영구 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="e4c31-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="e4c31-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="e4c31-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="e4c31-136">GB의 영구 디스크 크기</span><span class="sxs-lookup"><span data-stu-id="e4c31-136">Size of the persistent disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c31-137">-Public</span><span class="sxs-lookup"><span data-stu-id="e4c31-137">-Public</span></span>
<span data-ttu-id="e4c31-138">앱이 공용 엔드포인트를 노출하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="e4c31-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4c31-139">-ResourceGroupName</span></span>
<span data-ttu-id="e4c31-140">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="e4c31-141">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="e4c31-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="e4c31-142">-ServiceName</span></span>
<span data-ttu-id="e4c31-143">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="e4c31-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e4c31-144">-SubscriptionId</span></span>
<span data-ttu-id="e4c31-145">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="e4c31-146">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e4c31-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="e4c31-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="e4c31-148">임시 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="e4c31-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="e4c31-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="e4c31-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="e4c31-150">GB의 임시 디스크 크기</span><span class="sxs-lookup"><span data-stu-id="e4c31-150">Size of the temporary disk in GB</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4c31-151">-확인</span><span class="sxs-lookup"><span data-stu-id="e4c31-151">-Confirm</span></span>
<span data-ttu-id="e4c31-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4c31-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4c31-153">-WhatIf</span></span>
<span data-ttu-id="e4c31-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4c31-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4c31-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4c31-156">CommonParameters</span></span>
<span data-ttu-id="e4c31-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4c31-158">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4c31-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4c31-159">입력</span><span class="sxs-lookup"><span data-stu-id="e4c31-159">INPUTS</span></span>

### <span data-ttu-id="e4c31-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="e4c31-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="e4c31-161">출력</span><span class="sxs-lookup"><span data-stu-id="e4c31-161">OUTPUTS</span></span>

### <span data-ttu-id="e4c31-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="e4c31-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="e4c31-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4c31-163">NOTES</span></span>

<span data-ttu-id="e4c31-164">별칭</span><span class="sxs-lookup"><span data-stu-id="e4c31-164">ALIASES</span></span>

<span data-ttu-id="e4c31-165">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e4c31-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e4c31-166">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e4c31-167">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e4c31-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e4c31-168">INPUTOBJECT <ISpringCloudIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4c31-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e4c31-169">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="e4c31-170">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="e4c31-171">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="e4c31-172">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="e4c31-173">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="e4c31-174">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e4c31-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e4c31-175">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="e4c31-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="e4c31-176">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="e4c31-177">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="e4c31-178">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="e4c31-179">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="e4c31-180">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4c31-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="e4c31-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4c31-181">RELATED LINKS</span></span>

