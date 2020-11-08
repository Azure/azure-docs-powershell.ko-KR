---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudApp.md
ms.openlocfilehash: 1e5af469f92c07f7223ba95715bd32b22b4eb66f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213945"
---
# <span data-ttu-id="405f9-101">Get-AzSpringCloudApp</span><span class="sxs-lookup"><span data-stu-id="405f9-101">Get-AzSpringCloudApp</span></span>

## <span data-ttu-id="405f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="405f9-102">SYNOPSIS</span></span>
<span data-ttu-id="405f9-103">앱 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-103">Get an App and its properties.</span></span>

## <span data-ttu-id="405f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="405f9-104">SYNTAX</span></span>

### <span data-ttu-id="405f9-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="405f9-105">List (Default)</span></span>
```
Get-AzSpringCloudApp -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="405f9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="405f9-106">Get</span></span>
```
Get-AzSpringCloudApp -Name <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-SyncStatus <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="405f9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="405f9-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudApp -InputObject <ISpringCloudIdentity> [-SyncStatus <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="405f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="405f9-108">DESCRIPTION</span></span>
<span data-ttu-id="405f9-109">앱 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-109">Get an App and its properties.</span></span>

## <span data-ttu-id="405f9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="405f9-110">EXAMPLES</span></span>

### <span data-ttu-id="405f9-111">예제 1: 이름으로 스프링 클라우드 앱 가져오기.</span><span class="sxs-lookup"><span data-stu-id="405f9-111">Example 1: Get Spring Cloud App by name.</span></span>
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

<span data-ttu-id="405f9-112">이름으로 스프링 클라우드 앱을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-112">Get Spring Cloud App by name.</span></span>

### <span data-ttu-id="405f9-113">예제 2: 지정 된 스프링 클라우드 서비스의 모든 앱을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-113">Example 2: List all the app under a given spring cloud service.</span></span>
```powershell
PS C:\> Get-AzSpringCloudApp -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service
Name            Type                              Location
----            ----                              --------
account-service Microsoft.AppPlatform/Spring/apps eastus
auth-service    Microsoft.AppPlatform/Spring/apps eastus
gateway         Microsoft.AppPlatform/Spring/apps eastus
```

<span data-ttu-id="405f9-114">지정 된 스프링 클라우드 서비스의 모든 앱을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-114">List all the app under a given spring cloud service.</span></span>

## <span data-ttu-id="405f9-115">변수</span><span class="sxs-lookup"><span data-stu-id="405f9-115">PARAMETERS</span></span>

### <span data-ttu-id="405f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="405f9-116">-DefaultProfile</span></span>
<span data-ttu-id="405f9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="405f9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="405f9-118">-InputObject</span></span>
<span data-ttu-id="405f9-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="405f9-120">-이름</span><span class="sxs-lookup"><span data-stu-id="405f9-120">-Name</span></span>
<span data-ttu-id="405f9-121">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-121">The name of the App resource.</span></span>

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

### <span data-ttu-id="405f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="405f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="405f9-123">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-123">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="405f9-124">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-124">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="405f9-125">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="405f9-125">-ServiceName</span></span>
<span data-ttu-id="405f9-126">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-126">The name of the Service resource.</span></span>

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

### <span data-ttu-id="405f9-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="405f9-127">-SubscriptionId</span></span>
<span data-ttu-id="405f9-128">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-128">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="405f9-129">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-129">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="405f9-130">-SyncStatus</span><span class="sxs-lookup"><span data-stu-id="405f9-130">-SyncStatus</span></span>
<span data-ttu-id="405f9-131">동기화 상태 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-131">Indicates whether sync status</span></span>

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

### <span data-ttu-id="405f9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="405f9-132">CommonParameters</span></span>
<span data-ttu-id="405f9-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="405f9-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="405f9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="405f9-135">입력</span><span class="sxs-lookup"><span data-stu-id="405f9-135">INPUTS</span></span>

### <span data-ttu-id="405f9-136">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="405f9-136">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="405f9-137">출력</span><span class="sxs-lookup"><span data-stu-id="405f9-137">OUTPUTS</span></span>

### <span data-ttu-id="405f9-138">SpringCloud. PowerShell. Api20190501Preview. Iap보도 Ource</span><span class="sxs-lookup"><span data-stu-id="405f9-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IAppResource</span></span>

## <span data-ttu-id="405f9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="405f9-139">NOTES</span></span>

<span data-ttu-id="405f9-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="405f9-140">ALIASES</span></span>

<span data-ttu-id="405f9-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="405f9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="405f9-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="405f9-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="405f9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="405f9-144">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="405f9-144">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="405f9-145">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-145">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="405f9-146">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-146">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="405f9-147">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-147">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="405f9-148">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-148">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="405f9-149">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-149">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="405f9-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="405f9-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="405f9-151">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="405f9-151">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="405f9-152">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-152">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="405f9-153">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-153">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="405f9-154">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-154">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="405f9-155">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-155">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="405f9-156">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="405f9-156">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="405f9-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="405f9-157">RELATED LINKS</span></span>

