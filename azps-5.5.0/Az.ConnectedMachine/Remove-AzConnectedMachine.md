---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209912"
---
# <span data-ttu-id="5d97a-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="5d97a-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="5d97a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d97a-102">SYNOPSIS</span></span>
<span data-ttu-id="5d97a-103">Azure에서 하이브리드 컴퓨터 ID를 제거하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="5d97a-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d97a-104">SYNTAX</span></span>

### <span data-ttu-id="5d97a-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d97a-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d97a-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d97a-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d97a-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d97a-107">DESCRIPTION</span></span>
<span data-ttu-id="5d97a-108">Azure에서 하이브리드 컴퓨터 ID를 제거하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="5d97a-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d97a-109">EXAMPLES</span></span>

### <span data-ttu-id="5d97a-110">예제 1: 연결된 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="5d97a-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="5d97a-111">연결된 머신을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="5d97a-112">예제 2: 파이프라인을 통해 연결된 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="5d97a-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="5d97a-113">리소스 그룹의 모든 컴퓨터를 `contoso-connected-machines` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="5d97a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d97a-114">PARAMETERS</span></span>

### <span data-ttu-id="5d97a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d97a-115">-DefaultProfile</span></span>
<span data-ttu-id="5d97a-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d97a-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d97a-117">-InputObject</span></span>
<span data-ttu-id="5d97a-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5d97a-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d97a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5d97a-119">-Name</span></span>
<span data-ttu-id="5d97a-120">하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="5d97a-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d97a-121">-PassThru</span></span>
<span data-ttu-id="5d97a-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d97a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d97a-123">-ResourceGroupName</span></span>
<span data-ttu-id="5d97a-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="5d97a-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d97a-125">-SubscriptionId</span></span>
<span data-ttu-id="5d97a-126">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d97a-127">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d97a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d97a-128">-Confirm</span></span>
<span data-ttu-id="5d97a-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d97a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d97a-130">-WhatIf</span></span>
<span data-ttu-id="5d97a-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d97a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d97a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d97a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d97a-133">CommonParameters</span></span>
<span data-ttu-id="5d97a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d97a-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5d97a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d97a-136">입력</span><span class="sxs-lookup"><span data-stu-id="5d97a-136">INPUTS</span></span>

### <span data-ttu-id="5d97a-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span><span class="sxs-lookup"><span data-stu-id="5d97a-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="5d97a-138">출력</span><span class="sxs-lookup"><span data-stu-id="5d97a-138">OUTPUTS</span></span>

### <span data-ttu-id="5d97a-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d97a-139">System.Boolean</span></span>

## <span data-ttu-id="5d97a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d97a-140">NOTES</span></span>

<span data-ttu-id="5d97a-141">별칭</span><span class="sxs-lookup"><span data-stu-id="5d97a-141">ALIASES</span></span>

<span data-ttu-id="5d97a-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5d97a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d97a-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d97a-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d97a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d97a-145">INPUTOBJECT: <IConnectedMachineIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d97a-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d97a-146">`[ExtensionName <String>]`: 컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="5d97a-147">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5d97a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d97a-148">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="5d97a-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5d97a-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d97a-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="5d97a-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="5d97a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d97a-152">RELATED LINKS</span></span>

