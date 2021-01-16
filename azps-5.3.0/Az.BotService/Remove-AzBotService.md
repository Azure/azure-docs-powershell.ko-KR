---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/remove-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Remove-AzBotService.md
ms.openlocfilehash: ef75ec3e48a68bffce7c5b281f542bd2e3dba9d9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493996"
---
# <span data-ttu-id="32805-101">Remove-AzBotService</span><span class="sxs-lookup"><span data-stu-id="32805-101">Remove-AzBotService</span></span>

## <span data-ttu-id="32805-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32805-102">SYNOPSIS</span></span>
<span data-ttu-id="32805-103">리소스 그룹에서 Bot Service를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="32805-103">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="32805-104">구문</span><span class="sxs-lookup"><span data-stu-id="32805-104">SYNTAX</span></span>

### <span data-ttu-id="32805-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="32805-105">Delete (Default)</span></span>
```
Remove-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32805-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="32805-106">DeleteViaIdentity</span></span>
```
Remove-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32805-107">설명</span><span class="sxs-lookup"><span data-stu-id="32805-107">DESCRIPTION</span></span>
<span data-ttu-id="32805-108">리소스 그룹에서 Bot Service를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="32805-108">Deletes a Bot Service from the resource group.</span></span>

## <span data-ttu-id="32805-109">예제</span><span class="sxs-lookup"><span data-stu-id="32805-109">EXAMPLES</span></span>

### <span data-ttu-id="32805-110">예제 1: 이름 및 ResourceGroupName으로 BotService 삭제</span><span class="sxs-lookup"><span data-stu-id="32805-110">Example 1: Delete the BotService By Name and ResourceGroupName</span></span>
```powershell
PS C:\> Remove-AzBotService -Name youri-bot -ResourceGroupName youriBotTest

```

<span data-ttu-id="32805-111">BotService By Name 및 ResourceGroupName 삭제</span><span class="sxs-lookup"><span data-stu-id="32805-111">Delete the BotService By Name and ResourceGroupName</span></span>

### <span data-ttu-id="32805-112">예제 2: InputObject로 BotService 삭제</span><span class="sxs-lookup"><span data-stu-id="32805-112">Example 2: Delete the BotService By InputObject</span></span>
```powershell
PS C:\> $getservice = Get-AzBotService -Name youriechobottest -ResourceGroupName youriBotTest
Remove-AzBotService -InputObject $getservice

```

<span data-ttu-id="32805-113">InputObject로 BotService 삭제</span><span class="sxs-lookup"><span data-stu-id="32805-113">Delete the BotService By InputObject</span></span>

## <span data-ttu-id="32805-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32805-114">PARAMETERS</span></span>

### <span data-ttu-id="32805-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32805-115">-DefaultProfile</span></span>
<span data-ttu-id="32805-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32805-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32805-117">-InputObject</span></span>
<span data-ttu-id="32805-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="32805-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32805-119">-Name</span><span class="sxs-lookup"><span data-stu-id="32805-119">-Name</span></span>
<span data-ttu-id="32805-120">봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-120">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="32805-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32805-121">-PassThru</span></span>
<span data-ttu-id="32805-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="32805-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="32805-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32805-123">-ResourceGroupName</span></span>
<span data-ttu-id="32805-124">사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-124">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="32805-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="32805-125">-SubscriptionId</span></span>
<span data-ttu-id="32805-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="32805-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32805-127">-Confirm</span></span>
<span data-ttu-id="32805-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32805-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32805-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32805-129">-WhatIf</span></span>
<span data-ttu-id="32805-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32805-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32805-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32805-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32805-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32805-132">CommonParameters</span></span>
<span data-ttu-id="32805-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32805-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32805-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="32805-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32805-135">입력</span><span class="sxs-lookup"><span data-stu-id="32805-135">INPUTS</span></span>

### <span data-ttu-id="32805-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="32805-136">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="32805-137">출력</span><span class="sxs-lookup"><span data-stu-id="32805-137">OUTPUTS</span></span>

### <span data-ttu-id="32805-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="32805-138">System.Boolean</span></span>

## <span data-ttu-id="32805-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32805-139">NOTES</span></span>

<span data-ttu-id="32805-140">별칭</span><span class="sxs-lookup"><span data-stu-id="32805-140">ALIASES</span></span>

<span data-ttu-id="32805-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="32805-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32805-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="32805-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32805-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32805-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32805-144">INPUTOBJECT: <IBotServiceIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="32805-144">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32805-145">`[ChannelName <ChannelName?>]`: 채널 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-145">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="32805-146">`[ConnectionName <String>]`: Bot Service 연결 설정 리소스의 이름</span><span class="sxs-lookup"><span data-stu-id="32805-146">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="32805-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="32805-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32805-148">`[ResourceGroupName <String>]`: 사용자 구독의 봇 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-148">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="32805-149">`[ResourceName <String>]`: 봇 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-149">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="32805-150">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="32805-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="32805-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32805-151">RELATED LINKS</span></span>

