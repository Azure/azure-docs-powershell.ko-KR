---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 43001ca921344d334f91bfa7b594e733a3307d8d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198628"
---
# <span data-ttu-id="52b39-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="52b39-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="52b39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52b39-102">SYNOPSIS</span></span>
<span data-ttu-id="52b39-103">앱 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-103">Get an App and its properties.</span></span>

## <span data-ttu-id="52b39-104">구문</span><span class="sxs-lookup"><span data-stu-id="52b39-104">SYNTAX</span></span>

### <span data-ttu-id="52b39-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="52b39-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52b39-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="52b39-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="52b39-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="52b39-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="52b39-108">설명</span><span class="sxs-lookup"><span data-stu-id="52b39-108">DESCRIPTION</span></span>
<span data-ttu-id="52b39-109">앱 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-109">Get an App and its properties.</span></span>

## <span data-ttu-id="52b39-110">예제</span><span class="sxs-lookup"><span data-stu-id="52b39-110">EXAMPLES</span></span>

### <span data-ttu-id="52b39-111">예제 1: 이름으로 Spring Cloud App을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-111">Example 1: Get Spring Cloud App by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
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

<span data-ttu-id="52b39-112">이름으로 Spring Cloud App을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="52b39-113">예제 2: 주어진 Spring 클라우드 서비스에서 모든 앱을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="52b39-114">주어진 Spring 클라우드 서비스에서 모든 앱을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="52b39-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52b39-115">PARAMETERS</span></span>

### <span data-ttu-id="52b39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52b39-116">-DefaultProfile</span></span>
<span data-ttu-id="52b39-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52b39-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52b39-118">-InputObject</span></span>
<span data-ttu-id="52b39-119">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="52b39-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="52b39-120">-Name</span><span class="sxs-lookup"><span data-stu-id="52b39-120">-Name</span></span>
<span data-ttu-id="52b39-121">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-121">The name of the App resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AppName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b39-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52b39-122">-ResourceGroupName</span></span>
<span data-ttu-id="52b39-123">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="52b39-124">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b39-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="52b39-125">-ServiceName</span></span>
<span data-ttu-id="52b39-126">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-126">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b39-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52b39-127">-SubscriptionId</span></span>
<span data-ttu-id="52b39-128">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="52b39-129">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b39-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="52b39-130">-SyncStatus</span></span>
<span data-ttu-id="52b39-131">동기화 상태인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-131">Indicates whether sync status</span></span>

```yaml
Type: System.String
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52b39-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52b39-132">CommonParameters</span></span>
<span data-ttu-id="52b39-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52b39-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="52b39-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52b39-135">입력</span><span class="sxs-lookup"><span data-stu-id="52b39-135">INPUTS</span></span>

### <span data-ttu-id="52b39-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="52b39-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="52b39-137">출력</span><span class="sxs-lookup"><span data-stu-id="52b39-137">OUTPUTS</span></span>

### <span data-ttu-id="52b39-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span><span class="sxs-lookup"><span data-stu-id="52b39-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IAppResource</span></span>

## <span data-ttu-id="52b39-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="52b39-139">NOTES</span></span>

<span data-ttu-id="52b39-140">별칭</span><span class="sxs-lookup"><span data-stu-id="52b39-140">ALIASES</span></span>

<span data-ttu-id="52b39-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="52b39-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="52b39-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="52b39-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="52b39-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="52b39-144">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="52b39-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="52b39-145">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="52b39-146">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="52b39-147">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="52b39-148">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="52b39-149">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="52b39-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="52b39-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="52b39-151">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="52b39-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="52b39-152">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="52b39-153">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="52b39-154">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="52b39-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="52b39-156">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="52b39-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="52b39-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52b39-157">RELATED LINKS</span></span>

