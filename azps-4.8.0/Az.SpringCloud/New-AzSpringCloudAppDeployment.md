---
external help file: ''
Module Name: Az.SpringCloud
online version: https://docs.microsoft.com/en-us/powershell/module/az.SpringCloud/new-azSpringCloudappdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SpringCloud/help/New-AzSpringCloudAppDeployment.md
ms.openlocfilehash: 0669371f589722e3da18e554df98dbf7d193ccc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213930"
---
# <span data-ttu-id="742af-101">New-AzSpringCloudAppDeployment</span><span class="sxs-lookup"><span data-stu-id="742af-101">New-AzSpringCloudAppDeployment</span></span>

## <span data-ttu-id="742af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="742af-102">SYNOPSIS</span></span>
<span data-ttu-id="742af-103">새 배포를 만들거나 종료 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-103">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="742af-104">구문과</span><span class="sxs-lookup"><span data-stu-id="742af-104">SYNTAX</span></span>

```
New-AzSpringCloudAppDeployment -AppName <String> -Name <String> -ResourceGroupName <String>
 -ServiceName <String> [-SubscriptionId <String>] [-Cpu <Int32>] [-EnvironmentVariable <Hashtable>]
 [-InstanceCount <Int32>] [-JvmOption <String>] [-MemoryInGb <Int32>] [-RuntimeVersion <RuntimeVersion>]
 [-SourceArtifactSelector <String>] [-SourceRelativePath <String>] [-SourceType <UserSourceType>]
 [-SourceVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="742af-105">설명은</span><span class="sxs-lookup"><span data-stu-id="742af-105">DESCRIPTION</span></span>
<span data-ttu-id="742af-106">새 배포를 만들거나 종료 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-106">Create a new Deployment or update an exiting Deployment.</span></span>

## <span data-ttu-id="742af-107">예제의</span><span class="sxs-lookup"><span data-stu-id="742af-107">EXAMPLES</span></span>

### <span data-ttu-id="742af-108">예제 1: 예제 1: 스프링 클라우드 배포 만들기</span><span class="sxs-lookup"><span data-stu-id="742af-108">Example 1: Example 1: Create a spring cloud deployment.</span></span>
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

<span data-ttu-id="742af-109">스프링 클라우드 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="742af-109">Create a spring cloud deployment.</span></span>

## <span data-ttu-id="742af-110">변수</span><span class="sxs-lookup"><span data-stu-id="742af-110">PARAMETERS</span></span>

### <span data-ttu-id="742af-111">-AppName</span><span class="sxs-lookup"><span data-stu-id="742af-111">-AppName</span></span>
<span data-ttu-id="742af-112">앱 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-112">The name of the App resource.</span></span>

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

### <span data-ttu-id="742af-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="742af-113">-AsJob</span></span>
<span data-ttu-id="742af-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="742af-114">Run the command as a job</span></span>

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

### <span data-ttu-id="742af-115">-Cpu</span><span class="sxs-lookup"><span data-stu-id="742af-115">-Cpu</span></span>
<span data-ttu-id="742af-116">필수 CPU</span><span class="sxs-lookup"><span data-stu-id="742af-116">Required CPU</span></span>

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

### <span data-ttu-id="742af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="742af-117">-DefaultProfile</span></span>
<span data-ttu-id="742af-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="742af-119">-EnvironmentVariable</span><span class="sxs-lookup"><span data-stu-id="742af-119">-EnvironmentVariable</span></span>
<span data-ttu-id="742af-120">환경 변수 컬렉션</span><span class="sxs-lookup"><span data-stu-id="742af-120">Collection of environment variables</span></span>

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

### <span data-ttu-id="742af-121">-InstanceCount</span><span class="sxs-lookup"><span data-stu-id="742af-121">-InstanceCount</span></span>
<span data-ttu-id="742af-122">인스턴스 수</span><span class="sxs-lookup"><span data-stu-id="742af-122">Instance count</span></span>

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

### <span data-ttu-id="742af-123">-JvmOption</span><span class="sxs-lookup"><span data-stu-id="742af-123">-JvmOption</span></span>
<span data-ttu-id="742af-124">JVM 매개 변수</span><span class="sxs-lookup"><span data-stu-id="742af-124">JVM parameter</span></span>

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

### <span data-ttu-id="742af-125">-MemoryInGb</span><span class="sxs-lookup"><span data-stu-id="742af-125">-MemoryInGb</span></span>
<span data-ttu-id="742af-126">필요한 메모리 크기 (GB)</span><span class="sxs-lookup"><span data-stu-id="742af-126">Required Memory size in GB</span></span>

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

### <span data-ttu-id="742af-127">-이름</span><span class="sxs-lookup"><span data-stu-id="742af-127">-Name</span></span>
<span data-ttu-id="742af-128">배포 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-128">The name of the Deployment resource.</span></span>

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

### <span data-ttu-id="742af-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="742af-129">-NoWait</span></span>
<span data-ttu-id="742af-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="742af-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="742af-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="742af-131">-ResourceGroupName</span></span>
<span data-ttu-id="742af-132">리소스가 포함 된 자원 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-132">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="742af-133">Azure Resource Manager API 또는 포털에서이 값을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="742af-133">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="742af-134">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="742af-134">-RuntimeVersion</span></span>
<span data-ttu-id="742af-135">런타임 버전</span><span class="sxs-lookup"><span data-stu-id="742af-135">Runtime version</span></span>

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

### <span data-ttu-id="742af-136">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="742af-136">-ServiceName</span></span>
<span data-ttu-id="742af-137">서비스 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-137">The name of the Service resource.</span></span>

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

### <span data-ttu-id="742af-138">-SourceArtifactSelector</span><span class="sxs-lookup"><span data-stu-id="742af-138">-SourceArtifactSelector</span></span>
<span data-ttu-id="742af-139">다중 모듈 프로젝트의 배포에 사용 되는 아티팩트의 선택기입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-139">Selector for the artifact to be used for the deployment for multi-module projects.</span></span>
<span data-ttu-id="742af-140">이는 대상 모듈/프로젝트에 대 한 상대 경로를 지켜야 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-140">This should bethe relative path to the target module/project.</span></span>

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

### <span data-ttu-id="742af-141">-SourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="742af-141">-SourceRelativePath</span></span>
<span data-ttu-id="742af-142">원본을 저장 하는 저장소의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="742af-142">Relative path of the storage which stores the source</span></span>

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

### <span data-ttu-id="742af-143">-SourceType</span><span class="sxs-lookup"><span data-stu-id="742af-143">-SourceType</span></span>
<span data-ttu-id="742af-144">업로드 된 원본 유형</span><span class="sxs-lookup"><span data-stu-id="742af-144">Type of the source uploaded</span></span>

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

### <span data-ttu-id="742af-145">-SourceVersion</span><span class="sxs-lookup"><span data-stu-id="742af-145">-SourceVersion</span></span>
<span data-ttu-id="742af-146">원본 버전</span><span class="sxs-lookup"><span data-stu-id="742af-146">Version of the source</span></span>

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

### <span data-ttu-id="742af-147">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="742af-147">-SubscriptionId</span></span>
<span data-ttu-id="742af-148">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 ID를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="742af-148">Gets subscription ID which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="742af-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-149">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="742af-150">-확인</span><span class="sxs-lookup"><span data-stu-id="742af-150">-Confirm</span></span>
<span data-ttu-id="742af-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="742af-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="742af-152">-WhatIf</span></span>
<span data-ttu-id="742af-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="742af-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="742af-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="742af-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="742af-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="742af-155">CommonParameters</span></span>
<span data-ttu-id="742af-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="742af-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="742af-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="742af-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="742af-158">입력</span><span class="sxs-lookup"><span data-stu-id="742af-158">INPUTS</span></span>

## <span data-ttu-id="742af-159">출력</span><span class="sxs-lookup"><span data-stu-id="742af-159">OUTPUTS</span></span>

### <span data-ttu-id="742af-160">SpringCloud. PowerShell. Api20190501Preview. IDeploymentResource</span><span class="sxs-lookup"><span data-stu-id="742af-160">Microsoft.Azure.PowerShell.Cmdlets.SpringCloud.Models.Api20190501Preview.IDeploymentResource</span></span>

## <span data-ttu-id="742af-161">상속자</span><span class="sxs-lookup"><span data-stu-id="742af-161">NOTES</span></span>

<span data-ttu-id="742af-162">별칭과</span><span class="sxs-lookup"><span data-stu-id="742af-162">ALIASES</span></span>

## <span data-ttu-id="742af-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="742af-163">RELATED LINKS</span></span>

