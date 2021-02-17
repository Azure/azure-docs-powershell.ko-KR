---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209904"
---
# <span data-ttu-id="bec99-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="bec99-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="bec99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bec99-102">SYNOPSIS</span></span>
<span data-ttu-id="bec99-103">확장을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="bec99-104">구문</span><span class="sxs-lookup"><span data-stu-id="bec99-104">SYNTAX</span></span>

### <span data-ttu-id="bec99-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="bec99-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="bec99-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bec99-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="bec99-107">설명</span><span class="sxs-lookup"><span data-stu-id="bec99-107">DESCRIPTION</span></span>
<span data-ttu-id="bec99-108">확장을 삭제하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="bec99-109">예제</span><span class="sxs-lookup"><span data-stu-id="bec99-109">EXAMPLES</span></span>

### <span data-ttu-id="bec99-110">예제 1: 컴퓨터 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="bec99-111">머신에서 확장을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="bec99-112">예제 2: 파이프라인을 통해 확장 제거</span><span class="sxs-lookup"><span data-stu-id="bec99-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="bec99-113">지정된 컴퓨터의 모든 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="bec99-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bec99-114">PARAMETERS</span></span>

### <span data-ttu-id="bec99-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bec99-115">-AsJob</span></span>
<span data-ttu-id="bec99-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="bec99-116">Run the command as a job</span></span>

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

### <span data-ttu-id="bec99-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec99-117">-DefaultProfile</span></span>
<span data-ttu-id="bec99-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec99-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bec99-119">-InputObject</span></span>
<span data-ttu-id="bec99-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="bec99-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bec99-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="bec99-121">-MachineName</span></span>
<span data-ttu-id="bec99-122">확장을 삭제해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="bec99-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bec99-123">-Name</span></span>
<span data-ttu-id="bec99-124">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="bec99-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bec99-125">-NoWait</span></span>
<span data-ttu-id="bec99-126">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="bec99-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="bec99-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bec99-127">-PassThru</span></span>
<span data-ttu-id="bec99-128">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="bec99-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec99-129">-ResourceGroupName</span></span>
<span data-ttu-id="bec99-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="bec99-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bec99-131">-SubscriptionId</span></span>
<span data-ttu-id="bec99-132">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="bec99-133">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="bec99-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bec99-134">-Confirm</span></span>
<span data-ttu-id="bec99-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bec99-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bec99-136">-WhatIf</span></span>
<span data-ttu-id="bec99-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bec99-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bec99-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bec99-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec99-139">CommonParameters</span></span>
<span data-ttu-id="bec99-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec99-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bec99-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec99-142">입력</span><span class="sxs-lookup"><span data-stu-id="bec99-142">INPUTS</span></span>

### <span data-ttu-id="bec99-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="bec99-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="bec99-144">출력</span><span class="sxs-lookup"><span data-stu-id="bec99-144">OUTPUTS</span></span>

### <span data-ttu-id="bec99-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bec99-145">System.Boolean</span></span>

## <span data-ttu-id="bec99-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bec99-146">NOTES</span></span>

<span data-ttu-id="bec99-147">별칭</span><span class="sxs-lookup"><span data-stu-id="bec99-147">ALIASES</span></span>

<span data-ttu-id="bec99-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bec99-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bec99-149">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bec99-150">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bec99-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bec99-151">INPUTOBJECT: <IConnectedMachineIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bec99-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bec99-152">`[ExtensionName <String>]`: 컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="bec99-153">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="bec99-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bec99-154">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="bec99-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="bec99-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="bec99-157">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="bec99-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="bec99-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bec99-158">RELATED LINKS</span></span>

