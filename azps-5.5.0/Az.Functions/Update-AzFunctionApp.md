---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionApp.md
ms.openlocfilehash: 08485ab1686b87c6421f456b53caa5d1deaf0c7d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188401"
---
# <span data-ttu-id="2e893-101">Update-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="2e893-101">Update-AzFunctionApp</span></span>

## <span data-ttu-id="2e893-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e893-102">SYNOPSIS</span></span>
<span data-ttu-id="2e893-103">함수 앱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-103">Updates a function app.</span></span>

## <span data-ttu-id="2e893-104">구문</span><span class="sxs-lookup"><span data-stu-id="2e893-104">SYNTAX</span></span>

### <span data-ttu-id="2e893-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="2e893-105">ByName (Default)</span></span>
```
Update-AzFunctionApp -Name <String> -ResourceGroupName <String> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-SubscriptionId <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2e893-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="2e893-106">ByObjectInput</span></span>
```
Update-AzFunctionApp -InputObject <ISite> [-ApplicationInsightsKey <String>]
 [-ApplicationInsightsName <String>] [-IdentityID <String>] [-IdentityType <ManagedServiceIdentityType>]
 [-PlanName <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="2e893-107">설명</span><span class="sxs-lookup"><span data-stu-id="2e893-107">DESCRIPTION</span></span>
<span data-ttu-id="2e893-108">함수 앱을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-108">Updates a function app.</span></span>

## <span data-ttu-id="2e893-109">예제</span><span class="sxs-lookup"><span data-stu-id="2e893-109">EXAMPLES</span></span>

### <span data-ttu-id="2e893-110">예제 1: 함수 앱 호스팅 계획을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-110">Example 1: Update function app hosting plan.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -PlanName NewPlanName 
```

<span data-ttu-id="2e893-111">이 명령은 함수 앱 호스팅 계획을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-111">This command updates function app hosting plan.</span></span>

### <span data-ttu-id="2e893-112">예제 2: 함수 앱에 대한 SystemAssigned 관리 ID를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-112">Example 2: Set a SystemAssigned managed identity for a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType SystemAssigned 
```

<span data-ttu-id="2e893-113">이 명령은 함수 앱에 대한 SystemAssigned 관리 ID를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-113">This command sets a SystemAssigned managed identity for a function app.</span></span>

### <span data-ttu-id="2e893-114">예제 3: 함수 앱 Application Insights를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-114">Example 3: Update function app Application Insights.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -ApplicationInsightsName ApplicationInsightsProjectName 
```

<span data-ttu-id="2e893-115">이 명령은 함수 앱 Application Insights를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-115">This command updates function app Application Insights.</span></span>

### <span data-ttu-id="2e893-116">예제 3: 함수 앱에서 관리 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-116">Example 3: Remove managed identity from a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionApp -Name MyUniqueFunctionAppName -ResourceGroupName MyResourceGroupName -IdentityType None 
```

<span data-ttu-id="2e893-117">이 명령은 함수 앱에서 관리 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-117">This command removes a managed identity from a function app.</span></span>

## <span data-ttu-id="2e893-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2e893-118">PARAMETERS</span></span>

### <span data-ttu-id="2e893-119">-ApplicationInsightsKey</span><span class="sxs-lookup"><span data-stu-id="2e893-119">-ApplicationInsightsKey</span></span>
<span data-ttu-id="2e893-120">추가할 App Insights의 계측 키입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-120">Instrumentation key of App Insights to be added.</span></span>

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

### <span data-ttu-id="2e893-121">-ApplicationInsightsName</span><span class="sxs-lookup"><span data-stu-id="2e893-121">-ApplicationInsightsName</span></span>
<span data-ttu-id="2e893-122">함수 앱에 추가할 기존 App Insights 프로젝트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-122">Name of the existing App Insights project to be added to the function app.</span></span>

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

### <span data-ttu-id="2e893-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e893-123">-AsJob</span></span>
<span data-ttu-id="2e893-124">cmdlet을 백그라운드 작업으로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-124">Runs the cmdlet as a background job.</span></span>

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

### <span data-ttu-id="2e893-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e893-125">-DefaultProfile</span></span>


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

### <span data-ttu-id="2e893-126">-IdentityID</span><span class="sxs-lookup"><span data-stu-id="2e893-126">-IdentityID</span></span>
<span data-ttu-id="2e893-127">함수 앱과 연결된 사용자 ID 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-127">Specifies the list of user identities associated with the function app.</span></span>
<span data-ttu-id="2e893-128">사용자 ARM ID 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}' 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-128">The user identity references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/identities/{identityName}'</span></span>

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

