---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 97a1fa7aa5488034fa1f0147ae5a06ff639ecc06
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969056"
---
# <span data-ttu-id="e558e-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="e558e-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="e558e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e558e-102">SYNOPSIS</span></span>
<span data-ttu-id="e558e-103">함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-103">Creates a function app.</span></span>

## <span data-ttu-id="e558e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e558e-104">SYNTAX</span></span>

### <span data-ttu-id="e558e-105">소비(기본값)</span><span class="sxs-lookup"><span data-stu-id="e558e-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e558e-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="e558e-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e558e-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="e558e-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e558e-108">설명</span><span class="sxs-lookup"><span data-stu-id="e558e-108">DESCRIPTION</span></span>
<span data-ttu-id="e558e-109">함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-109">Creates a function app.</span></span>

## <span data-ttu-id="e558e-110">예제</span><span class="sxs-lookup"><span data-stu-id="e558e-110">EXAMPLES</span></span>

### <span data-ttu-id="e558e-111">예제 1: 미국 중부에서 소비 PowerShell 함수 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="e558e-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="e558e-112">이 명령은 미국 중부에 소비 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="e558e-113">예제 2: 서비스 계획에 호스트될 PowerShell 함수 앱을 만드겠습니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="e558e-114">이 명령은 서비스 계획에 호스트되는 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="e558e-115">예제 3: 개인 ACR 이미지를 사용하여 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="e558e-116">이 명령은 개인 ACR 이미지를 사용하여 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="e558e-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e558e-117">PARAMETERS</span></span>

### <span data-ttu-id="e558e-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="e558e-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="e558e-119">추가할 App Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-119">Instrumentation key of App Insights to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsKey

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="e558e-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="e558e-121">함수 앱에 추가할 기존 App Insights 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-121">Name of the existing App Insights project to be added to the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AppInsightsName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="e558e-122">-AppSetting</span></span>
<span data-ttu-id="e558e-123">함수 앱 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-123">Function app settings.</span></span>

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

### <span data-ttu-id="e558e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e558e-124">-AsJob</span></span>
<span data-ttu-id="e558e-125">cmdlet을 백그라운드 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="e558e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e558e-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="e558e-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="e558e-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="e558e-128">함수 앱 만들기 중에 애플리케이션 인사이트 리소스 만들기를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="e558e-129">로그를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-129">No logs will be available.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: DisableAppInsights

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="e558e-130">-DockerImageName</span></span>
<span data-ttu-id="e558e-131">Linux만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-131">Linux only.</span></span>
<span data-ttu-id="e558e-132">Docker Registry의 컨테이너 이미지 이름(예: publisher/image-name:tag)입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

```yaml
Type: System.String
Parameter Sets: CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e558e-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="e558e-134">컨테이너 레지스트리 사용자 이름 및 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-134">The container registry user name and password.</span></span>
<span data-ttu-id="e558e-135">개인 레지스트리에 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-135">Required for private registries.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: CustomDockerImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="e558e-136">-FunctionsVersion</span></span>
<span data-ttu-id="e558e-137">Functions 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-137">The Functions version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="e558e-138">-IdentityID</span></span>
<span data-ttu-id="e558e-139">함수 앱과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="e558e-140">사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e558e-141">-IdentityType</span></span>
<span data-ttu-id="e558e-142">함수 앱에 사용되는 ID 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="e558e-143">이 매개 변수에 대해 허용되는 값은 - SystemAssigned - UserAssigned입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Support.ManagedServiceIdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-144">-Location</span><span class="sxs-lookup"><span data-stu-id="e558e-144">-Location</span></span>
<span data-ttu-id="e558e-145">소비 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-145">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-146">-Name</span><span class="sxs-lookup"><span data-stu-id="e558e-146">-Name</span></span>
<span data-ttu-id="e558e-147">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-147">The name of the function app.</span></span>

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

### <span data-ttu-id="e558e-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e558e-148">-NoWait</span></span>
<span data-ttu-id="e558e-149">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="e558e-150">작업이 성공적으로 완료된지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="e558e-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="e558e-151">-OSType</span></span>
<span data-ttu-id="e558e-152">함수 앱을 호스트하는 OS입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-152">The OS to host the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e558e-153">-PassThru</span></span>
<span data-ttu-id="e558e-154">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="e558e-155">-PlanName</span><span class="sxs-lookup"><span data-stu-id="e558e-155">-PlanName</span></span>
<span data-ttu-id="e558e-156">서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-156">The name of the service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, CustomDockerImage
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e558e-157">-ResourceGroupName</span></span>
<span data-ttu-id="e558e-158">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="e558e-159">-런타임</span><span class="sxs-lookup"><span data-stu-id="e558e-159">-Runtime</span></span>
<span data-ttu-id="e558e-160">함수 런타임입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-160">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="e558e-161">-RuntimeVersion</span></span>
<span data-ttu-id="e558e-162">함수 런타임입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-162">The function runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAppServicePlan, Consumption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e558e-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e558e-163">-StorageAccountName</span></span>
<span data-ttu-id="e558e-164">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="e558e-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e558e-165">-SubscriptionId</span></span>
<span data-ttu-id="e558e-166">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="e558e-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="e558e-167">-Tag</span></span>
<span data-ttu-id="e558e-168">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-168">Resource tags.</span></span>

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

### <span data-ttu-id="e558e-169">-확인</span><span class="sxs-lookup"><span data-stu-id="e558e-169">-Confirm</span></span>
<span data-ttu-id="e558e-170">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e558e-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e558e-171">-WhatIf</span></span>
<span data-ttu-id="e558e-172">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e558e-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e558e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e558e-174">CommonParameters</span></span>
<span data-ttu-id="e558e-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e558e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e558e-176">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e558e-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e558e-177">입력</span><span class="sxs-lookup"><span data-stu-id="e558e-177">INPUTS</span></span>

## <span data-ttu-id="e558e-178">출력</span><span class="sxs-lookup"><span data-stu-id="e558e-178">OUTPUTS</span></span>

### <span data-ttu-id="e558e-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="e558e-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="e558e-180">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e558e-180">NOTES</span></span>

<span data-ttu-id="e558e-181">별칭</span><span class="sxs-lookup"><span data-stu-id="e558e-181">ALIASES</span></span>

## <span data-ttu-id="e558e-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e558e-182">RELATED LINKS</span></span>

