---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: d33f649d71a8fb3f4a112ac77937f37d867a24c4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213942"
---
# <span data-ttu-id="b7b67-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="b7b67-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="b7b67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7b67-102">SYNOPSIS</span></span>
<span data-ttu-id="b7b67-103">배포 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="b7b67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7b67-104">SYNTAX</span></span>

### <span data-ttu-id="b7b67-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7b67-105">List (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7b67-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b7b67-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b7b67-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b7b67-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7b67-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b7b67-108">DESCRIPTION</span></span>
<span data-ttu-id="b7b67-109">배포 및 해당 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-109">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="b7b67-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b7b67-110">EXAMPLES</span></span>

### <span data-ttu-id="b7b67-111">예제 1: 스프링 클라우드 앱 Deploymeng name으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-111">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default
Active                               : False
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-6bd6f87954-nl2wl}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : <default>
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="b7b67-112">스프링 클라우드 앱 Deploymeng를 이름으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-112">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="b7b67-113">예제 2: 지정 된 스프링 클라우드 앱에 모든 배포 나열</span><span class="sxs-lookup"><span data-stu-id="b7b67-113">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="b7b67-114">지정 된 스프링 클라우드 앱 아래에 모든 배포를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-114">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="b7b67-115">변수</span><span class="sxs-lookup"><span data-stu-id="b7b67-115">PARAMETERS</span></span>

### <span data-ttu-id="b7b67-116">-AppName</span><span class="sxs-lookup"><span data-stu-id="b7b67-116">-AppName</span></span>
<span data-ttu-id="b7b67-117">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-117">The name of the App resource.</span></span>

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

### <span data-ttu-id="b7b67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7b67-118">-DefaultProfile</span></span>
<span data-ttu-id="b7b67-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7b67-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7b67-120">-InputObject</span></span>
<span data-ttu-id="b7b67-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7b67-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b7b67-122">-Name</span></span>
<span data-ttu-id="b7b67-123">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-123">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b67-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7b67-124">-ResourceGroupName</span></span>
<span data-ttu-id="b7b67-125">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b7b67-126">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b7b67-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="b7b67-127">-ServiceName</span></span>
<span data-ttu-id="b7b67-128">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-128">The name of the Service resource.</span></span>

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

### <span data-ttu-id="b7b67-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b7b67-129">-SubscriptionId</span></span>
<span data-ttu-id="b7b67-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-130">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7b67-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7b67-132">-버전</span><span class="sxs-lookup"><span data-stu-id="b7b67-132">-Version</span></span>
<span data-ttu-id="b7b67-133">나열할 배포의 버전</span><span class="sxs-lookup"><span data-stu-id="b7b67-133">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7b67-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7b67-134">CommonParameters</span></span>
<span data-ttu-id="b7b67-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7b67-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7b67-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7b67-137">입력</span><span class="sxs-lookup"><span data-stu-id="b7b67-137">INPUTS</span></span>

### <span data-ttu-id="b7b67-138">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b7b67-138">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="b7b67-139">출력</span><span class="sxs-lookup"><span data-stu-id="b7b67-139">OUTPUTS</span></span>

### <span data-ttu-id="b7b67-140">SpringCloud. PowerShell. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="b7b67-140">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="b7b67-141">상속자</span><span class="sxs-lookup"><span data-stu-id="b7b67-141">NOTES</span></span>

<span data-ttu-id="b7b67-142">별칭과</span><span class="sxs-lookup"><span data-stu-id="b7b67-142">ALIASES</span></span>

<span data-ttu-id="b7b67-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b7b67-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7b67-144">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7b67-145">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7b67-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7b67-146">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7b67-146">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7b67-147">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-147">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="b7b67-148">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-148">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="b7b67-149">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-149">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="b7b67-150">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-150">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="b7b67-151">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-151">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="b7b67-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b7b67-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7b67-153">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="b7b67-153">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="b7b67-154">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-154">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b7b67-155">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-155">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b7b67-156">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-156">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="b7b67-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-157">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b7b67-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7b67-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b7b67-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7b67-159">RELATED LINKS</span></span>

