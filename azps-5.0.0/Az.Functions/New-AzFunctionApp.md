---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionApp.md
ms.openlocfilehash: 7a01cd2b6810d8405f2aba0a56e232891bd036f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215422"
---
# <span data-ttu-id="bfc5e-101">New-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="bfc5e-101">New-AzFunctionApp</span></span>

## <span data-ttu-id="bfc5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfc5e-102">SYNOPSIS</span></span>
<span data-ttu-id="bfc5e-103">함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-103">Creates a function app.</span></span>

## <span data-ttu-id="bfc5e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfc5e-104">SYNTAX</span></span>

### <span data-ttu-id="bfc5e-105">소비량 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bfc5e-105">Consumption (Default)</span></span>
```
New-AzFunctionApp -Location <String> -Name <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfc5e-106">ByAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="bfc5e-106">ByAppServicePlan</span></span>
```
New-AzFunctionApp -Name <String> -PlanName <String> -ResourceGroupName <String> -Runtime <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-FunctionsVersion <String>] [-IdentityID <String[]>]
 [-IdentityType <ManagedServiceIdentityType>] [-OSType <String>] [-PassThru] [-RuntimeVersion <String>]
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="bfc5e-107">CustomDockerImage</span><span class="sxs-lookup"><span data-stu-id="bfc5e-107">CustomDockerImage</span></span>
```
New-AzFunctionApp -DockerImageName <String> -Name <String> -PlanName <String> -ResourceGroupName <String>
 -StorageAccountName <String> [-ApplicationInsightsKey <String>] [-ApplicationInsightsName <String>]
 [-AppSetting <Hashtable>] [-DisableApplicationInsights] [-DockerRegistryCredential <PSCredential>]
 [-IdentityID <String[]>] [-IdentityType <ManagedServiceIdentityType>] [-PassThru] [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bfc5e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bfc5e-108">DESCRIPTION</span></span>
<span data-ttu-id="bfc5e-109">함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-109">Creates a function app.</span></span>

## <span data-ttu-id="bfc5e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bfc5e-110">EXAMPLES</span></span>

### <span data-ttu-id="bfc5e-111">예제 1: 중부 US에서 소비 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-111">Example 1: Create a consumption PowerShell function app in Central US.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -Location centralUS `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="bfc5e-112">이 명령은 중부 US에 소비 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-112">This command creates a consumption PowerShell function app in Central US.</span></span>

### <span data-ttu-id="bfc5e-113">예제 2: 서비스 계획에 호스팅되는 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-113">Example 2: Create a PowerShell function app which will be hosted in a service plan.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -Runtime PowerShell
```

<span data-ttu-id="bfc5e-114">이 명령은 서비스 계획에 호스팅되는 PowerShell 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-114">This command creates a PowerShell function app which will be hosted in a service plan.</span></span>

### <span data-ttu-id="bfc5e-115">예제 3: 전용 ACR 이미지를 사용 하 여 함수 앱 만들기</span><span class="sxs-lookup"><span data-stu-id="bfc5e-115">Example 3: Create a function app using a using a private ACR image.</span></span>
```powershell
PS C:\> New-AzFunctionApp -Name MyUniqueFunctionAppName `
                          -ResourceGroupName MyResourceGroupName `
                          -PlanName MyPlanName `
                          -StorageAccount MyStorageAccountName `
                          -DockerImageName myacr.azurecr.io/myimage:tag

