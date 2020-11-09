---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 1c75bb4e8f94fadfb3b56c2fbb44889c5eaff458
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305060"
---
# <span data-ttu-id="f49f2-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="f49f2-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="f49f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f49f2-102">SYNOPSIS</span></span>
<span data-ttu-id="f49f2-103">작업 영역 vNetPeering 링을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f49f2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f49f2-104">SYNTAX</span></span>

### <span data-ttu-id="f49f2-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f49f2-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="f49f2-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f49f2-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f49f2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f49f2-107">DESCRIPTION</span></span>
<span data-ttu-id="f49f2-108">작업 영역 vNetPeering 링을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="f49f2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f49f2-109">EXAMPLES</span></span>

### <span data-ttu-id="f49f2-110">예제 1: 이름으로 databricks의 vnet 피어 링을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="f49f2-111">이 명령은 이름으로 databricks의 vnet 피어 링을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="f49f2-112">예제 2: databricks의 vnet 피어 링 제거 개체</span><span class="sxs-lookup"><span data-stu-id="f49f2-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="f49f2-113">이 명령은 databricks의 vnet 피어 링을 개체 별로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="f49f2-114">변수</span><span class="sxs-lookup"><span data-stu-id="f49f2-114">PARAMETERS</span></span>

### <span data-ttu-id="f49f2-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f49f2-115">-AsJob</span></span>
<span data-ttu-id="f49f2-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f49f2-116">Run the command as a job</span></span>

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

### <span data-ttu-id="f49f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f49f2-117">-DefaultProfile</span></span>
<span data-ttu-id="f49f2-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f49f2-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f49f2-119">-InputObject</span></span>
<span data-ttu-id="f49f2-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f49f2-121">-이름</span><span class="sxs-lookup"><span data-stu-id="f49f2-121">-Name</span></span>
<span data-ttu-id="f49f2-122">작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="f49f2-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f49f2-123">-NoWait</span></span>
<span data-ttu-id="f49f2-124">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="f49f2-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f49f2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f49f2-125">-PassThru</span></span>
<span data-ttu-id="f49f2-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f49f2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f49f2-127">-ResourceGroupName</span></span>
<span data-ttu-id="f49f2-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-128">The name of the resource group.</span></span>
<span data-ttu-id="f49f2-129">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="f49f2-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f49f2-130">-SubscriptionId</span></span>
<span data-ttu-id="f49f2-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="f49f2-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f49f2-132">-WorkspaceName</span></span>
<span data-ttu-id="f49f2-133">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="f49f2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f49f2-134">-Confirm</span></span>
<span data-ttu-id="f49f2-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f49f2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f49f2-136">-WhatIf</span></span>
<span data-ttu-id="f49f2-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f49f2-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f49f2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f49f2-139">CommonParameters</span></span>
<span data-ttu-id="f49f2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f49f2-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f49f2-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f49f2-142">입력</span><span class="sxs-lookup"><span data-stu-id="f49f2-142">INPUTS</span></span>

### <span data-ttu-id="f49f2-143">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="f49f2-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="f49f2-144">출력</span><span class="sxs-lookup"><span data-stu-id="f49f2-144">OUTPUTS</span></span>

### <span data-ttu-id="f49f2-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f49f2-145">System.Boolean</span></span>

## <span data-ttu-id="f49f2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f49f2-146">NOTES</span></span>

<span data-ttu-id="f49f2-147">별칭과</span><span class="sxs-lookup"><span data-stu-id="f49f2-147">ALIASES</span></span>

<span data-ttu-id="f49f2-148">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="f49f2-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="f49f2-149">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f49f2-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="f49f2-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="f49f2-151">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f49f2-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f49f2-152">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="f49f2-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f49f2-153">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="f49f2-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="f49f2-155">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="f49f2-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="f49f2-157">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f49f2-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="f49f2-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f49f2-158">RELATED LINKS</span></span>