### <span data-ttu-id="2e893-129">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="2e893-129">-IdentityType</span></span>
<span data-ttu-id="2e893-130">함수 앱에 사용되는 ID 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-130">Specifies the type of identity used for the function app.</span></span>
<span data-ttu-id="2e893-131">'없음' 형식은 함수 앱에서 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-131">The type 'None' will remove any identities from the function app.</span></span>
<span data-ttu-id="2e893-132">이 매개 변수에 허용되는 값은 SystemAssigned - UserAssigned - None입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-132">The acceptable values for this parameter are: - SystemAssigned - UserAssigned - None</span></span>

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

### <span data-ttu-id="2e893-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e893-133">-InputObject</span></span>
<span data-ttu-id="2e893-134">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2e893-134">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite
Parameter Sets: ByObjectInput
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2e893-135">-Name</span><span class="sxs-lookup"><span data-stu-id="2e893-135">-Name</span></span>
<span data-ttu-id="2e893-136">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-136">The name of the function app.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e893-137">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2e893-137">-NoWait</span></span>
<span data-ttu-id="2e893-138">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-138">Starts the operation and returns immediately, before the operation is completed.</span></span>
<span data-ttu-id="2e893-139">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-139">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2e893-140">-PlanName</span><span class="sxs-lookup"><span data-stu-id="2e893-140">-PlanName</span></span>
<span data-ttu-id="2e893-141">서비스 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-141">The name of the service plan.</span></span>

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

### <span data-ttu-id="2e893-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e893-142">-ResourceGroupName</span></span>
<span data-ttu-id="2e893-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-143">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e893-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e893-144">-SubscriptionId</span></span>
<span data-ttu-id="2e893-145">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-145">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e893-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="2e893-146">-Tag</span></span>
<span data-ttu-id="2e893-147">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="2e893-147">Resource tags.</span></span>

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

### <span data-ttu-id="2e893-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2e893-148">-Confirm</span></span>
<span data-ttu-id="2e893-149">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e893-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e893-150">-WhatIf</span></span>
<span data-ttu-id="2e893-151">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2e893-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e893-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e893-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e893-153">CommonParameters</span></span>
<span data-ttu-id="2e893-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e893-155">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2e893-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e893-156">입력</span><span class="sxs-lookup"><span data-stu-id="2e893-156">INPUTS</span></span>

### <span data-ttu-id="2e893-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="2e893-157">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="2e893-158">출력</span><span class="sxs-lookup"><span data-stu-id="2e893-158">OUTPUTS</span></span>

### <span data-ttu-id="2e893-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="2e893-159">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="2e893-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2e893-160">NOTES</span></span>

<span data-ttu-id="2e893-161">별칭</span><span class="sxs-lookup"><span data-stu-id="2e893-161">ALIASES</span></span>

