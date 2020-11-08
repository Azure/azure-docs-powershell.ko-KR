---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/update-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudApp.md
ms.openlocfilehash: f8da3fe762abc3f281a8a06dd365cd0271eb0ac9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215224"
---
# <span data-ttu-id="540a0-101">Update-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="540a0-101">Update-AzSpringCloudApp</span></span>

## <span data-ttu-id="540a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="540a0-102">SYNOPSIS</span></span>
<span data-ttu-id="540a0-103">종료 된 앱을 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-103">Operation to update an exiting App.</span></span>

## <span data-ttu-id="540a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="540a0-104">SYNTAX</span></span>

### <span data-ttu-id="540a0-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="540a0-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String>] [-ActiveDeploymentName <String>] [-Fqdn <String>] [-HttpsOnly]
 [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>] [-Public]
 [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="540a0-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="540a0-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-ActiveDeploymentName <String>] [-Fqdn <String>]
 [-HttpsOnly] [-Location <String>] [-PersistentDiskMountPath <String>] [-PersistentDiskSizeInGb <Int32>]
 [-Public] [-TemporaryDiskMountPath <String>] [-TemporaryDiskSizeInGb <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="540a0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="540a0-107">DESCRIPTION</span></span>
<span data-ttu-id="540a0-108">종료 된 앱을 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-108">Operation to update an exiting App.</span></span>

## <span data-ttu-id="540a0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="540a0-109">EXAMPLES</span></span>

### <span data-ttu-id="540a0-110">예제 1: 이름으로 스프링 클라우드 앱 업데이트</span><span class="sxs-lookup"><span data-stu-id="540a0-110">Example 1: Update Spring Cloud App by name.</span></span>
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

<span data-ttu-id="540a0-111">스프링 클라우드 앱을 이름별로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-111">Update Spring Cloud App by name.</span></span>

### <span data-ttu-id="540a0-112">예제 2: 파이프에서 스프링 클라우드 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-112">Example 2: Update Spring Cloud App from pipe.</span></span>
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

<span data-ttu-id="540a0-113">파이프에서 스프링 클라우드 앱을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-113">Update Spring Cloud App from pipe.</span></span>

## <span data-ttu-id="540a0-114">변수</span><span class="sxs-lookup"><span data-stu-id="540a0-114">PARAMETERS</span></span>

### <span data-ttu-id="540a0-115">-ActiveDeploymentName</span><span class="sxs-lookup"><span data-stu-id="540a0-115">-ActiveDeploymentName</span></span>
<span data-ttu-id="540a0-116">앱의 활성 배포 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-116">Name of the active deployment of the App</span></span>

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

### <span data-ttu-id="540a0-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="540a0-117">-AsJob</span></span>
<span data-ttu-id="540a0-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="540a0-118">Run the command as a job</span></span>

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

### <span data-ttu-id="540a0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540a0-119">-DefaultProfile</span></span>
<span data-ttu-id="540a0-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="540a0-121">-Fqdn</span><span class="sxs-lookup"><span data-stu-id="540a0-121">-Fqdn</span></span>
<span data-ttu-id="540a0-122">정규화 된 dns 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-122">Fully qualified dns Name.</span></span>

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

### <span data-ttu-id="540a0-123">-HttpsOnly</span><span class="sxs-lookup"><span data-stu-id="540a0-123">-HttpsOnly</span></span>
<span data-ttu-id="540a0-124">Https만 허용 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-124">Indicate if only https is allowed.</span></span>

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

### <span data-ttu-id="540a0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="540a0-125">-InputObject</span></span>
<span data-ttu-id="540a0-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="540a0-127">-위치</span><span class="sxs-lookup"><span data-stu-id="540a0-127">-Location</span></span>
<span data-ttu-id="540a0-128">응용 프로그램의 지리적 위치 이며 항상 부모 리소스와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-128">The GEO location of the application, always the same with its parent resource</span></span>

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

### <span data-ttu-id="540a0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="540a0-129">-Name</span></span>
<span data-ttu-id="540a0-130">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-130">The name of the App resource.</span></span>

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

### <span data-ttu-id="540a0-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="540a0-131">-NoWait</span></span>
<span data-ttu-id="540a0-132">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="540a0-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="540a0-133">-PersistentDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="540a0-133">-PersistentDiskMountPath</span></span>
<span data-ttu-id="540a0-134">영구 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="540a0-134">Mount path of the persistent disk</span></span>

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

### <span data-ttu-id="540a0-135">-PersistentDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="540a0-135">-PersistentDiskSizeInGb</span></span>
<span data-ttu-id="540a0-136">영구 디스크의 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="540a0-136">Size of the persistent disk in GB</span></span>

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

### <span data-ttu-id="540a0-137">-공용</span><span class="sxs-lookup"><span data-stu-id="540a0-137">-Public</span></span>
<span data-ttu-id="540a0-138">앱이 공개 끝점을 노출 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-138">Indicates whether the App exposes public endpoint</span></span>

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

### <span data-ttu-id="540a0-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540a0-139">-ResourceGroupName</span></span>
<span data-ttu-id="540a0-140">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-140">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="540a0-141">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-141">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="540a0-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="540a0-142">-ServiceName</span></span>
<span data-ttu-id="540a0-143">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="540a0-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="540a0-144">-SubscriptionId</span></span>
<span data-ttu-id="540a0-145">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-145">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="540a0-146">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-146">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="540a0-147">-TemporaryDiskMountPath</span><span class="sxs-lookup"><span data-stu-id="540a0-147">-TemporaryDiskMountPath</span></span>
<span data-ttu-id="540a0-148">임시 디스크의 탑재 경로</span><span class="sxs-lookup"><span data-stu-id="540a0-148">Mount path of the temporary disk</span></span>

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

### <span data-ttu-id="540a0-149">-TemporaryDiskSizeInGb</span><span class="sxs-lookup"><span data-stu-id="540a0-149">-TemporaryDiskSizeInGb</span></span>
<span data-ttu-id="540a0-150">임시 디스크 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="540a0-150">Size of the temporary disk in GB</span></span>

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

### <span data-ttu-id="540a0-151">-확인</span><span class="sxs-lookup"><span data-stu-id="540a0-151">-Confirm</span></span>
<span data-ttu-id="540a0-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540a0-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540a0-153">-WhatIf</span></span>
<span data-ttu-id="540a0-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="540a0-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540a0-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540a0-156">CommonParameters</span></span>
<span data-ttu-id="540a0-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540a0-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="540a0-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540a0-159">입력</span><span class="sxs-lookup"><span data-stu-id="540a0-159">INPUTS</span></span>

### <span data-ttu-id="540a0-160">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="540a0-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="540a0-161">출력</span><span class="sxs-lookup"><span data-stu-id="540a0-161">OUTPUTS</span></span>

### <span data-ttu-id="540a0-162">SpringCloud. PowerShell. Api20200701. Iap보도 Ource</span><span class="sxs-lookup"><span data-stu-id="540a0-162">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="540a0-163">상속자</span><span class="sxs-lookup"><span data-stu-id="540a0-163">NOTES</span></span>

<span data-ttu-id="540a0-164">별칭과</span><span class="sxs-lookup"><span data-stu-id="540a0-164">ALIASES</span></span>

<span data-ttu-id="540a0-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="540a0-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="540a0-166">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="540a0-167">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="540a0-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="540a0-168">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="540a0-168">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="540a0-169">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-169">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="540a0-170">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-170">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="540a0-171">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-171">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="540a0-172">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-172">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="540a0-173">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-173">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="540a0-174">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="540a0-174">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="540a0-175">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="540a0-175">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="540a0-176">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-176">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="540a0-177">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-177">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="540a0-178">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-178">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="540a0-179">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-179">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="540a0-180">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="540a0-180">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="540a0-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="540a0-181">RELATED LINKS</span></span>

