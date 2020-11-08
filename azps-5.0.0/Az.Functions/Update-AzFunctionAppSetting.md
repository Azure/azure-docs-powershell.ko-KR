---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/update-azfunctionappsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/Update-AzFunctionAppSetting.md
ms.openlocfilehash: 4255940b9cf17420fe0b522d81c6a974e9cf9324
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215403"
---
# <span data-ttu-id="20ceb-101">Update-AzFunctionAppSetting</span><span class="sxs-lookup"><span data-stu-id="20ceb-101">Update-AzFunctionAppSetting</span></span>

## <span data-ttu-id="20ceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20ceb-102">SYNOPSIS</span></span>
<span data-ttu-id="20ceb-103">함수 앱에서 앱 설정을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-103">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="20ceb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20ceb-104">SYNTAX</span></span>

### <span data-ttu-id="20ceb-105">ByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="20ceb-105">ByName (Default)</span></span>
```
Update-AzFunctionAppSetting -Name <String> -ResourceGroupName <String> -AppSetting <Hashtable>
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="20ceb-106">ByObjectInput</span><span class="sxs-lookup"><span data-stu-id="20ceb-106">ByObjectInput</span></span>
```
Update-AzFunctionAppSetting -AppSetting <Hashtable> -InputObject <ISite> [-Force] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20ceb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="20ceb-107">DESCRIPTION</span></span>
<span data-ttu-id="20ceb-108">함수 앱에서 앱 설정을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-108">Adds or updates app settings in a function app.</span></span>

## <span data-ttu-id="20ceb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="20ceb-109">EXAMPLES</span></span>

### <span data-ttu-id="20ceb-110">예제 1: 함수 앱에 새 앱 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-110">Example 1: Add a new app setting in a function app.</span></span>
```powershell
PS C:\> Update-AzFunctionAppSetting -Name MyAppName -ResourceGroupName MyResourceGroupName -AppSetting @{"Name1" = "Value1"}
```

<span data-ttu-id="20ceb-111">이 명령은 함수 앱에 새 앱 설정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-111">This command adds a new app setting in a function app.</span></span>

## <span data-ttu-id="20ceb-112">변수</span><span class="sxs-lookup"><span data-stu-id="20ceb-112">PARAMETERS</span></span>

