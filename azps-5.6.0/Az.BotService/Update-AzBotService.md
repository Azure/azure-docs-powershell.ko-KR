---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: 330aca1a9d4cc9438bdf360d5aee4af914df6c7c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007291"
---
# <span data-ttu-id="e183c-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="e183c-101">Update-AzBotService</span></span>

## <span data-ttu-id="e183c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e183c-102">SYNOPSIS</span></span>
<span data-ttu-id="e183c-103">Bot Service 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-103">Updates a Bot Service</span></span>

## <span data-ttu-id="e183c-104">구문</span><span class="sxs-lookup"><span data-stu-id="e183c-104">SYNTAX</span></span>

### <span data-ttu-id="e183c-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="e183c-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e183c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e183c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e183c-107">설명</span><span class="sxs-lookup"><span data-stu-id="e183c-107">DESCRIPTION</span></span>
<span data-ttu-id="e183c-108">Bot Service 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-108">Updates a Bot Service</span></span>

## <span data-ttu-id="e183c-109">예제</span><span class="sxs-lookup"><span data-stu-id="e183c-109">EXAMPLES</span></span>

### <span data-ttu-id="e183c-110">예제 1: 이름 및 ResourceGroupName 봇 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="e183c-111">이름 및 ResourceGroupName 봇 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="e183c-112">예제 2: InputObject로 봇 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="e183c-113">InputObject로 봇 업데이트</span><span class="sxs-lookup"><span data-stu-id="e183c-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="e183c-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e183c-114">PARAMETERS</span></span>

### <span data-ttu-id="e183c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e183c-115">-DefaultProfile</span></span>
<span data-ttu-id="e183c-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e183c-117">-Description</span><span class="sxs-lookup"><span data-stu-id="e183c-117">-Description</span></span>
<span data-ttu-id="e183c-118">봇에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="e183c-118">The description of the bot</span></span>

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

### <span data-ttu-id="e183c-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="e183c-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="e183c-120">Application Insights 키</span><span class="sxs-lookup"><span data-stu-id="e183c-120">The Application Insights key</span></span>

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

### <span data-ttu-id="e183c-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="e183c-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="e183c-122">Application Insights Api 키</span><span class="sxs-lookup"><span data-stu-id="e183c-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="e183c-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="e183c-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="e183c-124">Application Insights 앱 ID</span><span class="sxs-lookup"><span data-stu-id="e183c-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="e183c-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e183c-125">-DisplayName</span></span>
<span data-ttu-id="e183c-126">봇의 이름</span><span class="sxs-lookup"><span data-stu-id="e183c-126">The Name of the bot</span></span>

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

### <span data-ttu-id="e183c-127">-엔드포인트</span><span class="sxs-lookup"><span data-stu-id="e183c-127">-Endpoint</span></span>
<span data-ttu-id="e183c-128">봇의 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="e183c-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="e183c-129">-Etag</span><span class="sxs-lookup"><span data-stu-id="e183c-129">-Etag</span></span>
<span data-ttu-id="e183c-130">엔터티 태그</span><span class="sxs-lookup"><span data-stu-id="e183c-130">Entity Tag</span></span>

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

### <span data-ttu-id="e183c-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="e183c-131">-IconUrl</span></span>
<span data-ttu-id="e183c-132">봇의 아이콘 URL</span><span class="sxs-lookup"><span data-stu-id="e183c-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="e183c-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e183c-133">-InputObject</span></span>
<span data-ttu-id="e183c-134">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="e183c-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e183c-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="e183c-135">-Kind</span></span>
<span data-ttu-id="e183c-136">필수.</span><span class="sxs-lookup"><span data-stu-id="e183c-136">Required.</span></span>
<span data-ttu-id="e183c-137">리소스의 종류를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e183c-138">-Location</span><span class="sxs-lookup"><span data-stu-id="e183c-138">-Location</span></span>
<span data-ttu-id="e183c-139">리소스의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="e183c-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="e183c-140">-LuisAppId</span></span>
<span data-ttu-id="e183c-141">LUIS 앱 ID 컬렉션</span><span class="sxs-lookup"><span data-stu-id="e183c-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="e183c-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="e183c-142">-LuisKey</span></span>
<span data-ttu-id="e183c-143">LUIS 키</span><span class="sxs-lookup"><span data-stu-id="e183c-143">The LUIS Key</span></span>

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

### <span data-ttu-id="e183c-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="e183c-144">-MsaAppId</span></span>
<span data-ttu-id="e183c-145">봇에 대한 Microsoft 앱 ID</span><span class="sxs-lookup"><span data-stu-id="e183c-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="e183c-146">-Name</span><span class="sxs-lookup"><span data-stu-id="e183c-146">-Name</span></span>
<span data-ttu-id="e183c-147">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-147">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e183c-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e183c-148">-ResourceGroupName</span></span>
<span data-ttu-id="e183c-149">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="e183c-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="e183c-150">-SkuName</span></span>
<span data-ttu-id="e183c-151">sku 이름</span><span class="sxs-lookup"><span data-stu-id="e183c-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e183c-152">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e183c-152">-SubscriptionId</span></span>
<span data-ttu-id="e183c-153">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="e183c-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="e183c-154">-Tag</span></span>
<span data-ttu-id="e183c-155">키/값 쌍으로 정의된 리소스 태그가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="e183c-156">-확인</span><span class="sxs-lookup"><span data-stu-id="e183c-156">-Confirm</span></span>
<span data-ttu-id="e183c-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e183c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e183c-158">-WhatIf</span></span>
<span data-ttu-id="e183c-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e183c-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e183c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e183c-161">CommonParameters</span></span>
<span data-ttu-id="e183c-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e183c-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e183c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e183c-164">입력</span><span class="sxs-lookup"><span data-stu-id="e183c-164">INPUTS</span></span>

### <span data-ttu-id="e183c-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="e183c-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="e183c-166">출력</span><span class="sxs-lookup"><span data-stu-id="e183c-166">OUTPUTS</span></span>

### <span data-ttu-id="e183c-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="e183c-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="e183c-168">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e183c-168">NOTES</span></span>

<span data-ttu-id="e183c-169">별칭</span><span class="sxs-lookup"><span data-stu-id="e183c-169">ALIASES</span></span>

<span data-ttu-id="e183c-170">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="e183c-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e183c-171">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e183c-172">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e183c-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e183c-173">INPUTOBJECT <IBotServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e183c-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e183c-174">`[ChannelName <ChannelName?>]`: 채널 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="e183c-175">`[ConnectionName <String>]`: 봇 서비스 연결 설정 리소스의 이름</span><span class="sxs-lookup"><span data-stu-id="e183c-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="e183c-176">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="e183c-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e183c-177">`[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="e183c-178">`[ResourceName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="e183c-179">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e183c-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="e183c-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e183c-180">RELATED LINKS</span></span>

