---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: b14ed0d682a6ba74eb557aae79a4fe151e952a73
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200185"
---
# <span data-ttu-id="a731f-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="a731f-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="a731f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a731f-102">SYNOPSIS</span></span>
<span data-ttu-id="a731f-103">HealthBot을 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="a731f-104">구문</span><span class="sxs-lookup"><span data-stu-id="a731f-104">SYNTAX</span></span>

### <span data-ttu-id="a731f-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="a731f-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a731f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a731f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a731f-107">설명</span><span class="sxs-lookup"><span data-stu-id="a731f-107">DESCRIPTION</span></span>
<span data-ttu-id="a731f-108">HealthBot을 패치합니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="a731f-109">예제</span><span class="sxs-lookup"><span data-stu-id="a731f-109">EXAMPLES</span></span>

### <span data-ttu-id="a731f-110">예제 1: Resourcegroupname 및 Name으로 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="a731f-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="a731f-111">Resourcegroupname 및 Name으로 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="a731f-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="a731f-112">예제 2: InputObject로 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="a731f-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="a731f-113">InputObject로 HealthBot 업데이트</span><span class="sxs-lookup"><span data-stu-id="a731f-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="a731f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a731f-114">PARAMETERS</span></span>

### <span data-ttu-id="a731f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a731f-115">-DefaultProfile</span></span>
<span data-ttu-id="a731f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a731f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a731f-117">-InputObject</span></span>
<span data-ttu-id="a731f-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="a731f-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a731f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a731f-119">-Name</span></span>
<span data-ttu-id="a731f-120">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="a731f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a731f-121">-ResourceGroupName</span></span>
<span data-ttu-id="a731f-122">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-122">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="a731f-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="a731f-123">-Sku</span></span>
<span data-ttu-id="a731f-124">HealthBot SKU의 이름</span><span class="sxs-lookup"><span data-stu-id="a731f-124">The name of the HealthBot SKU</span></span>

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

### <span data-ttu-id="a731f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a731f-125">-SubscriptionId</span></span>
<span data-ttu-id="a731f-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="a731f-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="a731f-127">-Tag</span></span>
<span data-ttu-id="a731f-128">HealthBot에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-128">Tags for a HealthBot.</span></span>

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

### <span data-ttu-id="a731f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a731f-129">-Confirm</span></span>
<span data-ttu-id="a731f-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a731f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a731f-131">-WhatIf</span></span>
<span data-ttu-id="a731f-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a731f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a731f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a731f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a731f-134">CommonParameters</span></span>
<span data-ttu-id="a731f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a731f-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a731f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a731f-137">입력</span><span class="sxs-lookup"><span data-stu-id="a731f-137">INPUTS</span></span>

### <span data-ttu-id="a731f-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="a731f-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="a731f-139">출력</span><span class="sxs-lookup"><span data-stu-id="a731f-139">OUTPUTS</span></span>

### <span data-ttu-id="a731f-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="a731f-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="a731f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a731f-141">NOTES</span></span>

<span data-ttu-id="a731f-142">별칭</span><span class="sxs-lookup"><span data-stu-id="a731f-142">ALIASES</span></span>

<span data-ttu-id="a731f-143">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="a731f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a731f-144">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a731f-145">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a731f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a731f-146">INPUTOBJECT: <IHealthBotIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a731f-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a731f-147">`[BotName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="a731f-148">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="a731f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a731f-149">`[ResourceGroupName <String>]`: 사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="a731f-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a731f-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="a731f-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a731f-151">RELATED LINKS</span></span>

