---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013232"
---
# <span data-ttu-id="f7fe8-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="f7fe8-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="f7fe8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7fe8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7fe8-103">HealthBot을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-103">Get a HealthBot.</span></span>

## <span data-ttu-id="f7fe8-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7fe8-104">SYNTAX</span></span>

### <span data-ttu-id="f7fe8-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="f7fe8-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7fe8-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f7fe8-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7fe8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f7fe8-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f7fe8-108">목록</span><span class="sxs-lookup"><span data-stu-id="f7fe8-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7fe8-109">설명</span><span class="sxs-lookup"><span data-stu-id="f7fe8-109">DESCRIPTION</span></span>
<span data-ttu-id="f7fe8-110">HealthBot을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-110">Get a HealthBot.</span></span>

## <span data-ttu-id="f7fe8-111">예제</span><span class="sxs-lookup"><span data-stu-id="f7fe8-111">EXAMPLES</span></span>

### <span data-ttu-id="f7fe8-112">예제 1: 모든 HealthBot 사용</span><span class="sxs-lookup"><span data-stu-id="f7fe8-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f7fe8-113">모든 HealthBot을 얻다</span><span class="sxs-lookup"><span data-stu-id="f7fe8-113">Get all HealthBot</span></span>

### <span data-ttu-id="f7fe8-114">예제 2: ResourceGroupName에 의해 모든 HealthBot을 얻다</span><span class="sxs-lookup"><span data-stu-id="f7fe8-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f7fe8-115">ResourceGroupName에 의해 모든 HealthBot을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="f7fe8-116">예제 3: ResourceGroupName 및 Name에 의해 HealthBot을 얻다</span><span class="sxs-lookup"><span data-stu-id="f7fe8-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f7fe8-117">ResourceGroupName 및 Name에 의해 HealthBot을 얻다</span><span class="sxs-lookup"><span data-stu-id="f7fe8-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="f7fe8-118">예제 4: InputObject로 HealthBot을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="f7fe8-119">InputObject로 HealthBot을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="f7fe8-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f7fe8-120">PARAMETERS</span></span>

### <span data-ttu-id="f7fe8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7fe8-121">-DefaultProfile</span></span>
<span data-ttu-id="f7fe8-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7fe8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7fe8-123">-InputObject</span></span>
<span data-ttu-id="f7fe8-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7fe8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="f7fe8-125">-Name</span></span>
<span data-ttu-id="f7fe8-126">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="f7fe8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7fe8-127">-ResourceGroupName</span></span>
<span data-ttu-id="f7fe8-128">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="f7fe8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f7fe8-129">-SubscriptionId</span></span>
<span data-ttu-id="f7fe8-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="f7fe8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7fe8-131">CommonParameters</span></span>
<span data-ttu-id="f7fe8-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7fe8-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7fe8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7fe8-134">입력</span><span class="sxs-lookup"><span data-stu-id="f7fe8-134">INPUTS</span></span>

### <span data-ttu-id="f7fe8-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="f7fe8-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="f7fe8-136">출력</span><span class="sxs-lookup"><span data-stu-id="f7fe8-136">OUTPUTS</span></span>

### <span data-ttu-id="f7fe8-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="f7fe8-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="f7fe8-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7fe8-138">NOTES</span></span>

<span data-ttu-id="f7fe8-139">별칭</span><span class="sxs-lookup"><span data-stu-id="f7fe8-139">ALIASES</span></span>

<span data-ttu-id="f7fe8-140">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f7fe8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f7fe8-141">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f7fe8-142">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f7fe8-143">INPUTOBJECT <IHealthBotIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f7fe8-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f7fe8-144">`[BotName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="f7fe8-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="f7fe8-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f7fe8-146">`[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="f7fe8-147">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f7fe8-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="f7fe8-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7fe8-148">RELATED LINKS</span></span>

