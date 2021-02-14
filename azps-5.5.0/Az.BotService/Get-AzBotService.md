---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181905"
---
# <span data-ttu-id="d85e6-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="d85e6-101">Get-AzBotService</span></span>

## <span data-ttu-id="d85e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d85e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d85e6-103">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d85e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="d85e6-104">SYNTAX</span></span>

### <span data-ttu-id="d85e6-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="d85e6-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d85e6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d85e6-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d85e6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d85e6-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d85e6-108">목록</span><span class="sxs-lookup"><span data-stu-id="d85e6-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d85e6-109">설명</span><span class="sxs-lookup"><span data-stu-id="d85e6-109">DESCRIPTION</span></span>
<span data-ttu-id="d85e6-110">매개 변수로 지정된 BotService를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="d85e6-111">예제</span><span class="sxs-lookup"><span data-stu-id="d85e6-111">EXAMPLES</span></span>

### <span data-ttu-id="d85e6-112">예제 1: 모든 BotServices를 얻게</span><span class="sxs-lookup"><span data-stu-id="d85e6-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="d85e6-113">모든 BotServices를 얻게</span><span class="sxs-lookup"><span data-stu-id="d85e6-113">Get all BotServices</span></span>

### <span data-ttu-id="d85e6-114">예제 2: ResourceGroupName 및 Name으로 BotService를 얻게</span><span class="sxs-lookup"><span data-stu-id="d85e6-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="d85e6-115">ResourceGroupName 및 Name으로 BotService를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="d85e6-116">예제 3: ResourceGroupName에서 모든 BotServices를 얻게</span><span class="sxs-lookup"><span data-stu-id="d85e6-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="d85e6-117">ResourceGroupName에서 모든 BotServices를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="d85e6-118">예제 4: inputObject로 BotService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="d85e6-119">inputObject로 BotService를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="d85e6-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d85e6-120">PARAMETERS</span></span>

### <span data-ttu-id="d85e6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d85e6-121">-DefaultProfile</span></span>
<span data-ttu-id="d85e6-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d85e6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d85e6-123">-InputObject</span></span>
<span data-ttu-id="d85e6-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d85e6-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d85e6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d85e6-125">-Name</span></span>
<span data-ttu-id="d85e6-126">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="d85e6-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d85e6-127">-ResourceGroupName</span></span>
<span data-ttu-id="d85e6-128">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="d85e6-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d85e6-129">-SubscriptionId</span></span>
<span data-ttu-id="d85e6-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="d85e6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d85e6-131">CommonParameters</span></span>
<span data-ttu-id="d85e6-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d85e6-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d85e6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d85e6-134">입력</span><span class="sxs-lookup"><span data-stu-id="d85e6-134">INPUTS</span></span>

### <span data-ttu-id="d85e6-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="d85e6-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="d85e6-136">출력</span><span class="sxs-lookup"><span data-stu-id="d85e6-136">OUTPUTS</span></span>

### <span data-ttu-id="d85e6-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="d85e6-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="d85e6-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d85e6-138">NOTES</span></span>

<span data-ttu-id="d85e6-139">별칭</span><span class="sxs-lookup"><span data-stu-id="d85e6-139">ALIASES</span></span>

<span data-ttu-id="d85e6-140">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d85e6-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d85e6-141">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d85e6-142">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d85e6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d85e6-143">INPUTOBJECT: <IBotServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d85e6-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d85e6-144">`[ChannelName <ChannelName?>]`: 채널 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="d85e6-145">`[ConnectionName <String>]`: Bot Service 연결 설정 리소스의 이름</span><span class="sxs-lookup"><span data-stu-id="d85e6-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="d85e6-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d85e6-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d85e6-147">`[ResourceGroupName <String>]`: 사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="d85e6-148">`[ResourceName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="d85e6-149">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d85e6-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d85e6-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d85e6-150">RELATED LINKS</span></span>

