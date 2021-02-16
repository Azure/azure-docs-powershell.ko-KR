---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthbot/remove-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Remove-AzHealthBot.md
ms.openlocfilehash: 1a3125939e1640a6bd734ee8f75f36a4c34196ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207296"
---
# <span data-ttu-id="d7728-101">Remove-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="d7728-101">Remove-AzHealthBot</span></span>

## <span data-ttu-id="d7728-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7728-102">SYNOPSIS</span></span>
<span data-ttu-id="d7728-103">HealthBot을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-103">Delete a HealthBot.</span></span>

## <span data-ttu-id="d7728-104">구문</span><span class="sxs-lookup"><span data-stu-id="d7728-104">SYNTAX</span></span>

### <span data-ttu-id="d7728-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="d7728-105">Delete (Default)</span></span>
```
Remove-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d7728-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d7728-106">DeleteViaIdentity</span></span>
```
Remove-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d7728-107">설명</span><span class="sxs-lookup"><span data-stu-id="d7728-107">DESCRIPTION</span></span>
<span data-ttu-id="d7728-108">HealthBot을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-108">Delete a HealthBot.</span></span>

## <span data-ttu-id="d7728-109">예제</span><span class="sxs-lookup"><span data-stu-id="d7728-109">EXAMPLES</span></span>

### <span data-ttu-id="d7728-110">예제 1: ResourceGroupName 및 Name으로 HealthBot 삭제</span><span class="sxs-lookup"><span data-stu-id="d7728-110">Example 1: Delete HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Remove-AzHealthBot -Name yourihealthbot -ResourceGroupName youriTest

```

<span data-ttu-id="d7728-111">ResourceGroupName 및 Name으로 HealthBot 삭제</span><span class="sxs-lookup"><span data-stu-id="d7728-111">Delete HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="d7728-112">예제 2: InputObject로 HealthBot 삭제</span><span class="sxs-lookup"><span data-stu-id="d7728-112">Example 2: Delete HealthBot by InputObject</span></span>
```powershell
PS C:\> $gethealthbot = Get-AzHealthBot -Name yourihealthbot1 -ResourceGroupName youriTest
Remove-AzHealthBot -InputObject $gethealthbot

```

<span data-ttu-id="d7728-113">InputObject로 HealthBot 삭제</span><span class="sxs-lookup"><span data-stu-id="d7728-113">Delete HealthBot by InputObject</span></span>

## <span data-ttu-id="d7728-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7728-114">PARAMETERS</span></span>

### <span data-ttu-id="d7728-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7728-115">-AsJob</span></span>
<span data-ttu-id="d7728-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="d7728-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d7728-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7728-117">-DefaultProfile</span></span>
<span data-ttu-id="d7728-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7728-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d7728-119">-InputObject</span></span>
<span data-ttu-id="d7728-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="d7728-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7728-121">-Name</span><span class="sxs-lookup"><span data-stu-id="d7728-121">-Name</span></span>
<span data-ttu-id="d7728-122">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-122">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7728-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d7728-123">-NoWait</span></span>
<span data-ttu-id="d7728-124">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="d7728-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d7728-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d7728-125">-PassThru</span></span>
<span data-ttu-id="d7728-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d7728-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7728-127">-ResourceGroupName</span></span>
<span data-ttu-id="d7728-128">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-128">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7728-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d7728-129">-SubscriptionId</span></span>
<span data-ttu-id="d7728-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-130">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7728-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7728-131">-Confirm</span></span>
<span data-ttu-id="d7728-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7728-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7728-133">-WhatIf</span></span>
<span data-ttu-id="d7728-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d7728-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7728-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7728-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7728-136">CommonParameters</span></span>
<span data-ttu-id="d7728-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7728-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d7728-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7728-139">입력</span><span class="sxs-lookup"><span data-stu-id="d7728-139">INPUTS</span></span>

### <span data-ttu-id="d7728-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="d7728-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="d7728-141">출력</span><span class="sxs-lookup"><span data-stu-id="d7728-141">OUTPUTS</span></span>

### <span data-ttu-id="d7728-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d7728-142">System.Boolean</span></span>

## <span data-ttu-id="d7728-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d7728-143">NOTES</span></span>

<span data-ttu-id="d7728-144">별칭</span><span class="sxs-lookup"><span data-stu-id="d7728-144">ALIASES</span></span>

<span data-ttu-id="d7728-145">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="d7728-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d7728-146">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d7728-147">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d7728-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d7728-148">INPUTOBJECT: <IHealthBotIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d7728-148">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d7728-149">`[BotName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-149">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="d7728-150">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="d7728-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d7728-151">`[ResourceGroupName <String>]`: 사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-151">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="d7728-152">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d7728-152">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="d7728-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d7728-153">RELATED LINKS</span></span>

