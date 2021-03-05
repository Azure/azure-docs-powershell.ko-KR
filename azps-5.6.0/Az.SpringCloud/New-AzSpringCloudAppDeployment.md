---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: de1f09fe6fd484345ebf4ebd7ae2a27d4640c694
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010192"
---
# <span data-ttu-id="4cf05-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="4cf05-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="4cf05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cf05-102">SYNOPSIS</span></span>
<span data-ttu-id="4cf05-103">새 배포를 만들거나 종료 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="4cf05-104">구문</span><span class="sxs-lookup"><span data-stu-id="4cf05-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4cf05-105">설명</span><span class="sxs-lookup"><span data-stu-id="4cf05-105">DESCRIPTION</span></span>
<span data-ttu-id="4cf05-106">새 배포를 만들거나 종료 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="4cf05-107">예제</span><span class="sxs-lookup"><span data-stu-id="4cf05-107">EXAMPLES</span></span>

### <span data-ttu-id="4cf05-108">예제 1: 예제 1: 스프링 클라우드 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="4cf05-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
```powershell
PS C:\> New-AzSpringCloudAppDeployment -ResourceGroupName spring-cloud-rp -name spring-cloud-service -AppName gateway -DeploymentName default

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

<span data-ttu-id="4cf05-109">스프링 클라우드 배포를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="4cf05-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4cf05-110">PARAMETERS</span></span>

### <span data-ttu-id="4cf05-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="4cf05-111">-AppName</span></span>
<span data-ttu-id="4cf05-112">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="4cf05-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4cf05-113">-AsJob</span></span>
<span data-ttu-id="4cf05-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4cf05-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="4cf05-115">-Cpu</span></span>
<span data-ttu-id="4cf05-116">필수 CPU</span><span class="sxs-lookup"><span data-stu-id="4cf05-116">Required CPU</span></span>

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

### <span data-ttu-id="4cf05-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cf05-117">-DefaultProfile</span></span>
<span data-ttu-id="4cf05-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cf05-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="4cf05-119">-EnvironmentVariable</span></span>
<span data-ttu-id="4cf05-120">환경 변수 컬렉션</span><span class="sxs-lookup"><span data-stu-id="4cf05-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="4cf05-121">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="4cf05-121">-JvmOption</span></span>
<span data-ttu-id="4cf05-122">JVM 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4cf05-122">JVM parameter</span></span>

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

### <span data-ttu-id="4cf05-123">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="4cf05-123">-MemoryInGb</span></span>
<span data-ttu-id="4cf05-124">필요한 메모리 크기(GB)입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-124">Required Memory size in GB</span></span>

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

### <span data-ttu-id="4cf05-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4cf05-125">-Name</span></span>
<span data-ttu-id="4cf05-126">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-126">The name of the Deployment resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DeploymentName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cf05-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4cf05-127">-NoWait</span></span>
<span data-ttu-id="4cf05-128">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="4cf05-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4cf05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cf05-129">-ResourceGroupName</span></span>
<span data-ttu-id="4cf05-130">리소스를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4cf05-131">Azure Resource Manager API 또는 포털에서 이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4cf05-132">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="4cf05-132">-RuntimeVersion</span></span>
<span data-ttu-id="4cf05-133">런타임 버전</span><span class="sxs-lookup"><span data-stu-id="4cf05-133">Runtime version</span></span>

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

### <span data-ttu-id="4cf05-134">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="4cf05-134">-ServiceName</span></span>
<span data-ttu-id="4cf05-135">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-135">The name of the Service resource.</span></span>

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

### <span data-ttu-id="4cf05-136">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="4cf05-136">-SourceArtifactSelector</span></span>
<span data-ttu-id="4cf05-137">다중 모듈 프로젝트에 대한 배포에 사용할 아티팩트의 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-137">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="4cf05-138">대상 모듈/프로젝트에 대한 상대 경로를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-138">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="4cf05-139">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="4cf05-139">-SourceRelativePath</span></span>
<span data-ttu-id="4cf05-140">원본을 저장하는 저장소의 상대 경로</span><span class="sxs-lookup"><span data-stu-id="4cf05-140">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="4cf05-141">-SourceType</span><span class="sxs-lookup"><span data-stu-id="4cf05-141">-SourceType</span></span>
<span data-ttu-id="4cf05-142">업로드된 원본 유형</span><span class="sxs-lookup"><span data-stu-id="4cf05-142">Type of the source uploaded</span></span>

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

### <span data-ttu-id="4cf05-143">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="4cf05-143">-SourceVersion</span></span>
<span data-ttu-id="4cf05-144">원본 버전</span><span class="sxs-lookup"><span data-stu-id="4cf05-144">Version of the source</span></span>

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

### <span data-ttu-id="4cf05-145">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cf05-145">-SubscriptionId</span></span>
<span data-ttu-id="4cf05-146">Microsoft Azure 구독을 고유하게 식별하는 구독 ID를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-146">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4cf05-147">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-147">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4cf05-148">-확인</span><span class="sxs-lookup"><span data-stu-id="4cf05-148">-Confirm</span></span>
<span data-ttu-id="4cf05-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4cf05-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4cf05-150">-WhatIf</span></span>
<span data-ttu-id="4cf05-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4cf05-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4cf05-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cf05-153">CommonParameters</span></span>
<span data-ttu-id="4cf05-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4cf05-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cf05-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cf05-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cf05-156">입력</span><span class="sxs-lookup"><span data-stu-id="4cf05-156">INPUTS</span></span>

## <span data-ttu-id="4cf05-157">출력</span><span class="sxs-lookup"><span data-stu-id="4cf05-157">OUTPUTS</span></span>

### <span data-ttu-id="4cf05-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="4cf05-158">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20200701.IDeploymentResource</span></span>

## <span data-ttu-id="4cf05-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4cf05-159">NOTES</span></span>

<span data-ttu-id="4cf05-160">별칭</span><span class="sxs-lookup"><span data-stu-id="4cf05-160">ALIASES</span></span>

## <span data-ttu-id="4cf05-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cf05-161">RELATED LINKS</span></span>