<span data-ttu-id="2e893-162">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2e893-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2e893-163">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e893-164">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2e893-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2e893-165">INPUTOBJECT: <ISite></span><span class="sxs-lookup"><span data-stu-id="2e893-165">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="2e893-166">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-166">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="2e893-167">`CloningInfoSourceWebAppId <String>`: ARM 앱의 리소스 ID를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-167">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="2e893-168">앱 리소스 ID는 프로덕션 슬롯 및 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-168">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="2e893-169">`[Kind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-169">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="2e893-170">`[Tag <IResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-170">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="2e893-171">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-171">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2e893-172">`[ClientAffinityEnabled <Boolean?>]`: 클라이언트 연결성을 사용하도록 설정하려면, 동일한 세션의 클라이언트 요청을 동일한 인스턴스로 라우팅하는 세션 연결 쿠키 전송을 <code>true</code> <code>false</code> 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-172">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="2e893-173">기본값은 <code>true</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-173">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="2e893-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증(TLS 상호 인증)을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-174">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="2e893-175">기본값은 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-175">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-176">`[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 콤마로 구분된 제외 경로</span><span class="sxs-lookup"><span data-stu-id="2e893-176">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="2e893-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제된 앱에 대한 애플리케이션 설정이 오버라이드됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-177">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="2e893-178">지정된 경우 이러한 설정은 원본 앱에서 복제된 설정을 오버라우트합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-178">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="2e893-179">그렇지 않으면 원본 앱의 애플리케이션 설정이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-179">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="2e893-180">`[(Any) <String>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-180">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2e893-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: 원본 앱에서 사용자 지정 호스트 이름을 복제합니다. 그렇지 않으면 <code>true</code> <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-181">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> 원본 앱에서 소스 제어를 복제합니다. 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-182">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> 원본 및 대상 앱에 대한 부하 분산을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-183">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="2e893-184">`[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-184">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="2e893-185">이 ID는 동일한 스냅숏을 사용하기 위해 여러 복제 작업을 함께 관련합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-185">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="2e893-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="2e893-186">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="2e893-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어치고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-187">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-188">`[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서부 또는 북유럽</span><span class="sxs-lookup"><span data-stu-id="2e893-188">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="2e893-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM 사용할 Traffic Manager 프로필의 리소스 ID(있는 경우)를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-189">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="2e893-190">Traffic Manager 리소스 ID는 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-190">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="2e893-191">`[CloningInfoTrafficManagerProfileName <String>]`: 만들 Traffic Manager 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-191">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="2e893-192">Traffic Manager 프로필이 아직 없는 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-192">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="2e893-193">`[Config <ISiteConfig>]`: 앱의 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-193">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="2e893-194">`IsPushEnabled <Boolean>`: 푸시 엔드포인트를 사용하도록 설정하는지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-194">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="2e893-195">`[ActionMinProcessExecutionTime <String>]`: 작업을 수행하기 전에 프로세스가 실행되어야 하는 최소 시간</span><span class="sxs-lookup"><span data-stu-id="2e893-195">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="2e893-196">`[ActionType <AutoHealActionType?>]`: 수행될 미리 정의된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-196">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="2e893-197">`[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용하도록 설정한 경우, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-197">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-198">`[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-198">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="2e893-199">`[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-199">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="2e893-200">`[AppCommandLine <String>]`: 앱 명령줄을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-200">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="2e893-201">`[AppSetting <INameValuePair[]>]`: 애플리케이션 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-201">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="2e893-202">`[Name <String>]`: 페어링 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-202">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="2e893-203">`[Value <String>]`: 쌍 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-203">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="2e893-204">`[AutoHealEnabled <Boolean?>]`: 자동 고치기 사용이 설정된 경우, 그렇지 않은 <code>true</code> <code>false</code> 경우.</span><span class="sxs-lookup"><span data-stu-id="2e893-204">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-205">`[AutoSwapSlotName <String>]`: 슬롯 이름을 자동 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-205">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="2e893-206">`[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-206">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="2e893-207">`[ConnectionString <String>]`: 연결 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-207">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="2e893-208">`[Name <String>]`: 연결 문자열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-208">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="2e893-209">`[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-209">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="2e893-210">`[CorAllowedOrigin <String[]>]`: 원본 간 호출을 허용해야 하는 원본 목록을 얻거나 설정합니다(예: http://example.com:12345)</span><span class="sxs-lookup"><span data-stu-id="2e893-210">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="2e893-211">"\*"를 사용하여 모두 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-211">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="2e893-212">`[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용하여 CORS 요청이 허용될지 여부를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-212">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="2e893-213">자세한         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         내용은 다음을 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-213">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="2e893-214">`[CustomActionExe <String>]`: 실행할 실행 가능.</span><span class="sxs-lookup"><span data-stu-id="2e893-214">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="2e893-215">`[CustomActionParameter <String>]`: 실행 가능한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-215">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="2e893-216">`[DefaultDocument <String[]>]`: 기본 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-216">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="2e893-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-217">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-218">`[DocumentRoot <String>]`: 문서 루트입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-218">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="2e893-219">`[DynamicTagsJson <String>]`: 푸시 등록 엔드포인트의 사용자 클레임에서 평가할 동적 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-219">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="2e893-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: 램프업 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-220">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="2e893-221">`[ActionHostName <String>]`: 결정된 경우 트래픽이 리디렉션될 슬롯의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-221">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="2e893-222">예:</span><span class="sxs-lookup"><span data-stu-id="2e893-222">E.g.</span></span> <span data-ttu-id="2e893-223">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="2e893-223">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="2e893-224">`[ChangeDecisionCallbackUrl <String>]`: URL을 지정할 수 있는 TiPCallback 사이트 확장에서 사용자 지정 의사 결정 알고리즘을 제공하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-224">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="2e893-225">스캐폴드 및 계약에 대한 TiPCallback 사이트 확장을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2e893-225">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="2e893-226"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="2e893-226">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="2e893-227">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 평가할 간격을 분으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-227">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="2e893-228">`[ChangeStep <Double?>]`: 자동 램프 시나리오에서는 \n 또는 에 도달할 때까지 추가/제거하는 <code>ReroutePercentage</code> <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-228">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="2e893-229">사이트 메트릭은 .\nCustom 의사 결정 알고리즘에 지정된 N분마다 확인되어 TiPCallback 사이트 확장에서 URL을 지정할 수 <code>ChangeIntervalInMinutes</code> <code>ChangeDecisionCallbackUrl</code> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-229">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="2e893-230">`[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지될 아래 상한 경계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-230">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="2e893-231">`[MinReroutePercentage <Double?>]`: ReroutePercentage가 유지될 아래쪽 경계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-231">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="2e893-232">`[Name <String>]`: 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-232">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="2e893-233">권장되는 이름은 실험에서 트래픽을 수신할 슬롯을 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-233">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="2e893-234">`[ReroutePercentage <Double?>]`: 리디렉션될 트래픽의 백분율입니다. <code>ActionHostName</code></span><span class="sxs-lookup"><span data-stu-id="2e893-234">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="2e893-235">`[FtpsState <FtpsState?>]`: FTP/FTPS 서비스 상태</span><span class="sxs-lookup"><span data-stu-id="2e893-235">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="2e893-236">`[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-236">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="2e893-237">`[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-237">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="2e893-238">`[Extension <String>]`: 이 확장이 있는 요청은 지정된 FastCGI 애플리케이션을 사용하여 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-238">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="2e893-239">`[ScriptProcessor <String>]`: FastCGI 애플리케이션에 대한 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-239">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="2e893-240">`[HealthCheckPath <String>]`: 상태 검사 경로</span><span class="sxs-lookup"><span data-stu-id="2e893-240">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="2e893-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http2.0을 통해 연결할 수 있도록 웹 사이트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-241">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="2e893-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-242">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: 기본에 대한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-243">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="2e893-244">`[Action <String>]`: 이 IP 범위에 대한 액세스를 허용하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-244">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="2e893-245">`[Description <String>]`: IP 제한 규칙 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-245">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="2e893-246">`[IPAddress <String>]`: IP 주소 보안 제한이 유효한 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-246">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="2e893-247">순수 ipv4 주소(필수 SubnetMask 속성) 또는 ipv4/mask(선행 비트 일치)와 같은 CIDR 문구의 형식일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-247">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="2e893-248">CIDR의 경우 SubnetMask 속성을 지정하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-248">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="2e893-249">`[Name <String>]`: IP 제한 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-249">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="2e893-250">`[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-250">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="2e893-251">`[SubnetMask <String>]`: IP 주소 범위에 대한 서브넷 마스크 제한이 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-251">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="2e893-252">`[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="2e893-252">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="2e893-253">`[Tag <IPFilterTag?>]`: 이 IP 필터를 사용할 것을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-253">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="2e893-254">이는 Proxies에서 IP 필터링을 지원하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-254">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="2e893-255">`[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="2e893-255">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="2e893-256">`[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="2e893-256">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="2e893-257">`[JavaContainer <String>]`: Java 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-257">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="2e893-258">`[JavaContainerVersion <String>]`: Java 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-258">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="2e893-259">`[JavaVersion <String>]`: Java 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-259">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="2e893-260">`[LimitMaxDiskSizeInMb <Int64?>]`: 허용되는 최대 디스크 크기 사용량(MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-260">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="2e893-261">`[LimitMaxMemoryInMb <Int64?>]`: 최대 허용되는 메모리 사용량(MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-261">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="2e893-262">`[LimitMaxPercentageCpu <Double?>]`: 허용되는 최대 CPU 사용량 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-262">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="2e893-263">`[LinuxFxVersion <String>]`: Linux App Framework 및 버전</span><span class="sxs-lookup"><span data-stu-id="2e893-263">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="2e893-264">`[LoadBalancing <SiteLoadBalancing?>]`: 사이트 부하 분산.</span><span class="sxs-lookup"><span data-stu-id="2e893-264">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="2e893-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-265">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-266">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="2e893-267">`[MachineKeyDecryption <String>]`: 암호 해독에 사용되는 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-267">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="2e893-268">`[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-268">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="2e893-269">`[MachineKeyValidation <String>]`: MachineKey 유효성 검사.</span><span class="sxs-lookup"><span data-stu-id="2e893-269">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="2e893-270">`[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-270">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="2e893-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리되는 파이프라인 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-271">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="2e893-272">`[ManagedServiceIdentityId <Int32?>]`: 관리 서비스 ID ID</span><span class="sxs-lookup"><span data-stu-id="2e893-272">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="2e893-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 TLS의 최소 버전을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-273">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="2e893-274">`[NetFrameworkVersion <String>]`: .NET Framework 버전.</span><span class="sxs-lookup"><span data-stu-id="2e893-274">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="2e893-275">`[NodeVersion <String>]`: Node.js.</span><span class="sxs-lookup"><span data-stu-id="2e893-275">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="2e893-276">`[NumberOfWorker <Int32?>]`: 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-276">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="2e893-277">`[PhpVersion <String>]`: PHP 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-277">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="2e893-278">`[PowerShellVersion <String>]`: PowerShell 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-278">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="2e893-279">`[PreWarmedInstanceCount <Int32?>]`: 미리 준비된 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-279">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="2e893-280">이 설정은 소비 및 탄력적 계획에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-280">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="2e893-281">`[PublishingUsername <String>]`: 사용자 이름을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-281">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="2e893-282">`[PushKind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-282">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="2e893-283">`[PythonVersion <String>]`: Python 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-283">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="2e893-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-284">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-285">`[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-285">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="2e893-286">`[RequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="2e893-286">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="2e893-287">`[RequestTimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-287">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="2e893-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-288">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-289">`[RequestTracingExpirationTime <DateTime?>]`: 요청 추적 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-289">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="2e893-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: SCM에 대한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-290">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="2e893-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: scm이 main을 사용하기 위한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-291">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="2e893-292">`[ScmType <ScmType?>]`: SCM 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-292">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="2e893-293">`[SlowRequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="2e893-293">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="2e893-294">`[SlowRequestTimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-294">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="2e893-295">`[SlowRequestTimeTaken <String>]`: 시간이 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-295">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="2e893-296">`[TagWhitelistJson <String>]`: 푸시 등록 엔드포인트에서 사용할 수 있는 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-296">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="2e893-297">`[TagsRequiringAuth <String>]`: 푸시 등록 엔드포인트에서 사용자 인증을 필요로 하는 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-297">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="2e893-298">태그는 영문자 문자와 '_', '@', '#', '.', ':', '-'로 구성될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-298">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="2e893-299">PushRequestHandler에서 유효성 검사를 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-299">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="2e893-300">`[TracingOption <String>]`: 추적 옵션.</span><span class="sxs-lookup"><span data-stu-id="2e893-300">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="2e893-301">`[TriggerPrivateBytesInKb <Int32?>]`: 개인 Bytes를 기반으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-301">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="2e893-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기반으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-302">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="2e893-303">`[Count <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="2e893-303">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="2e893-304">`[Status <Int32?>]`: HTTP 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-304">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="2e893-305">`[SubStatus <Int32?>]`: 요청 하위 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-305">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="2e893-306">`[TimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-306">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="2e893-307">`[Win32Status <Int32?>]`: Win32 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-307">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="2e893-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32비트 Worker 프로세스를 사용하는 경우. 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-308">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-309">`[VirtualApplication <IVirtualApplication[]>]`: 가상 애플리케이션.</span><span class="sxs-lookup"><span data-stu-id="2e893-309">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="2e893-310">`[PhysicalPath <String>]`: 물리적 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-310">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="2e893-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-311">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="2e893-312">`[VirtualDirectory <IVirtualDirectory[]>]`: 가상 애플리케이션에 대한 가상디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-312">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="2e893-313">`[PhysicalPath <String>]`: 물리적 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-313">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="2e893-314">`[VirtualPath <String>]`: 가상 애플리케이션에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-314">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="2e893-315">`[VirtualPath <String>]`: 가상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-315">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="2e893-316">`[VnetName <String>]`: Virtual Network 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-316">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="2e893-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-317">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="2e893-318">`[WindowsFxVersion <String>]`: Xenon App Framework 및 버전</span><span class="sxs-lookup"><span data-stu-id="2e893-318">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="2e893-319">`[XManagedServiceIdentityId <Int32?>]`: 명시적 관리 서비스 ID ID</span><span class="sxs-lookup"><span data-stu-id="2e893-319">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="2e893-320">`[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-320">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="2e893-321">`[DailyMemoryTimeQuota <Int32?>]`: 허용되는 최대 일일 메모리 시간 할당량(동적 앱에만 해당)</span><span class="sxs-lookup"><span data-stu-id="2e893-321">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="2e893-322">`[Enabled <Boolean?>]`: <code>true</code> 앱이 활성화되어 있는 경우, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-322">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="2e893-323">이 값을 false로 설정하면 앱이 비활성화됩니다(앱을 오프라인으로 전환).</span><span class="sxs-lookup"><span data-stu-id="2e893-323">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="2e893-324">`[HostNameSslState <IHostNameSslState[]>]`: 호스트 이름 SSL 상태는 앱의 호스트 이름에 대한 SSL 바인딩을 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-324">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="2e893-325">`[HostType <HostType?>]`: 호스트 이름의 표준 또는 리포지토리 호스트 이름인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-325">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="2e893-326">`[Name <String>]`: 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-326">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="2e893-327">`[SslState <SslState?>]`: SSL 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-327">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="2e893-328">`[Thumbprint <String>]`: SSL 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-328">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="2e893-329">`[ToUpdate <Boolean?>]`: 기존 호스트 <code>true</code> 이름을 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-329">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="2e893-330">`[VirtualIP <String>]`: IP 기반 SSL을 사용하는 경우 호스트 이름에 할당된 가상 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-330">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="2e893-331">`[HostNamesDisabled <Boolean?>]`: 앱의 공용 호스트 이름을 사용하지 않도록 설정하는 <code>true</code> 것입니다. 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-331">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="2e893-332">이 경우 앱은 API 관리 <code>true</code> 프로세스를 통해서만 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-332">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="2e893-333">`[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-333">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="2e893-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: https 요청만 수락하도록 웹 사이트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-334">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="2e893-335">http 요청에 대한 문제 리디렉션</span><span class="sxs-lookup"><span data-stu-id="2e893-335">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="2e893-336">`[HyperV <Boolean?>]`: Hyper-V 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="2e893-336">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="2e893-337">`[IdentityType <ManagedServiceIdentityType?>]`: 관리 서비스 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-337">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="2e893-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결된 사용자 할당 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-338">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="2e893-339">사용자 ARM ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-339">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="2e893-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: 이 개체에 추가할 수 있는 속성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-340">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="2e893-341">`[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="2e893-341">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="2e893-342">`[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드</span><span class="sxs-lookup"><span data-stu-id="2e893-342">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="2e893-343">`[Reserved <Boolean?>]`: <code>true</code> 예약된 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-343">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-344">`[ScmSiteAlsoStopped <Boolean?>]`: 앱이 중지된 경우 <code>true</code> SCM(KUDU) 사이트를 중지합니다. 그렇지 않으면 <code>false</code></span><span class="sxs-lookup"><span data-stu-id="2e893-344">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="2e893-345">기본값은 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="2e893-345">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="2e893-346">`[ServerFarmId <String>]`: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"으로 형식이 지정되는 연결된 App Service 계획의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2e893-346">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="2e893-347">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e893-347">RELATED LINKS</span></span>

