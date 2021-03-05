---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/powershell/module/az.functions/start-azfunctionapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Start-AzFunctionApp.md
ms.openlocfilehash: 629cad3d54c575eb9f68dfbef43f1cbdd0502c84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972027"
---
# <span data-ttu-id="5211e-101">Start-AzFunctionApp</span><span class="sxs-lookup"><span data-stu-id="5211e-101">Start-AzFunctionApp</span></span>

## <span data-ttu-id="5211e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5211e-102">SYNOPSIS</span></span>
<span data-ttu-id="5211e-103">함수 앱을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-103">Starts a function app.</span></span>

## <span data-ttu-id="5211e-104">구문</span><span class="sxs-lookup"><span data-stu-id="5211e-104">SYNTAX</span></span>

### <span data-ttu-id="5211e-105">StartByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="5211e-105">StartByName (Default)</span></span>
```
Start-AzFunctionApp -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5211e-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="5211e-106">ByObjectInput</span></span>
```
Start-AzFunctionApp -InputObject <ISite> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="5211e-107">설명</span><span class="sxs-lookup"><span data-stu-id="5211e-107">DESCRIPTION</span></span>
<span data-ttu-id="5211e-108">함수 앱을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-108">Starts a function app.</span></span>

## <span data-ttu-id="5211e-109">예제</span><span class="sxs-lookup"><span data-stu-id="5211e-109">EXAMPLES</span></span>

### <span data-ttu-id="5211e-110">예제 1: 함수 앱을 이름으로 다운로드하고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-110">Example 1: Get a function app by name and start it.</span></span>
```powershell
PS C:\> Get-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName | Start-AzFunctionApp
```

<span data-ttu-id="5211e-111">이 명령은 함수 앱을 이름으로 얻게 하여 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-111">This command gets a function app by name and starts it.</span></span>

