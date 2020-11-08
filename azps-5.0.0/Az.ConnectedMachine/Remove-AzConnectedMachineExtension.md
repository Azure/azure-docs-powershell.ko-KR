---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/remove-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Remove-AzConnectedMachineExtension.md
ms.openlocfilehash: ee746fd2f9a35415e4efd3c2f8aaba803d182beb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218735"
---
# <span data-ttu-id="69b76-101">Remove-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="69b76-101">Remove-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="69b76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69b76-102">SYNOPSIS</span></span>
<span data-ttu-id="69b76-103">확장을 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-103">The operation to delete the extension.</span></span>

## <span data-ttu-id="69b76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69b76-104">SYNTAX</span></span>

### <span data-ttu-id="69b76-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="69b76-105">Delete (Default)</span></span>
```
Remove-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="69b76-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="69b76-106">DeleteViaIdentity</span></span>
```
Remove-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69b76-107">설명은</span><span class="sxs-lookup"><span data-stu-id="69b76-107">DESCRIPTION</span></span>
<span data-ttu-id="69b76-108">확장을 삭제 하는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-108">The operation to delete the extension.</span></span>

## <span data-ttu-id="69b76-109">예제의</span><span class="sxs-lookup"><span data-stu-id="69b76-109">EXAMPLES</span></span>

### <span data-ttu-id="69b76-110">예제 1: 컴퓨터 확장명 제거</span><span class="sxs-lookup"><span data-stu-id="69b76-110">Example 1: Remove a machine extension.</span></span>
```powershell
PS C:\> Remove-AzConnectedMachineExtension -MachineName myMachine -ResourceGroupName myRG -Name custom

```

<span data-ttu-id="69b76-111">컴퓨터에서 확장을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-111">Deletes the extension on the machine.</span></span>

### <span data-ttu-id="69b76-112">예제 2: 파이프라인을 통해 확장 제거</span><span class="sxs-lookup"><span data-stu-id="69b76-112">Example 2: Remove extension via the pipeline</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName myMachine | Remove-AzConnectedMachineExtension

```

<span data-ttu-id="69b76-113">지정 된 컴퓨터의 모든 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-113">Removes all extensions in the specified machine.</span></span>

## <span data-ttu-id="69b76-114">변수</span><span class="sxs-lookup"><span data-stu-id="69b76-114">PARAMETERS</span></span>

### <span data-ttu-id="69b76-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69b76-115">-AsJob</span></span>
<span data-ttu-id="69b76-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="69b76-116">Run the command as a job</span></span>

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

### <span data-ttu-id="69b76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69b76-117">-DefaultProfile</span></span>
<span data-ttu-id="69b76-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69b76-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69b76-119">-InputObject</span></span>
<span data-ttu-id="69b76-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="69b76-121">-MachineName</span><span class="sxs-lookup"><span data-stu-id="69b76-121">-MachineName</span></span>
<span data-ttu-id="69b76-122">확장명을 삭제 해야 하는 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-122">The name of the machine where the extension should be deleted.</span></span>

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

### <span data-ttu-id="69b76-123">-이름</span><span class="sxs-lookup"><span data-stu-id="69b76-123">-Name</span></span>
<span data-ttu-id="69b76-124">컴퓨터 확장의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-124">The name of the machine extension.</span></span>

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

### <span data-ttu-id="69b76-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69b76-125">-NoWait</span></span>
<span data-ttu-id="69b76-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="69b76-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69b76-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69b76-127">-PassThru</span></span>
<span data-ttu-id="69b76-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="69b76-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69b76-129">-ResourceGroupName</span></span>
<span data-ttu-id="69b76-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="69b76-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69b76-131">-SubscriptionId</span></span>
<span data-ttu-id="69b76-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-132">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="69b76-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="69b76-134">-확인</span><span class="sxs-lookup"><span data-stu-id="69b76-134">-Confirm</span></span>
<span data-ttu-id="69b76-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69b76-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69b76-136">-WhatIf</span></span>
<span data-ttu-id="69b76-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69b76-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69b76-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69b76-139">CommonParameters</span></span>
<span data-ttu-id="69b76-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69b76-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b76-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69b76-142">입력</span><span class="sxs-lookup"><span data-stu-id="69b76-142">INPUTS</span></span>

### <span data-ttu-id="69b76-143">ConnectedMachine. IConnectedMachineIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="69b76-143">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity</span></span>

## <span data-ttu-id="69b76-144">출력</span><span class="sxs-lookup"><span data-stu-id="69b76-144">OUTPUTS</span></span>

### <span data-ttu-id="69b76-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="69b76-145">System.Boolean</span></span>

## <span data-ttu-id="69b76-146">상속자</span><span class="sxs-lookup"><span data-stu-id="69b76-146">NOTES</span></span>

<span data-ttu-id="69b76-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="69b76-147">ALIASES</span></span>

<span data-ttu-id="69b76-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="69b76-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="69b76-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="69b76-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="69b76-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="69b76-151">INPUTOBJECT <IConnectedMachineIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="69b76-151">INPUTOBJECT <IConnectedMachineIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="69b76-152">`[ExtensionName <String>]`: 컴퓨터 확장명의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-152">`[ExtensionName <String>]`: The name of the machine extension.</span></span>
  - <span data-ttu-id="69b76-153">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="69b76-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="69b76-154">`[Name <String>]`: 하이브리드 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-154">`[Name <String>]`: The name of the hybrid machine.</span></span>
  - <span data-ttu-id="69b76-155">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="69b76-156">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="69b76-157">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="69b76-157">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="69b76-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69b76-158">RELATED LINKS</span></span>