```

<span data-ttu-id="bfc5e-116">이 명령은 전용 ACR 이미지를 사용 하 여 함수 앱을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-116">This command creates a function app using a using a private ACR image.</span></span>

## <span data-ttu-id="bfc5e-117">변수</span><span class="sxs-lookup"><span data-stu-id="bfc5e-117">PARAMETERS</span></span>

### <span data-ttu-id="bfc5e-118">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="bfc5e-118">-ApplicationInsightsKey</span></span>
<span data-ttu-id="bfc5e-119">추가할 앱 Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-119">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="bfc5e-120">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="bfc5e-120">-ApplicationInsightsName</span></span>
<span data-ttu-id="bfc5e-121">함수 앱에 추가할 기존 App Insights 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-121">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="bfc5e-122">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="bfc5e-122">-AppSetting</span></span>
<span data-ttu-id="bfc5e-123">함수 앱 설정</span><span class="sxs-lookup"><span data-stu-id="bfc5e-123">Function app settings.</span></span>

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

### <span data-ttu-id="bfc5e-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfc5e-124">-AsJob</span></span>
<span data-ttu-id="bfc5e-125">백그라운드 작업으로 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-125">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="bfc5e-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfc5e-126">-DefaultProfile</span></span>


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

### <span data-ttu-id="bfc5e-127">-DisableApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="bfc5e-127">-DisableApplicationInsights</span></span>
<span data-ttu-id="bfc5e-128">함수 앱을 만드는 동안 application insights 리소스 만들기를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-128">Disable creating application insights resource during the function app creation.</span></span>
<span data-ttu-id="bfc5e-129">로그를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-129">No logs will be available.</span></span>

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

### <span data-ttu-id="bfc5e-130">-DockerImageName</span><span class="sxs-lookup"><span data-stu-id="bfc5e-130">-DockerImageName</span></span>
<span data-ttu-id="bfc5e-131">Linux만.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-131">Linux only.</span></span>
<span data-ttu-id="bfc5e-132">Docker 레지스트리의 컨테이너 이미지 이름 (예: publisher/image-name: tag).</span><span class="sxs-lookup"><span data-stu-id="bfc5e-132">Container image name from Docker Registry, e.g. publisher/image-name:tag.</span></span>

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

### <span data-ttu-id="bfc5e-133">-DockerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="bfc5e-133">-DockerRegistryCredential</span></span>
<span data-ttu-id="bfc5e-134">컨테이너 레지스트리 사용자 이름 및 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-134">The container registry user name and password.</span></span>
<span data-ttu-id="bfc5e-135">개인 레지스트리에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-135">Required for private registries.</span></span>

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

### <span data-ttu-id="bfc5e-136">-FunctionsVersion</span><span class="sxs-lookup"><span data-stu-id="bfc5e-136">-FunctionsVersion</span></span>
<span data-ttu-id="bfc5e-137">함수 버전.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-137">The Functions version.</span></span>

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

### <span data-ttu-id="bfc5e-138">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="bfc5e-138">-IdentityID</span></span>
<span data-ttu-id="bfc5e-139">함수 앱과 연결 된 사용자 id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-139">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="bfc5e-140">사용자 id 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName} ' 형식으로 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-140">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="bfc5e-141">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="bfc5e-141">-IdentityType</span></span>
<span data-ttu-id="bfc5e-142">함수 앱에 사용 되는 id 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-142">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="bfc5e-143">이 매개 변수에 허용 되는 값은-SystemAssigned-UserAssigned 됨입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-143">The acceptable values for this parameter are: - SystemAssigned - UserAssigned</span></span>

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

### <span data-ttu-id="bfc5e-144">-위치</span><span class="sxs-lookup"><span data-stu-id="bfc5e-144">-Location</span></span>
<span data-ttu-id="bfc5e-145">소비량 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-145">The location for the consumption plan.</span></span>

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

### <span data-ttu-id="bfc5e-146">-이름</span><span class="sxs-lookup"><span data-stu-id="bfc5e-146">-Name</span></span>
<span data-ttu-id="bfc5e-147">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-147">The name of the function app.</span></span>

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

### <span data-ttu-id="bfc5e-148">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bfc5e-148">-NoWait</span></span>
<span data-ttu-id="bfc5e-149">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-149">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="bfc5e-150">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-150">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bfc5e-151">-OSType</span><span class="sxs-lookup"><span data-stu-id="bfc5e-151">-OSType</span></span>
<span data-ttu-id="bfc5e-152">함수 앱을 호스트 하는 OS입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-152">The OS to host the function app.</span></span>

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

### <span data-ttu-id="bfc5e-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfc5e-153">-PassThru</span></span>
<span data-ttu-id="bfc5e-154">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-154">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="bfc5e-155">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="bfc5e-155">-PlanName</span></span>
<span data-ttu-id="bfc5e-156">서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-156">The name of the service plan.</span></span>

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

### <span data-ttu-id="bfc5e-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfc5e-157">-ResourceGroupName</span></span>
<span data-ttu-id="bfc5e-158">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-158">The name of the resource group.</span></span>

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

### <span data-ttu-id="bfc5e-159">런타임</span><span class="sxs-lookup"><span data-stu-id="bfc5e-159">-Runtime</span></span>
<span data-ttu-id="bfc5e-160">함수 런타임.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-160">The function runtime.</span></span>

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

### <span data-ttu-id="bfc5e-161">-RuntimeVersion</span><span class="sxs-lookup"><span data-stu-id="bfc5e-161">-RuntimeVersion</span></span>
<span data-ttu-id="bfc5e-162">함수 런타임.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-162">The function runtime.</span></span>

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

### <span data-ttu-id="bfc5e-163">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="bfc5e-163">-StorageAccountName</span></span>
<span data-ttu-id="bfc5e-164">저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-164">The name of the storage account.</span></span>

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

### <span data-ttu-id="bfc5e-165">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfc5e-165">-SubscriptionId</span></span>
<span data-ttu-id="bfc5e-166">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-166">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="bfc5e-167">태그</span><span class="sxs-lookup"><span data-stu-id="bfc5e-167">-Tag</span></span>
<span data-ttu-id="bfc5e-168">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-168">Resource tags.</span></span>

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

### <span data-ttu-id="bfc5e-169">-확인</span><span class="sxs-lookup"><span data-stu-id="bfc5e-169">-Confirm</span></span>
<span data-ttu-id="bfc5e-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfc5e-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfc5e-171">-WhatIf</span></span>
<span data-ttu-id="bfc5e-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfc5e-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfc5e-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfc5e-174">CommonParameters</span></span>
<span data-ttu-id="bfc5e-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfc5e-176">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfc5e-177">입력</span><span class="sxs-lookup"><span data-stu-id="bfc5e-177">INPUTS</span></span>

## <span data-ttu-id="bfc5e-178">출력</span><span class="sxs-lookup"><span data-stu-id="bfc5e-178">OUTPUTS</span></span>

### <span data-ttu-id="bfc5e-179">Api20190801. ISite의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="bfc5e-179">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="bfc5e-180">상속자</span><span class="sxs-lookup"><span data-stu-id="bfc5e-180">NOTES</span></span>

<span data-ttu-id="bfc5e-181">별칭과</span><span class="sxs-lookup"><span data-stu-id="bfc5e-181">ALIASES</span></span>

## <span data-ttu-id="bfc5e-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfc5e-182">RELATED LINKS</span></span>

