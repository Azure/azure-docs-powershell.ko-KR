---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013211"
---
# <span data-ttu-id="270b6-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="270b6-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="270b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="270b6-102">SYNOPSIS</span></span>
<span data-ttu-id="270b6-103">HealthBot을 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="270b6-104">구문</span><span class="sxs-lookup"><span data-stu-id="270b6-104">SYNTAX</span></span>

### <span data-ttu-id="270b6-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="270b6-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="270b6-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="270b6-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="270b6-107">설명</span><span class="sxs-lookup"><span data-stu-id="270b6-107">DESCRIPTION</span></span>
<span data-ttu-id="270b6-108">HealthBot을 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="270b6-109">예제</span><span class="sxs-lookup"><span data-stu-id="270b6-109">EXAMPLES</span></span>

### <span data-ttu-id="270b6-110">예제 1: Resourcegroupname 및 Name에 의해 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="270b6-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="270b6-111">Resourcegroupname 및 Name에 의해 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="270b6-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="270b6-112">예제 2: InputObject로 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="270b6-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="270b6-113">InputObject에 의해 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="270b6-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="270b6-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="270b6-114">PARAMETERS</span></span>

### <span data-ttu-id="270b6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="270b6-115">-DefaultProfile</span></span>
<span data-ttu-id="270b6-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="270b6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="270b6-117">-InputObject</span></span>
<span data-ttu-id="270b6-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="270b6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="270b6-119">-Name</span><span class="sxs-lookup"><span data-stu-id="270b6-119">-Name</span></span>
<span data-ttu-id="270b6-120">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="270b6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="270b6-121">-ResourceGroupName</span></span>
<span data-ttu-id="270b6-122">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="270b6-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="270b6-123">-Sku</span></span>
<span data-ttu-id="270b6-124">HealthBot SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="270b6-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="270b6-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="270b6-125">-SubscriptionId</span></span>
<span data-ttu-id="270b6-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="270b6-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="270b6-127">-Tag</span></span>
<span data-ttu-id="270b6-128">HealthBot에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="270b6-129">-확인</span><span class="sxs-lookup"><span data-stu-id="270b6-129">-Confirm</span></span>
<span data-ttu-id="270b6-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="270b6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="270b6-131">-WhatIf</span></span>
<span data-ttu-id="270b6-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="270b6-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="270b6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="270b6-134">CommonParameters</span></span>
<span data-ttu-id="270b6-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="270b6-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="270b6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="270b6-137">입력</span><span class="sxs-lookup"><span data-stu-id="270b6-137">INPUTS</span></span>

### <span data-ttu-id="270b6-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="270b6-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="270b6-139">출력</span><span class="sxs-lookup"><span data-stu-id="270b6-139">OUTPUTS</span></span>

### <span data-ttu-id="270b6-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="270b6-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="270b6-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="270b6-141">NOTES</span></span>

<span data-ttu-id="270b6-142">별칭</span><span class="sxs-lookup"><span data-stu-id="270b6-142">ALIASES</span></span>

<span data-ttu-id="270b6-143">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="270b6-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="270b6-144">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="270b6-145">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="270b6-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="270b6-146">INPUTOBJECT <IHealthBotIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="270b6-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="270b6-147">`[BotName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="270b6-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="270b6-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="270b6-149">`[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="270b6-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="270b6-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="270b6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="270b6-151">RELATED LINKS</span></span>

