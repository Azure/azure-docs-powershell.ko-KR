---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/remove-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Remove-AzResourceGraphQuery.md
ms.openlocfilehash: 3fc5c493f94b6da371a4249479e397ea6e2362f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377917"
---
# <span data-ttu-id="44dad-101">Remove-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="44dad-101">Remove-AzResourceGraphQuery</span></span>

## <span data-ttu-id="44dad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44dad-102">SYNOPSIS</span></span>
<span data-ttu-id="44dad-103">그래프 쿼리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-103">Delete a graph query.</span></span>

## <span data-ttu-id="44dad-104">구문</span><span class="sxs-lookup"><span data-stu-id="44dad-104">SYNTAX</span></span>

### <span data-ttu-id="44dad-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="44dad-105">Delete (Default)</span></span>
```
Remove-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44dad-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44dad-106">DeleteViaIdentity</span></span>
```
Remove-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44dad-107">설명</span><span class="sxs-lookup"><span data-stu-id="44dad-107">DESCRIPTION</span></span>
<span data-ttu-id="44dad-108">그래프 쿼리를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-108">Delete a graph query.</span></span>

## <span data-ttu-id="44dad-109">예제</span><span class="sxs-lookup"><span data-stu-id="44dad-109">EXAMPLES</span></span>

### <span data-ttu-id="44dad-110">예제 1: 이름으로 리소스 그래프 쿼리 제거</span><span class="sxs-lookup"><span data-stu-id="44dad-110">Example 1: Remove a resource graph query by name</span></span>
```powershell
PS C:\> Remove-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03

```

<span data-ttu-id="44dad-111">이 명령은 이름으로 리소스 그래프 쿼리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-111">This command removes a resource graph query by name.</span></span>

### <span data-ttu-id="44dad-112">예제 2: 개체에 따라 리소스 그래프 쿼리 제거</span><span class="sxs-lookup"><span data-stu-id="44dad-112">Example 2: Remove a resource graph query by object</span></span>
```powershell
PS C:\> $query = Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t02
PS C:\> Remove-AzResourceGraphQuery -InputObject $query 

```

<span data-ttu-id="44dad-113">이 명령은 개체에 따라 리소스 그래프 쿼리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-113">This command removes a resource graph query by object.</span></span>

## <span data-ttu-id="44dad-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44dad-114">PARAMETERS</span></span>

### <span data-ttu-id="44dad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44dad-115">-DefaultProfile</span></span>
<span data-ttu-id="44dad-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44dad-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44dad-117">-InputObject</span></span>
<span data-ttu-id="44dad-118">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="44dad-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44dad-119">-Name</span><span class="sxs-lookup"><span data-stu-id="44dad-119">-Name</span></span>
<span data-ttu-id="44dad-120">그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-120">The name of the Graph Query resource.</span></span>

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

### <span data-ttu-id="44dad-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44dad-121">-PassThru</span></span>
<span data-ttu-id="44dad-122">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="44dad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44dad-123">-ResourceGroupName</span></span>
<span data-ttu-id="44dad-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="44dad-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44dad-125">-SubscriptionId</span></span>
<span data-ttu-id="44dad-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-126">The Azure subscription Id.</span></span>

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

### <span data-ttu-id="44dad-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44dad-127">-Confirm</span></span>
<span data-ttu-id="44dad-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44dad-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44dad-129">-WhatIf</span></span>
<span data-ttu-id="44dad-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="44dad-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44dad-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44dad-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44dad-132">CommonParameters</span></span>
<span data-ttu-id="44dad-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44dad-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44dad-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44dad-135">입력</span><span class="sxs-lookup"><span data-stu-id="44dad-135">INPUTS</span></span>

### <span data-ttu-id="44dad-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="44dad-136">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="44dad-137">출력</span><span class="sxs-lookup"><span data-stu-id="44dad-137">OUTPUTS</span></span>

### <span data-ttu-id="44dad-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44dad-138">System.Boolean</span></span>

## <span data-ttu-id="44dad-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44dad-139">NOTES</span></span>

<span data-ttu-id="44dad-140">별칭</span><span class="sxs-lookup"><span data-stu-id="44dad-140">ALIASES</span></span>

<span data-ttu-id="44dad-141">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="44dad-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44dad-142">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44dad-143">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44dad-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44dad-144">INPUTOBJECT: <IResourceGraphIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="44dad-144">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44dad-145">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="44dad-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44dad-146">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-146">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="44dad-147">`[ResourceName <String>]`: 그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-147">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="44dad-148">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="44dad-148">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="44dad-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44dad-149">RELATED LINKS</span></span>

