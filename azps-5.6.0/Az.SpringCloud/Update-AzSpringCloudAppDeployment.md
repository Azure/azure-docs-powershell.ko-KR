---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 466bf2908cf1da940a369d2276dbf39106d60515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005307"
---
# <span data-ttu-id="c035b-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="c035b-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="c035b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c035b-102">SYNOPSIS</span></span>
<span data-ttu-id="c035b-103">종료 배포를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c035b-104">구문</span><span class="sxs-lookup"><span data-stu-id="c035b-104">SYNTAX</span></span>

### <span data-ttu-id="c035b-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="c035b-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="c035b-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c035b-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c035b-107">설명</span><span class="sxs-lookup"><span data-stu-id="c035b-107">DESCRIPTION</span></span>
<span data-ttu-id="c035b-108">종료 배포를 업데이트하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="c035b-109">예제</span><span class="sxs-lookup"><span data-stu-id="c035b-109">EXAMPLES</span></span>

### <span data-ttu-id="c035b-110">예제 1: 이름에 의해 Spring Cloud Deployment를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
```powershell
PS C:\> Update-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c035b-111">이름에 의해 Spring Cloud 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="c035b-112">예제 2: 파이프에서 Spring Cloud 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
```powershell
PS C:\> Get-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rg -ServiceName spring-cloud-service -AppName gateway -DeploymentName default | Update-AzSpringCloudAppDeployment -SourceRelativePath resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
Active                               : True
AppName                              : gateway
CreatedTime                          :
DeploymentSettingCpu                 : 1
DeploymentSettingEnvironmentVariable : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettingsEnvironmentVariables
DeploymentSettingInstanceCount       : 1
DeploymentSettingJvmOption           :
DeploymentSettingMemoryInGb          : 1
DeploymentSettingRuntimeVersion      : Java_8
Id                                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/spring-cloud-rg/providers/Microsoft.AppPlatform/Spring/spring-cloud-service/apps/gateway/deployments/default
Instance                             : {gateway-default-7-fb79b6b5d-kvmpz}
Name                                 : default
ProvisioningState                    : Succeeded
SourceArtifactSelector               :
SourceRelativePath                   : resources/4ea5ee68fea05586106890ded5733820bb77d919cda27bc4b8139b7cd33b8889-2020080815-6986fdbd-59f6-42b8-8d1f-a75d403cbcde
SourceType                           : Jar
SourceVersion                        :
Status                               : Running
Type                                 : Microsoft.AppPlatform/Spring/apps/deployments
DeploymentSetting                    : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentSettings
Property                             : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.DeploymentResourceProperties
Source                               : Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.UserSourceInfo
```

<span data-ttu-id="c035b-113">파이프에서 Spring Cloud 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="c035b-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c035b-114">PARAMETERS</span></span>

### <span data-ttu-id="c035b-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="c035b-115">-AppName</span></span>
<span data-ttu-id="c035b-116">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="c035b-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c035b-117">-AsJob</span></span>
<span data-ttu-id="c035b-118">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-118">Run the command as a job</span></span>

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

### <span data-ttu-id="c035b-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="c035b-119">-Cpu</span></span>
<span data-ttu-id="c035b-120">필수 CPU</span><span class="sxs-lookup"><span data-stu-id="c035b-120">Required CPU</span></span>

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

### <span data-ttu-id="c035b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c035b-121">-DefaultProfile</span></span>
<span data-ttu-id="c035b-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c035b-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="c035b-123">-EnvironmentVariable</span></span>
<span data-ttu-id="c035b-124">환경 변수 컬렉션</span><span class="sxs-lookup"><span data-stu-id="c035b-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="c035b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c035b-125">-InputObject</span></span>
<span data-ttu-id="c035b-126">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="c035b-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c035b-127">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="c035b-127">-JvmOption</span></span>
<span data-ttu-id="c035b-128">JVM 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c035b-128">JVM parameter</span></span>

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

### <span data-ttu-id="c035b-129">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="c035b-129">-MemoryInGb</span></span>
<span data-ttu-id="c035b-130">필요한 메모리 크기(GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-130">Required Memory size in GB</span></span>

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

### <span data-ttu-id="c035b-131">-Name</span><span class="sxs-lookup"><span data-stu-id="c035b-131">-Name</span></span>
<span data-ttu-id="c035b-132">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-132">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c035b-133">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c035b-133">-NoWait</span></span>
<span data-ttu-id="c035b-134">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="c035b-134">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c035b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c035b-135">-ResourceGroupName</span></span>
<span data-ttu-id="c035b-136">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c035b-137">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c035b-138">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="c035b-138">-RuntimeVersion</span></span>
<span data-ttu-id="c035b-139">런타임 버전</span><span class="sxs-lookup"><span data-stu-id="c035b-139">Runtime version</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.RuntimeVersion
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c035b-140">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c035b-140">-ServiceName</span></span>
<span data-ttu-id="c035b-141">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-141">The name of the Service resource.</span></span>

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

### <span data-ttu-id="c035b-142">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="c035b-142">-SourceArtifactSelector</span></span>
<span data-ttu-id="c035b-143">다중 모듈 프로젝트에 대한 배포에 사용할 아티팩트의 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-143">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="c035b-144">대상 모듈/프로젝트에 대한 상대 경로를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-144">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="c035b-145">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="c035b-145">-SourceRelativePath</span></span>
<span data-ttu-id="c035b-146">원본을 저장하는 저장소의 상대 경로</span><span class="sxs-lookup"><span data-stu-id="c035b-146">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="c035b-147">-SourceType</span><span class="sxs-lookup"><span data-stu-id="c035b-147">-SourceType</span></span>
<span data-ttu-id="c035b-148">업로드된 원본 유형</span><span class="sxs-lookup"><span data-stu-id="c035b-148">Type of the source uploaded</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Support.UserSourceType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c035b-149">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="c035b-149">-SourceVersion</span></span>
<span data-ttu-id="c035b-150">원본 버전</span><span class="sxs-lookup"><span data-stu-id="c035b-150">Version of the source</span></span>

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

### <span data-ttu-id="c035b-151">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c035b-151">-SubscriptionId</span></span>
<span data-ttu-id="c035b-152">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-152">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c035b-153">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-153">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c035b-154">-확인</span><span class="sxs-lookup"><span data-stu-id="c035b-154">-Confirm</span></span>
<span data-ttu-id="c035b-155">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c035b-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c035b-156">-WhatIf</span></span>
<span data-ttu-id="c035b-157">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c035b-158">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c035b-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c035b-159">CommonParameters</span></span>
<span data-ttu-id="c035b-160">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c035b-161">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c035b-161">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c035b-162">입력</span><span class="sxs-lookup"><span data-stu-id="c035b-162">INPUTS</span></span>

### <span data-ttu-id="c035b-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span><span class="sxs-lookup"><span data-stu-id="c035b-163">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="c035b-164">출력</span><span class="sxs-lookup"><span data-stu-id="c035b-164">OUTPUTS</span></span>

### <span data-ttu-id="c035b-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="c035b-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="c035b-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c035b-166">NOTES</span></span>

<span data-ttu-id="c035b-167">별칭</span><span class="sxs-lookup"><span data-stu-id="c035b-167">ALIASES</span></span>

<span data-ttu-id="c035b-168">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c035b-168">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c035b-169">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-169">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c035b-170">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c035b-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c035b-171">INPUTOBJECT <ISpringCloudIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c035b-171">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c035b-172">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-172">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="c035b-173">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-173">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="c035b-174">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-174">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="c035b-175">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-175">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="c035b-176">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-176">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="c035b-177">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="c035b-177">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c035b-178">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="c035b-178">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="c035b-179">`[ResourceGroupName <String>]`: 리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-179">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="c035b-180">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-180">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="c035b-181">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-181">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="c035b-182">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-182">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c035b-183">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c035b-183">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c035b-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c035b-184">RELATED LINKS</span></span>

