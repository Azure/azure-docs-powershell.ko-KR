---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.springcloud/get-azspringcloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Get-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 3accf4b622f77edb0e3d0cea6fe67bbc1db9ff6c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363910"
---
# <span data-ttu-id="73bc2-101">Get-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="73bc2-101">Get-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="73bc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73bc2-102">SYNOPSIS</span></span>
<span data-ttu-id="73bc2-103">배포 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-103">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="73bc2-104">구문</span><span class="sxs-lookup"><span data-stu-id="73bc2-104">SYNTAX</span></span>

### <span data-ttu-id="73bc2-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="73bc2-105">List1 (Default)</span></span>
```
Get-AzSpringCloudAppDeployment -ResourceGroupName <String> -ServiceName <String> [-SubscriptionId <String[]>]
 [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73bc2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="73bc2-106">Get</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="73bc2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73bc2-107">GetViaIdentity</span></span>
```
Get-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="73bc2-108">목록</span><span class="sxs-lookup"><span data-stu-id="73bc2-108">List</span></span>
```
Get-AzSpringCloudAppDeployment -AppName <String> -ResourceGroupName <String> -ServiceName <String>
 [-SubscriptionId <String[]>] [-Version <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="73bc2-109">설명</span><span class="sxs-lookup"><span data-stu-id="73bc2-109">DESCRIPTION</span></span>
<span data-ttu-id="73bc2-110">배포 및 해당 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-110">Get a Deployment and its properties.</span></span>

## <span data-ttu-id="73bc2-111">예제</span><span class="sxs-lookup"><span data-stu-id="73bc2-111">EXAMPLES</span></span>

### <span data-ttu-id="73bc2-112">예제 1: 이름에 따라 Spring Cloud App Deploymeng를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-112">Example 1: Get Spring Cloud App Deploymeng by name.</span></span>
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

<span data-ttu-id="73bc2-113">이름으로 Spring Cloud App Deploymeng를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-113">Get Spring Cloud App Deploymeng by name.</span></span>

### <span data-ttu-id="73bc2-114">예제 2: 주어진 Spring 클라우드 앱 아래에 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-114">Example 2: List all the deployment under a given spring cloud app.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway
Name    Type
----    ----
default Microsoft.AppPlatform/Spring/apps/deployments
prod    Microsoft.AppPlatform/Spring/apps/deployments
```

<span data-ttu-id="73bc2-115">지정한 Spring Cloud 앱 아래에 모든 배포를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-115">List all the deployment under a given spring cloud app.</span></span>

## <span data-ttu-id="73bc2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73bc2-116">PARAMETERS</span></span>

### <span data-ttu-id="73bc2-117">-AppName</span><span class="sxs-lookup"><span data-stu-id="73bc2-117">-AppName</span></span>
<span data-ttu-id="73bc2-118">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-118">The name of the App resource.</span></span>

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

### <span data-ttu-id="73bc2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73bc2-119">-DefaultProfile</span></span>
<span data-ttu-id="73bc2-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73bc2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73bc2-121">-InputObject</span></span>
<span data-ttu-id="73bc2-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="73bc2-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73bc2-123">-Name</span><span class="sxs-lookup"><span data-stu-id="73bc2-123">-Name</span></span>
<span data-ttu-id="73bc2-124">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-124">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="73bc2-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73bc2-125">-ResourceGroupName</span></span>
<span data-ttu-id="73bc2-126">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="73bc2-127">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bc2-128">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="73bc2-128">-ServiceName</span></span>
<span data-ttu-id="73bc2-129">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-129">The name of the Service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bc2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73bc2-130">-SubscriptionId</span></span>
<span data-ttu-id="73bc2-131">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-131">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="73bc2-132">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="73bc2-133">-Version</span><span class="sxs-lookup"><span data-stu-id="73bc2-133">-Version</span></span>
<span data-ttu-id="73bc2-134">나열할 배포의 버전</span><span class="sxs-lookup"><span data-stu-id="73bc2-134">Version of the deployments to be listed</span></span>

```yaml
Type: System.String[]
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73bc2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73bc2-135">CommonParameters</span></span>
<span data-ttu-id="73bc2-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73bc2-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="73bc2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73bc2-138">입력</span><span class="sxs-lookup"><span data-stu-id="73bc2-138">INPUTS</span></span>

### <span data-ttu-id="73bc2-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="73bc2-139">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="73bc2-140">출력</span><span class="sxs-lookup"><span data-stu-id="73bc2-140">OUTPUTS</span></span>

### <span data-ttu-id="73bc2-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="73bc2-141">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="73bc2-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="73bc2-142">NOTES</span></span>

<span data-ttu-id="73bc2-143">별칭</span><span class="sxs-lookup"><span data-stu-id="73bc2-143">ALIASES</span></span>

<span data-ttu-id="73bc2-144">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="73bc2-144">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73bc2-145">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-145">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73bc2-146">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73bc2-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73bc2-147">INPUTOBJECT: <ISpringCloudIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="73bc2-147">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73bc2-148">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-148">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="73bc2-149">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-149">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="73bc2-150">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-150">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="73bc2-151">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-151">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="73bc2-152">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-152">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="73bc2-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="73bc2-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73bc2-154">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="73bc2-154">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="73bc2-155">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="73bc2-156">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="73bc2-157">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-157">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="73bc2-158">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-158">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="73bc2-159">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="73bc2-159">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="73bc2-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73bc2-160">RELATED LINKS</span></span>

