---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: 486490a3b88025fb97b8790df202c944c05d888e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965072"
---
# <span data-ttu-id="abbcb-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="abbcb-101">Remove-AzBotService</span></span>

## <span data-ttu-id="abbcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="abbcb-102">SYNOPSIS</span></span>
<span data-ttu-id="abbcb-103">리소스 그룹에서 Bot Service를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="abbcb-104">구문</span><span class="sxs-lookup"><span data-stu-id="abbcb-104">SYNTAX</span></span>

### <span data-ttu-id="abbcb-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="abbcb-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="abbcb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="abbcb-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="abbcb-107">설명</span><span class="sxs-lookup"><span data-stu-id="abbcb-107">DESCRIPTION</span></span>
<span data-ttu-id="abbcb-108">리소스 그룹에서 Bot Service를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="abbcb-109">예제</span><span class="sxs-lookup"><span data-stu-id="abbcb-109">EXAMPLES</span></span>

### <span data-ttu-id="abbcb-110">예제 1: BotService By Name 및 ResourceGroupName 삭제</span><span class="sxs-lookup"><span data-stu-id="abbcb-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="abbcb-111">BotService By Name 및 ResourceGroupName 삭제</span><span class="sxs-lookup"><span data-stu-id="abbcb-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="abbcb-112">예제 2: InputObject로 BotService 삭제</span><span class="sxs-lookup"><span data-stu-id="abbcb-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="abbcb-113">InputObject로 BotService 삭제</span><span class="sxs-lookup"><span data-stu-id="abbcb-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="abbcb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="abbcb-114">PARAMETERS</span></span>

### <span data-ttu-id="abbcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="abbcb-115">-DefaultProfile</span></span>
<span data-ttu-id="abbcb-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="abbcb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="abbcb-117">-InputObject</span></span>
<span data-ttu-id="abbcb-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="abbcb-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="abbcb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="abbcb-119">-Name</span></span>
<span data-ttu-id="abbcb-120">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="abbcb-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="abbcb-121">-PassThru</span></span>
<span data-ttu-id="abbcb-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="abbcb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="abbcb-123">-ResourceGroupName</span></span>
<span data-ttu-id="abbcb-124">사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="abbcb-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="abbcb-125">-SubscriptionId</span></span>
<span data-ttu-id="abbcb-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="abbcb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="abbcb-127">-Confirm</span></span>
<span data-ttu-id="abbcb-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="abbcb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="abbcb-129">-WhatIf</span></span>
<span data-ttu-id="abbcb-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="abbcb-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="abbcb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="abbcb-132">CommonParameters</span></span>
<span data-ttu-id="abbcb-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="abbcb-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="abbcb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="abbcb-135">입력</span><span class="sxs-lookup"><span data-stu-id="abbcb-135">INPUTS</span></span>

### <span data-ttu-id="abbcb-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="abbcb-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="abbcb-137">출력</span><span class="sxs-lookup"><span data-stu-id="abbcb-137">OUTPUTS</span></span>

### <span data-ttu-id="abbcb-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="abbcb-138">System.Boolean</span></span>

## <span data-ttu-id="abbcb-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="abbcb-139">NOTES</span></span>

<span data-ttu-id="abbcb-140">별칭</span><span class="sxs-lookup"><span data-stu-id="abbcb-140">ALIASES</span></span>

<span data-ttu-id="abbcb-141">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="abbcb-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="abbcb-142">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="abbcb-143">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="abbcb-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="abbcb-144">INPUTOBJECT <IBotServiceIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="abbcb-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="abbcb-145">`[ChannelName <ChannelName?>]`: 채널 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="abbcb-146">`[ConnectionName <String>]`: 봇 서비스 연결 설정 리소스의 이름</span><span class="sxs-lookup"><span data-stu-id="abbcb-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="abbcb-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="abbcb-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="abbcb-148">`[ResourceGroupName <String>]`: 사용자 구독의 Bot 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="abbcb-149">`[ResourceName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="abbcb-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="abbcb-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="abbcb-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="abbcb-151">RELATED LINKS</span></span>

