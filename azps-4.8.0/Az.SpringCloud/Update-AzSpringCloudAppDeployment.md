---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/update-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/Update-AzSpringCloudAppDeployment.md
ms.openlocfilehash: f19383959e2a342555c7a741524e687b7bac37a8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213286"
---
# <span data-ttu-id="af191-101">Update-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="af191-101">Update-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="af191-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af191-102">SYNOPSIS</span></span>
<span data-ttu-id="af191-103">종료 된 배포를 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-103">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="af191-104">구문과</span><span class="sxs-lookup"><span data-stu-id="af191-104">SYNTAX</span></span>

### <span data-ttu-id="af191-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="af191-105">UpdateExpanded (Default)</span></span>
```
Update-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="af191-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="af191-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzSpringCloudAppDeployment -InputObject <ISpringCloudIdentity> [-Cpu <Int32>]
 [-EnvironmentVariable <Hashtable>] [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>]
 [-RuntimeVersion <RuntimeVersion>] [-SourceArtifactSelector <String>] [-SourceRelativePath <String>]
 [-SourceType <UserSourceType>] [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="af191-107">설명은</span><span class="sxs-lookup"><span data-stu-id="af191-107">DESCRIPTION</span></span>
<span data-ttu-id="af191-108">종료 된 배포를 업데이트 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-108">Operation to update an exiting Deployment.</span></span>

## <span data-ttu-id="af191-109">예제의</span><span class="sxs-lookup"><span data-stu-id="af191-109">EXAMPLES</span></span>

### <span data-ttu-id="af191-110">예제 1: 이름으로 스프링 클라우드 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="af191-110">Example 1: Update Spring Cloud Deployment by name.</span></span>
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

<span data-ttu-id="af191-111">이름에 따라 스프링 클라우드 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-111">Update Spring Cloud Deployment by name.</span></span>

### <span data-ttu-id="af191-112">예제 2: 파이프에서 스프링 클라우드 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="af191-112">Example 2: Update Spring Cloud Deployment from pipe.</span></span>
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

<span data-ttu-id="af191-113">파이프에서 스프링 클라우드 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-113">Update Spring Cloud Deployment from pipe.</span></span>

## <span data-ttu-id="af191-114">변수</span><span class="sxs-lookup"><span data-stu-id="af191-114">PARAMETERS</span></span>

### <span data-ttu-id="af191-115">-AppName</span><span class="sxs-lookup"><span data-stu-id="af191-115">-AppName</span></span>
<span data-ttu-id="af191-116">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-116">The name of the App resource.</span></span>

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

### <span data-ttu-id="af191-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af191-117">-AsJob</span></span>
<span data-ttu-id="af191-118">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="af191-118">Run the command as a job</span></span>

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

### <span data-ttu-id="af191-119">-Cpu</span><span class="sxs-lookup"><span data-stu-id="af191-119">-Cpu</span></span>
<span data-ttu-id="af191-120">필수 CPU</span><span class="sxs-lookup"><span data-stu-id="af191-120">Required CPU</span></span>

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

### <span data-ttu-id="af191-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af191-121">-DefaultProfile</span></span>
<span data-ttu-id="af191-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af191-123">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="af191-123">-EnvironmentVariable</span></span>
<span data-ttu-id="af191-124">환경 변수 컬렉션</span><span class="sxs-lookup"><span data-stu-id="af191-124">Collection of environment variables</span></span>

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

### <span data-ttu-id="af191-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="af191-125">-InputObject</span></span>
<span data-ttu-id="af191-126">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="af191-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="af191-127">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="af191-127">-InstanceCount</span></span>
<span data-ttu-id="af191-128">인스턴스 수</span><span class="sxs-lookup"><span data-stu-id="af191-128">Instance count</span></span>

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

### <span data-ttu-id="af191-129">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="af191-129">-JvmOption</span></span>
<span data-ttu-id="af191-130">JVM 매개 변수</span><span class="sxs-lookup"><span data-stu-id="af191-130">JVM parameter</span></span>

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

### <span data-ttu-id="af191-131">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="af191-131">-MemoryInGb</span></span>
<span data-ttu-id="af191-132">필요한 메모리 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="af191-132">Required Memory size in GB</span></span>

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

### <span data-ttu-id="af191-133">-이름</span><span class="sxs-lookup"><span data-stu-id="af191-133">-Name</span></span>
<span data-ttu-id="af191-134">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-134">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="af191-135">-NoWait</span><span class="sxs-lookup"><span data-stu-id="af191-135">-NoWait</span></span>
<span data-ttu-id="af191-136">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="af191-136">Run the command asynchronously</span></span>

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

### <span data-ttu-id="af191-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af191-137">-ResourceGroupName</span></span>
<span data-ttu-id="af191-138">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-138">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="af191-139">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af191-139">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="af191-140">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="af191-140">-RuntimeVersion</span></span>
<span data-ttu-id="af191-141">런타임 버전</span><span class="sxs-lookup"><span data-stu-id="af191-141">Runtime version</span></span>

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

### <span data-ttu-id="af191-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="af191-142">-ServiceName</span></span>
<span data-ttu-id="af191-143">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-143">The name of the Service resource.</span></span>

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

### <span data-ttu-id="af191-144">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="af191-144">-SourceArtifactSelector</span></span>
<span data-ttu-id="af191-145">다중 모듈 프로젝트의 배포에 사용 되는 아티팩트의 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-145">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="af191-146">이는 대상 모듈/프로젝트에 대 한 상대 경로를 지켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-146">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="af191-147">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="af191-147">-SourceRelativePath</span></span>
<span data-ttu-id="af191-148">원본을 저장 하는 저장소의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-148">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="af191-149">-SourceType</span><span class="sxs-lookup"><span data-stu-id="af191-149">-SourceType</span></span>
<span data-ttu-id="af191-150">업로드 된 원본 유형</span><span class="sxs-lookup"><span data-stu-id="af191-150">Type of the source uploaded</span></span>

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

### <span data-ttu-id="af191-151">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="af191-151">-SourceVersion</span></span>
<span data-ttu-id="af191-152">원본 버전</span><span class="sxs-lookup"><span data-stu-id="af191-152">Version of the source</span></span>

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

### <span data-ttu-id="af191-153">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="af191-153">-SubscriptionId</span></span>
<span data-ttu-id="af191-154">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af191-154">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="af191-155">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-155">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="af191-156">-확인</span><span class="sxs-lookup"><span data-stu-id="af191-156">-Confirm</span></span>
<span data-ttu-id="af191-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af191-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af191-158">-WhatIf</span></span>
<span data-ttu-id="af191-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="af191-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af191-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af191-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af191-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af191-161">CommonParameters</span></span>
<span data-ttu-id="af191-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af191-163">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="af191-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af191-164">입력</span><span class="sxs-lookup"><span data-stu-id="af191-164">INPUTS</span></span>

### <span data-ttu-id="af191-165">SpringCloud. ISpringCloudIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="af191-165">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.ISpringCloudIdentity</span></span>

## <span data-ttu-id="af191-166">출력</span><span class="sxs-lookup"><span data-stu-id="af191-166">OUTPUTS</span></span>

### <span data-ttu-id="af191-167">SpringCloud. PowerShell. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="af191-167">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="af191-168">상속자</span><span class="sxs-lookup"><span data-stu-id="af191-168">NOTES</span></span>

<span data-ttu-id="af191-169">별칭과</span><span class="sxs-lookup"><span data-stu-id="af191-169">ALIASES</span></span>

<span data-ttu-id="af191-170">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="af191-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="af191-171">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="af191-172">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="af191-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="af191-173">INPUTOBJECT <ISpringCloudIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="af191-173">INPUTOBJECT <ISpringCloudIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="af191-174">`[AppName <String>]`: 앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-174">`[AppName <String>]`: The name of the App resource.</span></span>
  - <span data-ttu-id="af191-175">`[BindingName <String>]`: 바인딩 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-175">`[BindingName <String>]`: The name of the Binding resource.</span></span>
  - <span data-ttu-id="af191-176">`[CertificateName <String>]`: 인증서 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-176">`[CertificateName <String>]`: The name of the certificate resource.</span></span>
  - <span data-ttu-id="af191-177">`[DeploymentName <String>]`: 배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-177">`[DeploymentName <String>]`: The name of the Deployment resource.</span></span>
  - <span data-ttu-id="af191-178">`[DomainName <String>]`: 사용자 지정 도메인 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-178">`[DomainName <String>]`: The name of the custom domain resource.</span></span>
  - <span data-ttu-id="af191-179">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="af191-179">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="af191-180">`[Location <String>]`: 지역</span><span class="sxs-lookup"><span data-stu-id="af191-180">`[Location <String>]`: the region</span></span>
  - <span data-ttu-id="af191-181">`[ResourceGroupName <String>]`: 리소스를 포함 하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-181">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="af191-182">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af191-182">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="af191-183">`[ServiceName <String>]`: 서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af191-183">`[ServiceName <String>]`: The name of the Service resource.</span></span>
  - <span data-ttu-id="af191-184">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="af191-184">`[SubscriptionId <String>]`: Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="af191-185">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="af191-185">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="af191-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af191-186">RELATED LINKS</span></span>

