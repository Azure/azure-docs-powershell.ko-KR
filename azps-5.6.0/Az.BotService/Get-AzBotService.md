---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 305e65e95b876e3093f4a14590e8b2e111e44aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009312"
---
# <span data-ttu-id="1cd51-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="1cd51-101">Get-AzBotService</span></span>

## <span data-ttu-id="1cd51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cd51-102">SYNOPSIS</span></span>
<span data-ttu-id="1cd51-103">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1cd51-104">구문</span><span class="sxs-lookup"><span data-stu-id="1cd51-104">SYNTAX</span></span>

### <span data-ttu-id="1cd51-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="1cd51-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cd51-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1cd51-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cd51-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1cd51-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1cd51-108">목록</span><span class="sxs-lookup"><span data-stu-id="1cd51-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1cd51-109">설명</span><span class="sxs-lookup"><span data-stu-id="1cd51-109">DESCRIPTION</span></span>
<span data-ttu-id="1cd51-110">매개 변수에 의해 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1cd51-111">예제</span><span class="sxs-lookup"><span data-stu-id="1cd51-111">EXAMPLES</span></span>

### <span data-ttu-id="1cd51-112">예제 1: 모든 BotServices 사용</span><span class="sxs-lookup"><span data-stu-id="1cd51-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1cd51-113">모든 BotServices를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-113">Get all BotServices</span></span>

### <span data-ttu-id="1cd51-114">예제 2: ResourceGroupName 및 Name로 BotService를 얻다</span><span class="sxs-lookup"><span data-stu-id="1cd51-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1cd51-115">ResourceGroupName 및 Name로 BotService를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="1cd51-116">예제 3: ResourceGroupName에 의해 모든 BotServices를 얻다</span><span class="sxs-lookup"><span data-stu-id="1cd51-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1cd51-117">ResourceGroupName에 의해 모든 BotServices를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="1cd51-118">예제 4: inputObject로 BotService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1cd51-119">inputObject로 BotService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="1cd51-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1cd51-120">PARAMETERS</span></span>

### <span data-ttu-id="1cd51-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cd51-121">-DefaultProfile</span></span>
<span data-ttu-id="1cd51-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cd51-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cd51-123">-InputObject</span></span>
<span data-ttu-id="1cd51-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1cd51-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cd51-125">-Name</span><span class="sxs-lookup"><span data-stu-id="1cd51-125">-Name</span></span>
<span data-ttu-id="1cd51-126">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd51-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cd51-127">-ResourceGroupName</span></span>
<span data-ttu-id="1cd51-128">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd51-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1cd51-129">-SubscriptionId</span></span>
<span data-ttu-id="1cd51-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cd51-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cd51-131">CommonParameters</span></span>
<span data-ttu-id="1cd51-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cd51-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1cd51-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cd51-134">입력</span><span class="sxs-lookup"><span data-stu-id="1cd51-134">INPUTS</span></span>

### <span data-ttu-id="1cd51-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1cd51-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="1cd51-136">출력</span><span class="sxs-lookup"><span data-stu-id="1cd51-136">OUTPUTS</span></span>

### <span data-ttu-id="1cd51-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="1cd51-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="1cd51-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1cd51-138">NOTES</span></span>

<span data-ttu-id="1cd51-139">별칭</span><span class="sxs-lookup"><span data-stu-id="1cd51-139">ALIASES</span></span>

<span data-ttu-id="1cd51-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1cd51-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1cd51-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1cd51-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1cd51-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1cd51-143">INPUTOBJECT <IBotServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1cd51-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1cd51-144">`[ChannelName <ChannelName?>]`: 채널 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="1cd51-145">`[ConnectionName <String>]`: 봇 서비스 연결 설정 리소스의 이름</span><span class="sxs-lookup"><span data-stu-id="1cd51-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="1cd51-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1cd51-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1cd51-147">`[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="1cd51-148">`[ResourceName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="1cd51-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1cd51-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1cd51-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1cd51-150">RELATED LINKS</span></span>

