---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachine
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachine.md
ms.openlocfilehash: e8988f5dd6e2e37cc98c31ceab244693eae1941e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218738"
---
# <span data-ttu-id="58201-101">Remove-AzConnectedMachine</span><span class="sxs-lookup"><span data-stu-id="58201-101">Remove-AzConnectedMachine</span></span>

## <span data-ttu-id="58201-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58201-102">SYNOPSIS</span></span>
<span data-ttu-id="58201-103">Azure에서 하이브리드 컴퓨터 id를 제거 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-103">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="58201-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58201-104">SYNTAX</span></span>

### <span data-ttu-id="58201-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="58201-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachine -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="58201-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="58201-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachine -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="58201-107">설명은</span><span class="sxs-lookup"><span data-stu-id="58201-107">DESCRIPTION</span></span>
<span data-ttu-id="58201-108">Azure에서 하이브리드 컴퓨터 id를 제거 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-108">The operation to remove a hybrid machine identity in Azure.</span></span>

## <span data-ttu-id="58201-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58201-109">EXAMPLES</span></span>

### <span data-ttu-id="58201-110">예제 1: 연결 된 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="58201-110">Example 1: Remove a connected machine</span></span>
```powershell
PS C:\> Remove-AzConnectedMachine -Name myMachine -ResourceGroupName myRG

```

<span data-ttu-id="58201-111">연결 된 컴퓨터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-111">Deletes the connected machine.</span></span>

### <span data-ttu-id="58201-112">예제 2: 파이프라인을 통해 연결 된 컴퓨터 제거</span><span class="sxs-lookup"><span data-stu-id="58201-112">Example 2: Remove connected machines via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachine -ResourceGroupName contoso-connected-machines | Remove-AzConnectedMachine

```

<span data-ttu-id="58201-113">리소스 그룹의 모든 컴퓨터를 제거 `contoso-connected-machines` 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-113">Removes all machines in the `contoso-connected-machines` resource group.</span></span>

## <span data-ttu-id="58201-114">변수</span><span class="sxs-lookup"><span data-stu-id="58201-114">PARAMETERS</span></span>

### <span data-ttu-id="58201-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58201-115">-DefaultProfile</span></span>
<span data-ttu-id="58201-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58201-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58201-117">-InputObject</span></span>
<span data-ttu-id="58201-118">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="58201-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="58201-119">-이름</span><span class="sxs-lookup"><span data-stu-id="58201-119">-Name</span></span>
<span data-ttu-id="58201-120">하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-120">The name of the hybrid machine.</span></span>

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

### <span data-ttu-id="58201-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58201-121">-PassThru</span></span>
<span data-ttu-id="58201-122">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="58201-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58201-123">-ResourceGroupName</span></span>
<span data-ttu-id="58201-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="58201-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58201-125">-SubscriptionId</span></span>
<span data-ttu-id="58201-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="58201-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="58201-128">-확인</span><span class="sxs-lookup"><span data-stu-id="58201-128">-Confirm</span></span>
<span data-ttu-id="58201-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58201-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58201-130">-WhatIf</span></span>
<span data-ttu-id="58201-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58201-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58201-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58201-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58201-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58201-133">CommonParameters</span></span>
<span data-ttu-id="58201-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58201-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58201-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58201-136">입력</span><span class="sxs-lookup"><span data-stu-id="58201-136">INPUTS</span></span>

### <span data-ttu-id="58201-137">ConnectedMachine. IConnectedMachineIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="58201-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="58201-138">출력</span><span class="sxs-lookup"><span data-stu-id="58201-138">OUTPUTS</span></span>

### <span data-ttu-id="58201-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="58201-139">System.Boolean</span></span>

## <span data-ttu-id="58201-140">상속자</span><span class="sxs-lookup"><span data-stu-id="58201-140">NOTES</span></span>

<span data-ttu-id="58201-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="58201-141">ALIASES</span></span>

<span data-ttu-id="58201-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="58201-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="58201-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="58201-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="58201-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="58201-145">INPUTOBJECT <IConnectedMachineIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="58201-145">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="58201-146">`[ExtensionName <String>]`: 컴퓨터 확장명의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-146">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="58201-147">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="58201-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="58201-148">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-148">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="58201-149">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-149">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="58201-150">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="58201-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="58201-151">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58201-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="58201-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58201-152">RELATED LINKS</span></span>