### <span data-ttu-id="20ceb-113">-AppSetting</span><span class="sxs-lookup"><span data-stu-id="20ceb-113">-AppSetting</span></span>
<span data-ttu-id="20ceb-114">키 및 값이 있는 해시 테이블은 함수 앱에서 추가 하거나 업데이트할 앱 설정을 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-114">Hashtable with keys and values describe the app settings to be added or updated in the function app.</span></span>
<span data-ttu-id="20ceb-115">예: @ {"myappsetting" = "123"}</span><span class="sxs-lookup"><span data-stu-id="20ceb-115">For example: @{"myappsetting"="123"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20ceb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20ceb-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="20ceb-117">-Force</span><span class="sxs-lookup"><span data-stu-id="20ceb-117">-Force</span></span>
<span data-ttu-id="20ceb-118">확인 메시지 없이 cmdlet에서 함수 앱 설정을 업데이트 하도록 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-118">Forces the cmdlet to update function app setting without prompting for confirmation.</span></span>

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

### <span data-ttu-id="20ceb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20ceb-119">-InputObject</span></span>
<span data-ttu-id="20ceb-120">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-120">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20ceb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="20ceb-121">-Name</span></span>
<span data-ttu-id="20ceb-122">함수 앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-122">Name of the function app.</span></span>

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

### <span data-ttu-id="20ceb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20ceb-123">-ResourceGroupName</span></span>
<span data-ttu-id="20ceb-124">자원이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-124">Name of the resource group to which the resource belongs.</span></span>

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

### <span data-ttu-id="20ceb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20ceb-125">-SubscriptionId</span></span>
<span data-ttu-id="20ceb-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-126">The Azure subscription ID.</span></span>

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

### <span data-ttu-id="20ceb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="20ceb-127">-Confirm</span></span>
<span data-ttu-id="20ceb-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20ceb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20ceb-129">-WhatIf</span></span>
<span data-ttu-id="20ceb-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20ceb-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20ceb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20ceb-132">CommonParameters</span></span>
<span data-ttu-id="20ceb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20ceb-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ceb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20ceb-135">입력</span><span class="sxs-lookup"><span data-stu-id="20ceb-135">INPUTS</span></span>

### <span data-ttu-id="20ceb-136">Api20190801. ISite의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="20ceb-136">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.ISite</span></span>

## <span data-ttu-id="20ceb-137">출력</span><span class="sxs-lookup"><span data-stu-id="20ceb-137">OUTPUTS</span></span>

### <span data-ttu-id="20ceb-138">Api20190801. IStringDictionary의. PowerShell for.</span><span class="sxs-lookup"><span data-stu-id="20ceb-138">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IStringDictionary</span></span>

## <span data-ttu-id="20ceb-139">상속자</span><span class="sxs-lookup"><span data-stu-id="20ceb-139">NOTES</span></span>

<span data-ttu-id="20ceb-140">별칭과</span><span class="sxs-lookup"><span data-stu-id="20ceb-140">ALIASES</span></span>

<span data-ttu-id="20ceb-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="20ceb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20ceb-142">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20ceb-143">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ceb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20ceb-144">INPUTOBJECT <ISite> :</span><span class="sxs-lookup"><span data-stu-id="20ceb-144">INPUTOBJECT <ISite>:</span></span> 
  - <span data-ttu-id="20ceb-145">`Location <String>`: 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-145">`Location <String>`: Resource Location.</span></span>
  - <span data-ttu-id="20ceb-146">`CloningInfoSourceWebAppId <String>`: ARM 원본 앱의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-146">`CloningInfoSourceWebAppId <String>`: ARM resource ID of the source app.</span></span> <span data-ttu-id="20ceb-147">앱 리소스 ID는 프로덕션 슬롯 및 다른 슬롯의/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName}에 대 한/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-147">App resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName} for production slots and         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Web/sites/{siteName}/slots/{slotName} for other slots.</span></span>
  - <span data-ttu-id="20ceb-148">`[Kind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-148">`[Kind <String>]`: Kind of resource.</span></span>
  - <span data-ttu-id="20ceb-149">`[Tag <IResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="20ceb-149">`[Tag <IResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="20ceb-150">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-150">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="20ceb-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> <code>false</code> 동일한 세션에서 클라이언트 요청을 동일한 인스턴스로 라우팅하기 위해 클라이언트 선호도를 사용 하도록 설정 하 고 세션 선호도 쿠키 보내기를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-151">`[ClientAffinityEnabled <Boolean?>]`: <code>true</code> to enable client affinity; <code>false</code> to stop sending session affinity cookies, which route client requests in the same session to the same instance.</span></span> <span data-ttu-id="20ceb-152">기본값은 <code>true</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-152">Default is <code>true</code>.</span></span>
  - <span data-ttu-id="20ceb-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> 클라이언트 인증서 인증 (TLS 상호 인증)을 사용 하도록 설정 하는 방법, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-153">`[ClientCertEnabled <Boolean?>]`: <code>true</code> to enable client certificate authentication (TLS mutual authentication); otherwise, <code>false</code>.</span></span> <span data-ttu-id="20ceb-154">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-154">Default is <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-155">`[ClientCertExclusionPath <String>]`: 클라이언트 인증서 인증 쉼표로 구분 된 제외 경로</span><span class="sxs-lookup"><span data-stu-id="20ceb-155">`[ClientCertExclusionPath <String>]`: client certificate authentication comma-separated exclusion paths</span></span>
  - <span data-ttu-id="20ceb-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: 복제 된 앱에 대 한 응용 프로그램 설정 재정의입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-156">`[CloningInfoAppSettingsOverride <ICloningInfoAppSettingsOverrides>]`: Application setting overrides for cloned app.</span></span> <span data-ttu-id="20ceb-157">이 설정을 지정 하면 원본 앱에서 복제 된 설정이 재정의 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-157">If specified, these settings override the settings cloned         from source app.</span></span> <span data-ttu-id="20ceb-158">그렇지 않으면 원본 앱의 응용 프로그램 설정이 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-158">Otherwise, application settings from source app are retained.</span></span>
    - <span data-ttu-id="20ceb-159">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-159">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="20ceb-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> 원본 앱에서 사용자 지정 호스트 이름을 복제 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-160">`[CloningInfoCloneCustomHostName <Boolean?>]`: <code>true</code> to clone custom hostnames from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> 원본 앱에서 원본 컨트롤을 복제 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-161">`[CloningInfoCloneSourceControl <Boolean?>]`: <code>true</code> to clone source control from source app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> 원본 및 대상 앱에 대 한 부하 분산을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-162">`[CloningInfoConfigureLoadBalancing <Boolean?>]`: <code>true</code> to configure load balancing for source and destination app.</span></span>
  - <span data-ttu-id="20ceb-163">`[CloningInfoCorrelationId <String>]`: 복제 작업의 상관 관계 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-163">`[CloningInfoCorrelationId <String>]`: Correlation ID of cloning operation.</span></span> <span data-ttu-id="20ceb-164">이 ID는 여러 복제 작업을 결합 하 여 동일한 스냅숏을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-164">This ID ties multiple cloning operations         together to use the same snapshot.</span></span>
  - <span data-ttu-id="20ceb-165">`[CloningInfoHostingEnvironment <String>]`: 앱 서비스 환경.</span><span class="sxs-lookup"><span data-stu-id="20ceb-165">`[CloningInfoHostingEnvironment <String>]`: App Service Environment.</span></span>
  - <span data-ttu-id="20ceb-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> 대상 앱을 덮어쓰려면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-166">`[CloningInfoOverwrite <Boolean?>]`: <code>true</code> to overwrite destination app; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-167">`[CloningInfoSourceWebAppLocation <String>]`: 원본 앱의 위치 예: 미국 서 부 또는 서유럽</span><span class="sxs-lookup"><span data-stu-id="20ceb-167">`[CloningInfoSourceWebAppLocation <String>]`: Location of source app ex: West US or North Europe</span></span>
  - <span data-ttu-id="20ceb-168">`[CloningInfoTrafficManagerProfileId <String>]`: 사용할 Traffic Manager 프로필의 ARM 리소스 ID입니다 (있는 경우).</span><span class="sxs-lookup"><span data-stu-id="20ceb-168">`[CloningInfoTrafficManagerProfileId <String>]`: ARM resource ID of the Traffic Manager profile to use, if it exists.</span></span> <span data-ttu-id="20ceb-169">Traffic Manager 리소스 ID의 형식/subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span><span class="sxs-lookup"><span data-stu-id="20ceb-169">Traffic Manager resource ID is of the form         /subscriptions/{subId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/trafficManagerProfiles/{profileName}.</span></span>
  - <span data-ttu-id="20ceb-170">`[CloningInfoTrafficManagerProfileName <String>]`: 만들려는 Traffic Manager 프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-170">`[CloningInfoTrafficManagerProfileName <String>]`: Name of Traffic Manager profile to create.</span></span> <span data-ttu-id="20ceb-171">이는 Traffic Manager 프로필이 아직 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-171">This is only needed if Traffic Manager profile does not already exist.</span></span>
  - <span data-ttu-id="20ceb-172">`[Config <ISiteConfig>]`: 앱의 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-172">`[Config <ISiteConfig>]`: Configuration of the app.</span></span>
    - <span data-ttu-id="20ceb-173">`IsPushEnabled <Boolean>`: 푸시 끝점을 사용할 수 있는지 여부를 나타내는 플래그를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-173">`IsPushEnabled <Boolean>`: Gets or sets a flag indicating whether the Push endpoint is enabled.</span></span>
    - <span data-ttu-id="20ceb-174">`[ActionMinProcessExecutionTime <String>]`: 작업을 수행 하기 전에 프로세스를 실행 해야 하는 최소 시간</span><span class="sxs-lookup"><span data-stu-id="20ceb-174">`[ActionMinProcessExecutionTime <String>]`: Minimum time the process must execute         before taking the action</span></span>
    - <span data-ttu-id="20ceb-175">`[ActionType <AutoHealActionType?>]`: 수행 되도록 미리 정의 된 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-175">`[ActionType <AutoHealActionType?>]`: Predefined action to be taken.</span></span>
    - <span data-ttu-id="20ceb-176">`[AlwaysOn <Boolean?>]`: <code>true</code> Always On을 사용 하도록 설정 되 면, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-176">`[AlwaysOn <Boolean?>]`: <code>true</code> if Always On is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-177">`[ApiDefinitionUrl <String>]`: API 정의의 URL입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-177">`[ApiDefinitionUrl <String>]`: The URL of the API definition.</span></span>
    - <span data-ttu-id="20ceb-178">`[ApiManagementConfigId <String>]`: APIM-Api 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-178">`[ApiManagementConfigId <String>]`: APIM-Api Identifier.</span></span>
    - <span data-ttu-id="20ceb-179">`[AppCommandLine <String>]`: 실행할 앱 명령줄입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-179">`[AppCommandLine <String>]`: App command line to launch.</span></span>
    - <span data-ttu-id="20ceb-180">`[AppSetting <INameValuePair[]>]`: 응용 프로그램 설정</span><span class="sxs-lookup"><span data-stu-id="20ceb-180">`[AppSetting <INameValuePair[]>]`: Application settings.</span></span>
      - <span data-ttu-id="20ceb-181">`[Name <String>]`: 쌍 이름.</span><span class="sxs-lookup"><span data-stu-id="20ceb-181">`[Name <String>]`: Pair name.</span></span>
      - <span data-ttu-id="20ceb-182">`[Value <String>]`: Pair 값.</span><span class="sxs-lookup"><span data-stu-id="20ceb-182">`[Value <String>]`: Pair value.</span></span>
    - <span data-ttu-id="20ceb-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> 자동 치료를 사용 하는 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-183">`[AutoHealEnabled <Boolean?>]`: <code>true</code> if Auto Heal is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-184">`[AutoSwapSlotName <String>]`: 자동 스왑 슬롯 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-184">`[AutoSwapSlotName <String>]`: Auto-swap slot name.</span></span>
    - <span data-ttu-id="20ceb-185">`[ConnectionString <IConnStringInfo[]>]`: 연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-185">`[ConnectionString <IConnStringInfo[]>]`: Connection strings.</span></span>
      - <span data-ttu-id="20ceb-186">`[ConnectionString <String>]`: 연결 문자열 값입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-186">`[ConnectionString <String>]`: Connection string value.</span></span>
      - <span data-ttu-id="20ceb-187">`[Name <String>]`: 연결 문자열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-187">`[Name <String>]`: Name of connection string.</span></span>
      - <span data-ttu-id="20ceb-188">`[Type <ConnectionStringType?>]`: 데이터베이스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-188">`[Type <ConnectionStringType?>]`: Type of database.</span></span>
    - <span data-ttu-id="20ceb-189">`[CorAllowedOrigin <String[]>]`: 교차 원본 호출을 허용 해야 하는 원본 목록 (예:)을 가져오거나 설정 http://example.com:12345) 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-189">`[CorAllowedOrigin <String[]>]`: Gets or sets the list of origins that should be allowed to make cross-origin         calls (for example: http://example.com:12345).</span></span> <span data-ttu-id="20ceb-190">"\*"를 사용 하 여 all을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-190">Use "\*" to allow all.</span></span>
    - <span data-ttu-id="20ceb-191">`[CorSupportCredentials <Boolean?>]`: 자격 증명을 사용 하 여 CORS 요청을 사용할 수 있는지 여부를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-191">`[CorSupportCredentials <Boolean?>]`: Gets or sets whether CORS requests with credentials are allowed.</span></span> <span data-ttu-id="20ceb-192">자세한 내용은         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ceb-192">See         https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS#Requests_with_credentials         for more details.</span></span>
    - <span data-ttu-id="20ceb-193">`[CustomActionExe <String>]`: 실행할 실행 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-193">`[CustomActionExe <String>]`: Executable to be run.</span></span>
    - <span data-ttu-id="20ceb-194">`[CustomActionParameter <String>]`: 실행 파일에 대 한 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-194">`[CustomActionParameter <String>]`: Parameters for the executable.</span></span>
    - <span data-ttu-id="20ceb-195">`[DefaultDocument <String[]>]`: 기본 문서.</span><span class="sxs-lookup"><span data-stu-id="20ceb-195">`[DefaultDocument <String[]>]`: Default documents.</span></span>
    - <span data-ttu-id="20ceb-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> 자세한 오류 로깅이 사용 되는 경우, 그렇지 않은 경우 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-196">`[DetailedErrorLoggingEnabled <Boolean?>]`: <code>true</code> if detailed error logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-197">`[DocumentRoot <String>]`: 문서 루트</span><span class="sxs-lookup"><span data-stu-id="20ceb-197">`[DocumentRoot <String>]`: Document root.</span></span>
    - <span data-ttu-id="20ceb-198">`[DynamicTagsJson <String>]`: 푸시 등록 끝점의 사용자 클레임에서 평가 되는 동적 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-198">`[DynamicTagsJson <String>]`: Gets or sets a JSON string containing a list of dynamic tags that will be evaluated from user claims in the push registration endpoint.</span></span>
    - <span data-ttu-id="20ceb-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: 램프 규칙의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-199">`[ExperimentRampUpRule <IRampUpRule[]>]`: List of ramp-up rules.</span></span>
      - <span data-ttu-id="20ceb-200">`[ActionHostName <String>]`: 트래픽을 결정 하는 경우 트래픽이 리디렉션되는 슬롯의 호스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-200">`[ActionHostName <String>]`: Hostname of a slot to which the traffic will be redirected if decided to.</span></span> <span data-ttu-id="20ceb-201">즉.</span><span class="sxs-lookup"><span data-stu-id="20ceb-201">E.g.</span></span> <span data-ttu-id="20ceb-202">myapp-stage.azurewebsites.net.</span><span class="sxs-lookup"><span data-stu-id="20ceb-202">myapp-stage.azurewebsites.net.</span></span>
      - <span data-ttu-id="20ceb-203">`[ChangeDecisionCallbackUrl <String>]`: 사용자 지정 결정 알고리즘은 TiPCallback 사이트 확장에서 지정할 수 있는 URL을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-203">`[ChangeDecisionCallbackUrl <String>]`: Custom decision algorithm can be provided in TiPCallback site extension which URL can be specified.</span></span> <span data-ttu-id="20ceb-204">모델링 및 계약에 대 한 TiPCallback 사이트 확장을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="20ceb-204">See TiPCallback site extension for the scaffold and contracts.</span></span>         <span data-ttu-id="20ceb-205"> https://www.siteextensions.net/packages/TiPCallback/</span><span class="sxs-lookup"><span data-stu-id="20ceb-205">https://www.siteextensions.net/packages/TiPCallback/</span></span>
      - <span data-ttu-id="20ceb-206">`[ChangeIntervalInMinute <Int32?>]`: ReroutePercentage를 다시 계산 하는 간격 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-206">`[ChangeIntervalInMinute <Int32?>]`: Specifies interval in minutes to reevaluate ReroutePercentage.</span></span>
      - <span data-ttu-id="20ceb-207">`[ChangeStep <Double?>]`: 자동 램프 시나리오에서 <code>ReroutePercentage</code> \n 또는에 도달할 때까지 추가/제거 하는 단계입니다 <code>MinReroutePercentage</code>         <code>MaxReroutePercentage</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-207">`[ChangeStep <Double?>]`: In auto ramp up scenario this is the step to add/remove from <code>ReroutePercentage</code> until it reaches \n<code>MinReroutePercentage</code> or         <code>MaxReroutePercentage</code>.</span></span> <span data-ttu-id="20ceb-208">사이트 메트릭은 .\NCustom 의사 결정 알고리즘에 지정 된 매 N 분을 <code>ChangeIntervalInMinutes</code> TiPCallback site extension에서 제공 하 고 URL에서 지정할 수 있는 것으로 확인 됩니다 <code>ChangeDecisionCallbackUrl</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-208">Site metrics are checked every N minutes specified in <code>ChangeIntervalInMinutes</code>.\nCustom decision algorithm         can be provided in TiPCallback site extension which URL can be specified in <code>ChangeDecisionCallbackUrl</code>.</span></span>
      - <span data-ttu-id="20ceb-209">`[MaxReroutePercentage <Double?>]`: ReroutePercentage가 유지 되는 위쪽 경계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-209">`[MaxReroutePercentage <Double?>]`: Specifies upper boundary below which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="20ceb-210">`[MinReroutePercentage <Double?>]`: ReroutePercentage이 유지 되는 아래쪽 경계를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-210">`[MinReroutePercentage <Double?>]`: Specifies lower boundary above which ReroutePercentage will stay.</span></span>
      - <span data-ttu-id="20ceb-211">`[Name <String>]`: 라우팅 규칙의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-211">`[Name <String>]`: Name of the routing rule.</span></span> <span data-ttu-id="20ceb-212">권장 되는 이름은 실험에서 트래픽을 수신 하는 슬롯을 가리키도록 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-212">The recommended name would be to point to the slot which will receive the traffic in the experiment.</span></span>
      - <span data-ttu-id="20ceb-213">`[ReroutePercentage <Double?>]`: 리디렉션되는 소통량의 백분율 <code>ActionHostName</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-213">`[ReroutePercentage <Double?>]`: Percentage of the traffic which will be redirected to <code>ActionHostName</code>.</span></span>
    - <span data-ttu-id="20ceb-214">`[FtpsState <FtpsState?>]`: FTP/FTPS 서비스의 상태</span><span class="sxs-lookup"><span data-stu-id="20ceb-214">`[FtpsState <FtpsState?>]`: State of FTP / FTPS service</span></span>
    - <span data-ttu-id="20ceb-215">`[HandlerMapping <IHandlerMapping[]>]`: 처리기 매핑.</span><span class="sxs-lookup"><span data-stu-id="20ceb-215">`[HandlerMapping <IHandlerMapping[]>]`: Handler mappings.</span></span>
      - <span data-ttu-id="20ceb-216">`[Argument <String>]`: 스크립트 프로세서에 전달할 명령줄 인수입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-216">`[Argument <String>]`: Command-line arguments to be passed to the script processor.</span></span>
      - <span data-ttu-id="20ceb-217">`[Extension <String>]`:이 확장명을 가진 요청은 지정 된 FastCGI 응용 프로그램을 사용 하 여 처리 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-217">`[Extension <String>]`: Requests with this extension will be handled using the specified FastCGI application.</span></span>
      - <span data-ttu-id="20ceb-218">`[ScriptProcessor <String>]`: FastCGI 응용 프로그램의 절대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-218">`[ScriptProcessor <String>]`: The absolute path to the FastCGI application.</span></span>
    - <span data-ttu-id="20ceb-219">`[HealthCheckPath <String>]`: 상태 검사 경로</span><span class="sxs-lookup"><span data-stu-id="20ceb-219">`[HealthCheckPath <String>]`: Health check path</span></span>
    - <span data-ttu-id="20ceb-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: 클라이언트가 http 2.0을 통해 연결할 수 있도록 웹 사이트를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-220">`[Http20Enabled <Boolean?>]`: Http20Enabled: configures a web site to allow clients to connect over http2.0</span></span>
    - <span data-ttu-id="20ceb-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> HTTP 로깅이 사용 하도록 설정 되어 있으면 이 고, 그렇지 않으면 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-221">`[HttpLoggingEnabled <Boolean?>]`: <code>true</code> if HTTP logging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: 메인에 대 한 IP 보안 제한.</span><span class="sxs-lookup"><span data-stu-id="20ceb-222">`[IPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for main.</span></span>
      - <span data-ttu-id="20ceb-223">`[Action <String>]`:이 IP 범위에 대 한 액세스를 허용 하거나 거부 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-223">`[Action <String>]`: Allow or Deny access for this IP range.</span></span>
      - <span data-ttu-id="20ceb-224">`[Description <String>]`: IP 제한 규칙 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-224">`[Description <String>]`: IP restriction rule description.</span></span>
      - <span data-ttu-id="20ceb-225">`[IPAddress <String>]`: IP 주소 보안 제한이에 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-225">`[IPAddress <String>]`: IP address the security restriction is valid for.</span></span>         <span data-ttu-id="20ceb-226">순수한 ipv4 주소 (필수 SubnetMask 속성) 또는 ipv4/ipv6 표기법 (예: ipv4/mask (행간 비트 일치))의 형태가 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-226">It can be in form of pure ipv4 address (required SubnetMask property) or         CIDR notation such as ipv4/mask (leading bit match).</span></span> <span data-ttu-id="20ceb-227">CIDR의 경우 SubnetMask 속성을 지정 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-227">For CIDR,         SubnetMask property must not be specified.</span></span>
      - <span data-ttu-id="20ceb-228">`[Name <String>]`: IP 제한 규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-228">`[Name <String>]`: IP restriction rule name.</span></span>
      - <span data-ttu-id="20ceb-229">`[Priority <Int32?>]`: IP 제한 규칙의 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-229">`[Priority <Int32?>]`: Priority of IP restriction rule.</span></span>
      - <span data-ttu-id="20ceb-230">`[SubnetMask <String>]`: 제한이 유효한 IP 주소 범위에 대 한 서브넷 마스크입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-230">`[SubnetMask <String>]`: Subnet mask for the range of IP addresses the restriction is valid for.</span></span>
      - <span data-ttu-id="20ceb-231">`[SubnetTrafficTag <Int32?>]`: (내부) 서브넷 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="20ceb-231">`[SubnetTrafficTag <Int32?>]`: (internal) Subnet traffic tag</span></span>
      - <span data-ttu-id="20ceb-232">`[Tag <IPFilterTag?>]`:이 IP 필터를 사용할 용도를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-232">`[Tag <IPFilterTag?>]`: Defines what this IP filter will be used for.</span></span> <span data-ttu-id="20ceb-233">이는 프록시에서 IP 필터링을 지원 하기 위한 것입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-233">This is to support IP filtering on proxies.</span></span>
      - <span data-ttu-id="20ceb-234">`[VnetSubnetResourceId <String>]`: 가상 네트워크 리소스 id</span><span class="sxs-lookup"><span data-stu-id="20ceb-234">`[VnetSubnetResourceId <String>]`: Virtual network resource id</span></span>
      - <span data-ttu-id="20ceb-235">`[VnetTrafficTag <Int32?>]`: (내부) Vnet 트래픽 태그</span><span class="sxs-lookup"><span data-stu-id="20ceb-235">`[VnetTrafficTag <Int32?>]`: (internal) Vnet traffic tag</span></span>
    - <span data-ttu-id="20ceb-236">`[JavaContainer <String>]`: Java 컨테이너.</span><span class="sxs-lookup"><span data-stu-id="20ceb-236">`[JavaContainer <String>]`: Java container.</span></span>
    - <span data-ttu-id="20ceb-237">`[JavaContainerVersion <String>]`: Java 컨테이너 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-237">`[JavaContainerVersion <String>]`: Java container version.</span></span>
    - <span data-ttu-id="20ceb-238">`[JavaVersion <String>]`: Java 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-238">`[JavaVersion <String>]`: Java version.</span></span>
    - <span data-ttu-id="20ceb-239">`[LimitMaxDiskSizeInMb <Int64?>]`: 최대 허용 디스크 크기 사용량 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-239">`[LimitMaxDiskSizeInMb <Int64?>]`: Maximum allowed disk size usage in MB.</span></span>
    - <span data-ttu-id="20ceb-240">`[LimitMaxMemoryInMb <Int64?>]`: 허용 되는 최대 메모리 사용량 (MB)입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-240">`[LimitMaxMemoryInMb <Int64?>]`: Maximum allowed memory usage in MB.</span></span>
    - <span data-ttu-id="20ceb-241">`[LimitMaxPercentageCpu <Double?>]`: 허용 되는 최대 CPU 사용 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-241">`[LimitMaxPercentageCpu <Double?>]`: Maximum allowed CPU usage percentage.</span></span>
    - <span data-ttu-id="20ceb-242">`[LinuxFxVersion <String>]`: Linux 앱 프레임 워크 및 버전</span><span class="sxs-lookup"><span data-stu-id="20ceb-242">`[LinuxFxVersion <String>]`: Linux App Framework and version</span></span>
    - <span data-ttu-id="20ceb-243">`[LoadBalancing <SiteLoadBalancing?>]`: 사이트 로드 밸런싱.</span><span class="sxs-lookup"><span data-stu-id="20ceb-243">`[LoadBalancing <SiteLoadBalancing?>]`: Site load balancing.</span></span>
    - <span data-ttu-id="20ceb-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> 로컬 MySQL을 사용 하도록 설정 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-244">`[LocalMySqlEnabled <Boolean?>]`: <code>true</code> to enable local MySQL; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP 로그 디렉터리 크기 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-245">`[LogsDirectorySizeLimit <Int32?>]`: HTTP logs directory size limit.</span></span>
    - <span data-ttu-id="20ceb-246">`[MachineKeyDecryption <String>]`: 암호 해독에 사용 되는 알고리즘입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-246">`[MachineKeyDecryption <String>]`: Algorithm used for decryption.</span></span>
    - <span data-ttu-id="20ceb-247">`[MachineKeyDecryptionKey <String>]`: 암호 해독 키입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-247">`[MachineKeyDecryptionKey <String>]`: Decryption key.</span></span>
    - <span data-ttu-id="20ceb-248">`[MachineKeyValidation <String>]`: MachineKey 유효성 검사.</span><span class="sxs-lookup"><span data-stu-id="20ceb-248">`[MachineKeyValidation <String>]`: MachineKey validation.</span></span>
    - <span data-ttu-id="20ceb-249">`[MachineKeyValidationKey <String>]`: 유효성 검사 키입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-249">`[MachineKeyValidationKey <String>]`: Validation key.</span></span>
    - <span data-ttu-id="20ceb-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: 관리 되는 파이프라인 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-250">`[ManagedPipelineMode <ManagedPipelineMode?>]`: Managed pipeline mode.</span></span>
    - <span data-ttu-id="20ceb-251">`[ManagedServiceIdentityId <Int32?>]`: 관리 되는 서비스 Id Id</span><span class="sxs-lookup"><span data-stu-id="20ceb-251">`[ManagedServiceIdentityId <Int32?>]`: Managed Service Identity Id</span></span>
    - <span data-ttu-id="20ceb-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: SSL 요청에 필요한 TLS의 최소 버전을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-252">`[MinTlsVersion <SupportedTlsVersions?>]`: MinTlsVersion: configures the minimum version of TLS required for SSL requests</span></span>
    - <span data-ttu-id="20ceb-253">`[NetFrameworkVersion <String>]`: .NET Framework 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-253">`[NetFrameworkVersion <String>]`: .NET Framework version.</span></span>
    - <span data-ttu-id="20ceb-254">`[NodeVersion <String>]`: Node.js 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-254">`[NodeVersion <String>]`: Version of Node.js.</span></span>
    - <span data-ttu-id="20ceb-255">`[NumberOfWorker <Int32?>]`: 작업자 수.</span><span class="sxs-lookup"><span data-stu-id="20ceb-255">`[NumberOfWorker <Int32?>]`: Number of workers.</span></span>
    - <span data-ttu-id="20ceb-256">`[PhpVersion <String>]`: PHP 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-256">`[PhpVersion <String>]`: Version of PHP.</span></span>
    - <span data-ttu-id="20ceb-257">`[PowerShellVersion <String>]`: PowerShell의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-257">`[PowerShellVersion <String>]`: Version of PowerShell.</span></span>
    - <span data-ttu-id="20ceb-258">`[PreWarmedInstanceCount <Int32?>]`: PreWarmed 인스턴스 수입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-258">`[PreWarmedInstanceCount <Int32?>]`: Number of preWarmed instances.</span></span>         <span data-ttu-id="20ceb-259">이 설정은 사용량과 탄력적 요금제에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-259">This setting only applies to the Consumption and Elastic Plans</span></span>
    - <span data-ttu-id="20ceb-260">`[PublishingUsername <String>]`: 게시 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-260">`[PublishingUsername <String>]`: Publishing user name.</span></span>
    - <span data-ttu-id="20ceb-261">`[PushKind <String>]`: 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-261">`[PushKind <String>]`: Kind of resource.</span></span>
    - <span data-ttu-id="20ceb-262">`[PythonVersion <String>]`: Python의 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-262">`[PythonVersion <String>]`: Version of Python.</span></span>
    - <span data-ttu-id="20ceb-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> 원격 디버깅을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-263">`[RemoteDebuggingEnabled <Boolean?>]`: <code>true</code> if remote debugging is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-264">`[RemoteDebuggingVersion <String>]`: 원격 디버깅 버전.</span><span class="sxs-lookup"><span data-stu-id="20ceb-264">`[RemoteDebuggingVersion <String>]`: Remote debugging version.</span></span>
    - <span data-ttu-id="20ceb-265">`[RequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="20ceb-265">`[RequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="20ceb-266">`[RequestTimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="20ceb-266">`[RequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="20ceb-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> 요청 추적을 사용 하도록 설정 하면 이 고, 그렇지 않으면 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-267">`[RequestTracingEnabled <Boolean?>]`: <code>true</code> if request tracing is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-268">`[RequestTracingExpirationTime <DateTime?>]`: 추적 만료 시간을 요청 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-268">`[RequestTracingExpirationTime <DateTime?>]`: Request tracing expiration time.</span></span>
    - <span data-ttu-id="20ceb-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: Scm에 대 한 IP 보안 제한.</span><span class="sxs-lookup"><span data-stu-id="20ceb-269">`[ScmIPSecurityRestriction <IIPSecurityRestriction[]>]`: IP security restrictions for scm.</span></span>
    - <span data-ttu-id="20ceb-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: Scm이 main을 사용할 수 있는 IP 보안 제한입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-270">`[ScmIPSecurityRestrictionsUseMain <Boolean?>]`: IP security restrictions for scm to use main.</span></span>
    - <span data-ttu-id="20ceb-271">`[ScmType <ScmType?>]`: SCM 유형.</span><span class="sxs-lookup"><span data-stu-id="20ceb-271">`[ScmType <ScmType?>]`: SCM type.</span></span>
    - <span data-ttu-id="20ceb-272">`[SlowRequestCount <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="20ceb-272">`[SlowRequestCount <Int32?>]`: Request Count.</span></span>
    - <span data-ttu-id="20ceb-273">`[SlowRequestTimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="20ceb-273">`[SlowRequestTimeInterval <String>]`: Time interval.</span></span>
    - <span data-ttu-id="20ceb-274">`[SlowRequestTimeTaken <String>]`: 소요 시간.</span><span class="sxs-lookup"><span data-stu-id="20ceb-274">`[SlowRequestTimeTaken <String>]`: Time taken.</span></span>
    - <span data-ttu-id="20ceb-275">`[TagWhitelistJson <String>]`: 푸시 등록 끝점에서 사용 하는 허용 목록 태그 목록을 포함 하는 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-275">`[TagWhitelistJson <String>]`: Gets or sets a JSON string containing a list of tags that are whitelisted for use by the push registration endpoint.</span></span>
    - <span data-ttu-id="20ceb-276">`[TagsRequiringAuth <String>]`: 푸시 등록 끝점에서 사용자 인증을 사용 해야 하는 태그 목록이 포함 된 JSON 문자열을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-276">`[TagsRequiringAuth <String>]`: Gets or sets a JSON string containing a list of tags that require user authentication to be used in the push registration endpoint.</span></span>         <span data-ttu-id="20ceb-277">태그는 영숫자 문자로 구성 되며 ' _ ', ' @ ', ' # ', '. ', ': ', '-'로 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-277">Tags can consist of alphanumeric characters and the following:         '_', '@', '#', '.', ':', '-'.</span></span>         <span data-ttu-id="20ceb-278">PushRequestHandler에서 유효성 검사를 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-278">Validation should be performed at the PushRequestHandler.</span></span>
    - <span data-ttu-id="20ceb-279">`[TracingOption <String>]`: 추적 옵션</span><span class="sxs-lookup"><span data-stu-id="20ceb-279">`[TracingOption <String>]`: Tracing options.</span></span>
    - <span data-ttu-id="20ceb-280">`[TriggerPrivateBytesInKb <Int32?>]`: 전용 바이트를 기준으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-280">`[TriggerPrivateBytesInKb <Int32?>]`: A rule based on private bytes.</span></span>
    - <span data-ttu-id="20ceb-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: 상태 코드를 기준으로 하는 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-281">`[TriggerStatusCode <IStatusCodesBasedTrigger[]>]`: A rule based on status codes.</span></span>
      - <span data-ttu-id="20ceb-282">`[Count <Int32?>]`: 요청 수.</span><span class="sxs-lookup"><span data-stu-id="20ceb-282">`[Count <Int32?>]`: Request Count.</span></span>
      - <span data-ttu-id="20ceb-283">`[Status <Int32?>]`: HTTP 상태 코드.</span><span class="sxs-lookup"><span data-stu-id="20ceb-283">`[Status <Int32?>]`: HTTP status code.</span></span>
      - <span data-ttu-id="20ceb-284">`[SubStatus <Int32?>]`: 하위 상태 요청</span><span class="sxs-lookup"><span data-stu-id="20ceb-284">`[SubStatus <Int32?>]`: Request Sub Status.</span></span>
      - <span data-ttu-id="20ceb-285">`[TimeInterval <String>]`: 시간 간격.</span><span class="sxs-lookup"><span data-stu-id="20ceb-285">`[TimeInterval <String>]`: Time interval.</span></span>
      - <span data-ttu-id="20ceb-286">`[Win32Status <Int32?>]`: Win32 오류 코드.</span><span class="sxs-lookup"><span data-stu-id="20ceb-286">`[Win32Status <Int32?>]`: Win32 error code.</span></span>
    - <span data-ttu-id="20ceb-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> 32 비트 작업자 프로세스를 사용 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-287">`[Use32BitWorkerProcess <Boolean?>]`: <code>true</code> to use 32-bit worker process; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-288">`[VirtualApplication <IVirtualApplication[]>]`: 가상 응용 프로그램.</span><span class="sxs-lookup"><span data-stu-id="20ceb-288">`[VirtualApplication <IVirtualApplication[]>]`: Virtual applications.</span></span>
      - <span data-ttu-id="20ceb-289">`[PhysicalPath <String>]`: 실제 경로.</span><span class="sxs-lookup"><span data-stu-id="20ceb-289">`[PhysicalPath <String>]`: Physical path.</span></span>
      - <span data-ttu-id="20ceb-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> 미리 로드를 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-290">`[PreloadEnabled <Boolean?>]`: <code>true</code> if preloading is enabled; otherwise, <code>false</code>.</span></span>
      - <span data-ttu-id="20ceb-291">`[VirtualDirectory <IVirtualDirectory[]>]`: 가상 응용 프로그램의 가상 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-291">`[VirtualDirectory <IVirtualDirectory[]>]`: Virtual directories for virtual application.</span></span>
        - <span data-ttu-id="20ceb-292">`[PhysicalPath <String>]`: 실제 경로.</span><span class="sxs-lookup"><span data-stu-id="20ceb-292">`[PhysicalPath <String>]`: Physical path.</span></span>
        - <span data-ttu-id="20ceb-293">`[VirtualPath <String>]`: 가상 응용 프로그램 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-293">`[VirtualPath <String>]`: Path to virtual application.</span></span>
      - <span data-ttu-id="20ceb-294">`[VirtualPath <String>]`: 가상 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-294">`[VirtualPath <String>]`: Virtual path.</span></span>
    - <span data-ttu-id="20ceb-295">`[VnetName <String>]`: 가상 네트워크 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-295">`[VnetName <String>]`: Virtual Network name.</span></span>
    - <span data-ttu-id="20ceb-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> WebSocket을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-296">`[WebSocketsEnabled <Boolean?>]`: <code>true</code> if WebSocket is enabled; otherwise, <code>false</code>.</span></span>
    - <span data-ttu-id="20ceb-297">`[WindowsFxVersion <String>]`: 크 세 앱 프레임 워크 및 버전</span><span class="sxs-lookup"><span data-stu-id="20ceb-297">`[WindowsFxVersion <String>]`: Xenon App Framework and version</span></span>
    - <span data-ttu-id="20ceb-298">`[XManagedServiceIdentityId <Int32?>]`: 관리 되는 명시적 서비스 Id Id</span><span class="sxs-lookup"><span data-stu-id="20ceb-298">`[XManagedServiceIdentityId <Int32?>]`: Explicit Managed Service Identity Id</span></span>
  - <span data-ttu-id="20ceb-299">`[ContainerSize <Int32?>]`: 함수 컨테이너의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-299">`[ContainerSize <Int32?>]`: Size of the function container.</span></span>
  - <span data-ttu-id="20ceb-300">`[DailyMemoryTimeQuota <Int32?>]`: 허용 되는 최대 메모리 시간 할당량 (동적 앱에만 해당).</span><span class="sxs-lookup"><span data-stu-id="20ceb-300">`[DailyMemoryTimeQuota <Int32?>]`: Maximum allowed daily memory-time quota (applicable on dynamic apps only).</span></span>
  - <span data-ttu-id="20ceb-301">`[Enabled <Boolean?>]`: <code>true</code> 앱을 사용 하도록 설정한 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-301">`[Enabled <Boolean?>]`: <code>true</code> if the app is enabled; otherwise, <code>false</code>.</span></span> <span data-ttu-id="20ceb-302">이 값을 false로 설정 하면 앱을 사용할 수 없게 됩니다 (앱을 오프 라인 상태로 전환).</span><span class="sxs-lookup"><span data-stu-id="20ceb-302">Setting this value to false disables the app (takes the app offline).</span></span>
  - <span data-ttu-id="20ceb-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL 상태는 앱의 호스트 이름에 대 한 SSL 바인딩을 관리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-303">`[HostNameSslState <IHostNameSslState[]>]`: Hostname SSL states are used to manage the SSL bindings for app's hostnames.</span></span>
    - <span data-ttu-id="20ceb-304">`[HostType <HostType?>]`: 호스트 이름이 표준 또는 리포지토리 호스트 이름 인지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-304">`[HostType <HostType?>]`: Indicates whether the hostname is a standard or repository hostname.</span></span>
    - <span data-ttu-id="20ceb-305">`[Name <String>]`이름의.</span><span class="sxs-lookup"><span data-stu-id="20ceb-305">`[Name <String>]`: Hostname.</span></span>
    - <span data-ttu-id="20ceb-306">`[SslState <SslState?>]`: SSL 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-306">`[SslState <SslState?>]`: SSL type.</span></span>
    - <span data-ttu-id="20ceb-307">`[Thumbprint <String>]`: SSL 인증서 지문.</span><span class="sxs-lookup"><span data-stu-id="20ceb-307">`[Thumbprint <String>]`: SSL certificate thumbprint.</span></span>
    - <span data-ttu-id="20ceb-308">`[ToUpdate <Boolean?>]`: <code>true</code> 기존 호스트 이름을 업데이트 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-308">`[ToUpdate <Boolean?>]`: Set to <code>true</code> to update existing hostname.</span></span>
    - <span data-ttu-id="20ceb-309">`[VirtualIP <String>]`: IP 기반 SSL을 사용 하는 경우 호스트 이름에 가상 IP 주소를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-309">`[VirtualIP <String>]`: Virtual IP address assigned to the hostname if IP based SSL is enabled.</span></span>
  - <span data-ttu-id="20ceb-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> 앱의 공용 호스트 이름을 사용 하지 않도록 설정 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-310">`[HostNamesDisabled <Boolean?>]`: <code>true</code> to disable the public hostnames of the app; otherwise, <code>false</code>.</span></span>          <span data-ttu-id="20ceb-311"><code>true</code>앱이 API management 프로세스를 통해서만 액세스할 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="20ceb-311">If <code>true</code>, the app is only accessible via API management process.</span></span>
  - <span data-ttu-id="20ceb-312">`[HostingEnvironmentProfileId <String>]`: 앱 서비스 환경의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-312">`[HostingEnvironmentProfileId <String>]`: Resource ID of the App Service Environment.</span></span>
  - <span data-ttu-id="20ceb-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: 웹 사이트가 https 요청만 수락 하도록 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-313">`[HttpsOnly <Boolean?>]`: HttpsOnly: configures a web site to accept only https requests.</span></span> <span data-ttu-id="20ceb-314">Http 요청에 대 한 문제 리디렉션</span><span class="sxs-lookup"><span data-stu-id="20ceb-314">Issues redirect for         http requests</span></span>
  - <span data-ttu-id="20ceb-315">`[HyperV <Boolean?>]`: Hyper-v 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="20ceb-315">`[HyperV <Boolean?>]`: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="20ceb-316">`[IdentityType <ManagedServiceIdentityType?>]`: 관리 되는 서비스 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-316">`[IdentityType <ManagedServiceIdentityType?>]`: Type of managed service identity.</span></span>
  - <span data-ttu-id="20ceb-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: 리소스와 연결 된 사용자 할당 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-317">`[IdentityUserAssignedIdentity <IManagedServiceIdentityUserAssignedIdentities>]`: The list of user assigned identities associated with the resource.</span></span> <span data-ttu-id="20ceb-318">사용자 id 사전 키 참조는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 팔로 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-318">The user identity dictionary key references will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}</span></span>
    - <span data-ttu-id="20ceb-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-319">`[(Any) <IComponents1Jq1T4ISchemasManagedserviceidentityPropertiesUserassignedidentitiesAdditionalproperties>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="20ceb-320">`[IsXenon <Boolean?>]`: 구식: Hyper-v 샌드박스.</span><span class="sxs-lookup"><span data-stu-id="20ceb-320">`[IsXenon <Boolean?>]`: Obsolete: Hyper-V sandbox.</span></span>
  - <span data-ttu-id="20ceb-321">`[RedundancyMode <RedundancyMode?>]`: 사이트 중복 모드</span><span class="sxs-lookup"><span data-stu-id="20ceb-321">`[RedundancyMode <RedundancyMode?>]`: Site redundancy mode</span></span>
  - <span data-ttu-id="20ceb-322">`[Reserved <Boolean?>]`: <code>true</code> 예약 된 경우, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-322">`[Reserved <Boolean?>]`: <code>true</code> if reserved; otherwise, <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> 앱이 중지 되 면 SCM (KUDU) 사이트를 중지 하 고, 그렇지 않으면 <code>false</code> .</span><span class="sxs-lookup"><span data-stu-id="20ceb-323">`[ScmSiteAlsoStopped <Boolean?>]`: <code>true</code> to stop SCM (KUDU) site when the app is stopped; otherwise, <code>false</code>.</span></span> <span data-ttu-id="20ceb-324">기본값은 <code>false</code> 입니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-324">The default is <code>false</code>.</span></span>
  - <span data-ttu-id="20ceb-325">`[ServerFarmId <String>]`: 연결 된 앱 서비스 계획의 리소스 ID: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}" 형식으로 지정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20ceb-325">`[ServerFarmId <String>]`: Resource ID of the associated App Service plan, formatted as: "/subscriptions/{subscriptionID}/resourceGroups/{groupName}/providers/Microsoft.Web/serverfarms/{appServicePlanName}".</span></span>

## <span data-ttu-id="20ceb-326">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20ceb-326">RELATED LINKS</span></span>