### <span data-ttu-id="5211e-112">예제 2: 이름에 의해 함수 앱을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-112">Example 2: Start a function app by name.</span></span>
```powershell
PS C:\> Start-AzFunctionApp -Name MyAppName -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="5211e-113">이 명령은 함수 앱을 이름으로 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-113">This command starts a function app by name.</span></span>

## <span data-ttu-id="5211e-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5211e-114">PARAMETERS</span></span>

### <span data-ttu-id="5211e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5211e-115">-DefaultProfile</span></span>
<span data-ttu-id="5211e-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5211e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5211e-117">-InputObject</span></span>
<span data-ttu-id="5211e-118">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5211e-118">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5211e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5211e-119">-Name</span></span>
<span data-ttu-id="5211e-120">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-120">The name of function app.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5211e-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5211e-121">-PassThru</span></span>
<span data-ttu-id="5211e-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-122">Returns true when the command succeeds.</span></span>

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

### <span data-ttu-id="5211e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5211e-123">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5211e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5211e-124">-SubscriptionId</span></span>
<span data-ttu-id="5211e-125">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-125">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: StartByName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5211e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="5211e-126">-Confirm</span></span>
<span data-ttu-id="5211e-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5211e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5211e-128">-WhatIf</span></span>
<span data-ttu-id="5211e-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5211e-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5211e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5211e-131">CommonParameters</span></span>
<span data-ttu-id="5211e-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5211e-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5211e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5211e-134">입력</span><span class="sxs-lookup"><span data-stu-id="5211e-134">INPUTS</span></span>

### <span data-ttu-id="5211e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span><span class="sxs-lookup"><span data-stu-id="5211e-135">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="5211e-136">출력</span><span class="sxs-lookup"><span data-stu-id="5211e-136">OUTPUTS</span></span>

### <span data-ttu-id="5211e-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5211e-137">System.Boolean</span></span>

## <span data-ttu-id="5211e-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5211e-138">NOTES</span></span>

<span data-ttu-id="5211e-139">별칭</span><span class="sxs-lookup"><span data-stu-id="5211e-139">ALIASES</span></span>

<span data-ttu-id="5211e-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5211e-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5211e-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5211e-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5211e-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5211e-143">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="5211e-143">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="5211e-144">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-144">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="5211e-145">`CloningInfoSourceWebAppId <String>`: ARM 앱의 리소스 ID를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-145">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="5211e-146">앱 리소스 ID는 프로덕션 슬롯 및 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}의 폼/subscriptions/{subId}/resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-146">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="5211e-147">`[Kind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-147">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="5211e-148">`[Tag <IResourceTags>]`: 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-148">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="5211e-149">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-149">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5211e-150">`[ClientAffinityEnabled <Boolean?>]`: 클라이언트 연결성을 사용하도록 설정하려면 세션 연결 쿠키를 보내지 못하도록 하여 동일한 세션에서 클라이언트 요청을 동일한 인스턴스로 <code>true</code> <code>false</code> 라우팅합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-150">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="5211e-151">기본값은 <code>true</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-151">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="5211e-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증(TLS 상호 인증)을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-152">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="5211e-153">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-153">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-154">`[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 콤마로 구분된 제외 경로</span><span class="sxs-lookup"><span data-stu-id="5211e-154">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="5211e-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제된 앱에 대한 애플리케이션 설정이재정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-155">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="5211e-156">지정한 경우 이러한 설정은 원본 앱에서 복제된 설정을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-156">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="5211e-157">그렇지 않으면 원본 앱에서 애플리케이션 설정이 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-157">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="5211e-158">`[(Any) <String>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-158">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5211e-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: 원본 앱에서 사용자 지정 호스트 이름을 <code>true</code> 복제합니다. 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-159">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-160">`[CloningInfoCloneSourceControl <Boolean?>]`: 원본 앱에서 원본 제어를 <code>true</code> 복제합니다. 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-160">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: 원본 및 대상 앱에 대한 부하 <code>true</code> 분산을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-161">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="5211e-162">`[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-162">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="5211e-163">이 ID는 동일한 스냅숏을 사용하기 위해 여러 복제 작업을 함께 연계합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-163">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="5211e-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span><span class="sxs-lookup"><span data-stu-id="5211e-164">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="5211e-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어 덮어 던지기 위해, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-165">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-166">`[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서부 또는 북유럽</span><span class="sxs-lookup"><span data-stu-id="5211e-166">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="5211e-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM 있는 경우 사용할 Traffic Manager 프로필의 리소스 ID를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-167">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="5211e-168">Traffic Manager 리소스 ID는 양식 /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-168">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="5211e-169">`[CloningInfoTrafficManagerProfileName <String>]`: 만들 Traffic Manager 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-169">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="5211e-170">Traffic Manager 프로필이 아직 없는 경우만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-170">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="5211e-171">`[Config <ISiteConfig>]`: 앱의 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-171">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="5211e-172">`IsPushEnabled <Boolean>`: 푸시 엔드포인트를 사용하도록 설정하는지 여부를 나타내는 플래그를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-172">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="5211e-173">`[ActionMinProcessExecutionTime <String>]`: 작업을 수행하기 전에 프로세스가 실행되어야 하는 최소 시간</span><span class="sxs-lookup"><span data-stu-id="5211e-173">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="5211e-174">`[ActionType <AutoHealActionType?>]`: 수행될 미리 정의된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-174">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="5211e-175">`[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-175">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-176">`[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-176">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="5211e-177">`[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-177">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="5211e-178">`[AppCommandLine <String>]`: 시작할 앱 명령줄입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-178">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="5211e-179">`[AppSetting <INameValuePair[]>]`: 애플리케이션 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-179">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="5211e-180">`[Name <String>]`: 쌍 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-180">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="5211e-181">`[Value <String>]`: 쌍 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-181">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="5211e-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> 자동 고치기(Auto Heal)를 사용하도록 설정되어 있는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-182">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-183">`[AutoSwapSlotName <String>]`: 슬롯 이름을 자동 교환합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-183">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="5211e-184">`[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-184">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="5211e-185">`[ConnectionString <String>]`: 연결 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-185">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="5211e-186">`[Name <String>]`: 연결 문자열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-186">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="5211e-187">`[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-187">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="5211e-188">`[CorAllowedOrigin <String[]>]`: 원본 간 호출을 허용해야 하는 원본 목록을 얻거나 설정합니다(예: http://example.com:12345) ).</span><span class="sxs-lookup"><span data-stu-id="5211e-188">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="5211e-189">"\*"를 사용하여 모두를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-189">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="5211e-190">`[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용하여 CORS 요청을 허용할지 여부를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-190">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="5211e-191">자세한         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         내용은 를 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-191">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="5211e-192">`[CustomActionExe <String>]`: 실행할 실행 가능.</span><span class="sxs-lookup"><span data-stu-id="5211e-192">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="5211e-193">`[CustomActionParameter <String>]`: 실행 가능한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-193">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="5211e-194">`[DefaultDocument <String[]>]`: 기본 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-194">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="5211e-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-195">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-196">`[DocumentRoot <String>]`: 문서 루트입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-196">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="5211e-197">`[DynamicTagsJson <String>]`: 푸시 등록 엔드포인트의 사용자 클레임에서 평가될 동적 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-197">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="5211e-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: 램프업 규칙 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-198">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="5211e-199">`[ActionHostName <String>]`: 결정된 경우 트래픽이 리디렉션되는 슬롯의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-199">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="5211e-200">예:</span><span class="sxs-lookup"><span data-stu-id="5211e-200">E.g.</span></span> <span data-ttu-id="5211e-201">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="5211e-201">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="5211e-202">`[ChangeDecisionCallbackUrl <String>]`: URL을 지정할 수 있는 TiPCallback 사이트 확장에 사용자 지정 의사 결정 알고리즘을 제공 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-202">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="5211e-203">스캐폴드 및 계약에 대한 TiPCallback 사이트 확장을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5211e-203">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="5211e-204"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="5211e-204">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="5211e-205">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 평가하기 위해 분 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-205">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="5211e-206">`[ChangeStep <Double?>]`: 자동 램프 업 시나리오에서는 \n 또는 에 도달할 때까지 추가/제거하는 <code>ReroutePercentage</code> <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> 단계입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-206">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="5211e-207">사이트 메트릭은 .\nCustom 의사 결정 알고리즘에 지정된 N 분마다 검사되어 에서 URL을 지정할 수 있는 TiPCallback 사이트 확장에 제공될 <code>ChangeIntervalInMinutes</code> 수 <code>ChangeDecisionCallbackUrl</code> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-207">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="5211e-208">`[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지될 위쪽 경계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-208">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="5211e-209">`[MinReroutePercentage <Double?>]`: ReroutePercentage가 유지될 위의 하위 경계를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-209">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="5211e-210">`[Name <String>]`: 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-210">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="5211e-211">권장되는 이름은 실험에서 트래픽을 수신할 슬롯을 지정하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-211">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="5211e-212">`[ReroutePercentage <Double?>]`: 로 리디렉션될 트래픽의 <code>ActionHostName</code> 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-212">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="5211e-213">`[FtpsState <FtpsState?>]`: FTP/FTPS 서비스 상태</span><span class="sxs-lookup"><span data-stu-id="5211e-213">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="5211e-214">`[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑.</span><span class="sxs-lookup"><span data-stu-id="5211e-214">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="5211e-215">`[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-215">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="5211e-216">`[Extension <String>]`: 이 확장을 사용하는 요청은 지정된 FastCGI 애플리케이션을 사용하여 처리됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-216">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="5211e-217">`[ScriptProcessor <String>]`: FastCGI 애플리케이션에 대한 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-217">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="5211e-218">`[HealthCheckPath <String>]`: 상태 확인 경로</span><span class="sxs-lookup"><span data-stu-id="5211e-218">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="5211e-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http2.0을 통해 연결할 수 있도록 웹 사이트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-219">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="5211e-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-220">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: main에 대한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-221">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="5211e-222">`[Action <String>]`: 이 IP 범위에 대한 액세스를 허용하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-222">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="5211e-223">`[Description <String>]`: IP 제한 규칙 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-223">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="5211e-224">`[IPAddress <String>]`: IP 주소 보안 제한이 유효한 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-224">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="5211e-225">순수한 ipv4 주소(필수 SubnetMask 속성) 또는 ipv4/mask(선행 비트 일치)와 같은 CIDR 어코드의 형태로 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-225">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="5211e-226">CIDR의 경우 SubnetMask 속성을 지정하지 말아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-226">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="5211e-227">`[Name <String>]`: IP 제한 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-227">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="5211e-228">`[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-228">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="5211e-229">`[SubnetMask <String>]`: IP 주소 범위에 대한 서브넷 마스크는 제한이 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-229">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="5211e-230">`[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="5211e-230">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="5211e-231">`[Tag <IPFilterTag?>]`: 이 IP 필터를 사용할 것을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-231">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="5211e-232">이는 proxies에서 IP 필터링을 지원하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-232">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="5211e-233">`[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="5211e-233">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="5211e-234">`[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="5211e-234">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="5211e-235">`[JavaContainer <String>]`: Java 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-235">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="5211e-236">`[JavaContainerVersion <String>]`: Java 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-236">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="5211e-237">`[JavaVersion <String>]`: Java 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-237">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="5211e-238">`[LimitMaxDiskSizeInMb <Int64?>]`: MB에서 허용되는 최대 디스크 크기 사용량입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-238">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="5211e-239">`[LimitMaxMemoryInMb <Int64?>]`: MB에서 허용되는 최대 메모리 사용량입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-239">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="5211e-240">`[LimitMaxPercentageCpu <Double?>]`: 허용되는 최대 CPU 사용량 비율입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-240">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="5211e-241">`[LinuxFxVersion <String>]`: Linux App Framework 및 버전</span><span class="sxs-lookup"><span data-stu-id="5211e-241">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="5211e-242">`[LoadBalancing <SiteLoadBalancing?>]`: 사이트 부하 분산.</span><span class="sxs-lookup"><span data-stu-id="5211e-242">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="5211e-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용하도록 설정하려면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-243">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한.</span><span class="sxs-lookup"><span data-stu-id="5211e-244">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="5211e-245">`[MachineKeyDecryption <String>]`: 암호 해독에 사용되는 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-245">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="5211e-246">`[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-246">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="5211e-247">`[MachineKeyValidation <String>]`: MachineKey 유효성 검사.</span><span class="sxs-lookup"><span data-stu-id="5211e-247">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="5211e-248">`[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-248">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="5211e-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리되는 파이프라인 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-249">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="5211e-250">`[ManagedServiceIdentityId <Int32?>]`: 관리되는 서비스 ID ID</span><span class="sxs-lookup"><span data-stu-id="5211e-250">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="5211e-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 최소 버전의 TLS를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-251">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="5211e-252">`[NetFrameworkVersion <String>]`: .NET Framework 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-252">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="5211e-253">`[NodeVersion <String>]`: Node.js.</span><span class="sxs-lookup"><span data-stu-id="5211e-253">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="5211e-254">`[NumberOfWorker <Int32?>]`: 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-254">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="5211e-255">`[PhpVersion <String>]`: PHP 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-255">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="5211e-256">`[PowerShellVersion <String>]`: PowerShell 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-256">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="5211e-257">`[PreWarmedInstanceCount <Int32?>]`: 미리 준비된 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-257">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="5211e-258">이 설정은 소비 및 탄력적 계획에만 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-258">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="5211e-259">`[PublishingUsername <String>]`: 사용자 이름을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-259">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="5211e-260">`[PushKind <String>]`: 리소스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-260">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="5211e-261">`[PythonVersion <String>]`: Python 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-261">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="5211e-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용하도록 설정되어 있는 경우, 그렇지 않으면 을(를) 사용할 수 <code>false</code> 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-262">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-263">`[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-263">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="5211e-264">`[RequestCount <Int32?>]`: 요청 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-264">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="5211e-265">`[RequestTimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-265">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="5211e-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용하도록 설정되어 있는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-266">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-267">`[RequestTracingExpirationTime <DateTime?>]`: 요청 추적 만료 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-267">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="5211e-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: scm에 대한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-268">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="5211e-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: main를 사용할 scm에 대한 IP 보안 제한 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-269">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="5211e-270">`[ScmType <ScmType?>]`: SCM 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-270">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="5211e-271">`[SlowRequestCount <Int32?>]`: 요청 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-271">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="5211e-272">`[SlowRequestTimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-272">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="5211e-273">`[SlowRequestTimeTaken <String>]`: 시간이 찍은 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-273">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="5211e-274">`[TagWhitelistJson <String>]`: 푸시 등록 엔드포인트에서 사용할 수 있는 태그 목록이 포함된 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-274">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="5211e-275">`[TagsRequiringAuth <String>]`: 푸시 등록 엔드포인트에서 사용자 인증을 필요로 하는 태그 목록을 포함하는 JSON 문자열을 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-275">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="5211e-276">태그는 영수 문자와 '_', '@', '#', '.', '.', ':', '-'로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-276">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="5211e-277">유효성 검사는 PushRequestHandler에서 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-277">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="5211e-278">`[TracingOption <String>]`: 추적 옵션.</span><span class="sxs-lookup"><span data-stu-id="5211e-278">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="5211e-279">`[TriggerPrivateBytesInKb <Int32?>]`: 개인 bytes를 기반으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-279">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="5211e-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기반으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-280">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="5211e-281">`[Count <Int32?>]`: 요청 수입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-281">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="5211e-282">`[Status <Int32?>]`: HTTP 상태 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-282">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="5211e-283">`[SubStatus <Int32?>]`: 하위 상태를 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-283">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="5211e-284">`[TimeInterval <String>]`: 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-284">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="5211e-285">`[Win32Status <Int32?>]`: Win32 오류 코드입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-285">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="5211e-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32비트 작업 프로세스, 그렇지 않으면 <code>false</code> 을 사용</span><span class="sxs-lookup"><span data-stu-id="5211e-286">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-287">`[VirtualApplication <IVirtualApplication[]>]`: 가상 애플리케이션.</span><span class="sxs-lookup"><span data-stu-id="5211e-287">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="5211e-288">`[PhysicalPath <String>]`: 물리적 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-288">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="5211e-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용하도록 설정되어 있는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-289">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="5211e-290">`[VirtualDirectory <IVirtualDirectory[]>]`: 가상 애플리케이션에 대한 가상 감독입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-290">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="5211e-291">`[PhysicalPath <String>]`: 물리적 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-291">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="5211e-292">`[VirtualPath <String>]`: 가상 애플리케이션에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-292">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="5211e-293">`[VirtualPath <String>]`: 가상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-293">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="5211e-294">`[VnetName <String>]`: 가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-294">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="5211e-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-295">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="5211e-296">`[WindowsFxVersion <String>]`: Xenon App Framework 및 버전</span><span class="sxs-lookup"><span data-stu-id="5211e-296">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="5211e-297">`[XManagedServiceIdentityId <Int32?>]`: 명시적 관리 서비스 ID</span><span class="sxs-lookup"><span data-stu-id="5211e-297">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="5211e-298">`[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-298">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="5211e-299">`[DailyMemoryTimeQuota <Int32?>]`: 허용되는 최대 일일 메모리 시간 할당량(동적 앱에만 해당)</span><span class="sxs-lookup"><span data-stu-id="5211e-299">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="5211e-300">`[Enabled <Boolean?>]`: <code>true</code> 앱이 활성화되어 있는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-300">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="5211e-301">이 값을 false로 설정하면 앱이 비활성화됩니다(앱을 오프라인으로 전환).</span><span class="sxs-lookup"><span data-stu-id="5211e-301">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="5211e-302">`[HostNameSslState <IHostNameSslState[]>]`: 호스트 이름 SSL 상태는 앱의 호스트 이름에 대한 SSL 바인딩을 관리하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-302">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="5211e-303">`[HostType <HostType?>]`: 호스트 이름이 표준인지 리포지토리 호스트 이름인지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-303">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="5211e-304">`[Name <String>]`: 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-304">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="5211e-305">`[SslState <SslState?>]`: SSL 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-305">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="5211e-306">`[Thumbprint <String>]`: SSL 인증서 지문입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-306">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="5211e-307">`[ToUpdate <Boolean?>]`: 기존 호스트 <code>true</code> 이름을 업데이트로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-307">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="5211e-308">`[VirtualIP <String>]`: IP 기반 SSL을 사용하도록 설정한 경우 호스트 이름에 할당된 가상 IP 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-308">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="5211e-309">`[HostNamesDisabled <Boolean?>]`: 앱의 공용 호스트 이름을 사용하지 않도록 <code>true</code> 설정하는 경우, 그렇지 않으면 을 사용하지 않도록 <code>false</code> 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-309">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="5211e-310">의 경우 API 관리 프로세스를 <code>true</code> 통해서만 앱에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-310">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="5211e-311">`[HostingEnvironmentProfileId <String>]`: App Service Environment의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-311">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="5211e-312">`[HttpsOnly <Boolean?>]`: httpsOnly: https 요청만 수락하도록 웹 사이트를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-312">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="5211e-313">http 요청에 대한 문제 리디렉션</span><span class="sxs-lookup"><span data-stu-id="5211e-313">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="5211e-314">`[HyperV <Boolean?>]`: Hyper-V 샌드박스입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-314">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="5211e-315">`[IdentityType <ManagedServiceIdentityType?>]`: 관리되는 서비스 ID 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-315">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="5211e-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결된 사용자 할당 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-316">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="5211e-317">사용자 ARM ID 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} 형식의 리소스 ID로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-317">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="5211e-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: 이 개체에 속성을 추가할 수 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-318">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="5211e-319">`[IsXenon <Boolean?>]`: 사용되지 않습니다. Hyper-V 샌드박스입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-319">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="5211e-320">`[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드</span><span class="sxs-lookup"><span data-stu-id="5211e-320">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="5211e-321">`[Reserved <Boolean?>]`: <code>true</code> 예약된 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-321">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-322">`[ScmSiteAlsoStopped <Boolean?>]`: 앱이 중지된 경우 <code>true</code> SCM(KUDU) 사이트를 중지합니다. 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="5211e-322">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="5211e-323">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-323">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="5211e-324">`[ServerFarmId <String>]`: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}"으로 서식이 지정된 연결된 App Service 계획의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5211e-324">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="5211e-325">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5211e-325">RELATED LINKS</span></span>

