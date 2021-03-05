---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/remove-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Remove-AzDatabricksVNetPeering.md
ms.openlocfilehash: 986bea9de45ea8a628cea8eda4d8a63ec74d46fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980763"
---
# <span data-ttu-id="02fcb-101">Remove-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="02fcb-101">Remove-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="02fcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02fcb-102">SYNOPSIS</span></span>
<span data-ttu-id="02fcb-103">작업 영역 vNetPeering을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-103">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="02fcb-104">구문</span><span class="sxs-lookup"><span data-stu-id="02fcb-104">SYNTAX</span></span>

### <span data-ttu-id="02fcb-105">삭제(기본값)</span><span class="sxs-lookup"><span data-stu-id="02fcb-105">Delete (Default)</span></span>
```
Remove-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="02fcb-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="02fcb-106">DeleteViaIdentity</span></span>
```
Remove-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02fcb-107">설명</span><span class="sxs-lookup"><span data-stu-id="02fcb-107">DESCRIPTION</span></span>
<span data-ttu-id="02fcb-108">작업 영역 vNetPeering을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-108">Deletes the workspace vNetPeering.</span></span>

## <span data-ttu-id="02fcb-109">예제</span><span class="sxs-lookup"><span data-stu-id="02fcb-109">EXAMPLES</span></span>

### <span data-ttu-id="02fcb-110">예제 1: 이름에 따라 databricks의 vnet 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="02fcb-110">Example 1: Remove a vnet peering of databricks by name</span></span>
```powershell
PS C:\> Remove-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01

```

<span data-ttu-id="02fcb-111">이 명령은 이름으로 databricks의 vnet 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-111">This command removes a vnet peering of databricks by name</span></span>

### <span data-ttu-id="02fcb-112">예제 2: 개체에 따라 databricks의 vnet 피어링 제거</span><span class="sxs-lookup"><span data-stu-id="02fcb-112">Example 2: Remove a vnet peering of databricks by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01 | Remove-AzDatabricksVNetPeering

```

<span data-ttu-id="02fcb-113">이 명령은 개체에 따라 databricks의 vnet 피어링을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-113">This command removes a vnet peering of databricks by object</span></span>

## <span data-ttu-id="02fcb-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="02fcb-114">PARAMETERS</span></span>

### <span data-ttu-id="02fcb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02fcb-115">-AsJob</span></span>
<span data-ttu-id="02fcb-116">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="02fcb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02fcb-117">-DefaultProfile</span></span>
<span data-ttu-id="02fcb-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02fcb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02fcb-119">-InputObject</span></span>
<span data-ttu-id="02fcb-120">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="02fcb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="02fcb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="02fcb-121">-Name</span></span>
<span data-ttu-id="02fcb-122">작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-122">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="02fcb-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="02fcb-123">-NoWait</span></span>
<span data-ttu-id="02fcb-124">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="02fcb-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02fcb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02fcb-125">-PassThru</span></span>
<span data-ttu-id="02fcb-126">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="02fcb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02fcb-127">-ResourceGroupName</span></span>
<span data-ttu-id="02fcb-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-128">The name of the resource group.</span></span>
<span data-ttu-id="02fcb-129">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="02fcb-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="02fcb-130">-SubscriptionId</span></span>
<span data-ttu-id="02fcb-131">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="02fcb-132">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="02fcb-132">-WorkspaceName</span></span>
<span data-ttu-id="02fcb-133">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-133">The name of the workspace.</span></span>

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

### <span data-ttu-id="02fcb-134">-확인</span><span class="sxs-lookup"><span data-stu-id="02fcb-134">-Confirm</span></span>
<span data-ttu-id="02fcb-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02fcb-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02fcb-136">-WhatIf</span></span>
<span data-ttu-id="02fcb-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02fcb-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02fcb-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02fcb-139">CommonParameters</span></span>
<span data-ttu-id="02fcb-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02fcb-141">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02fcb-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02fcb-142">입력</span><span class="sxs-lookup"><span data-stu-id="02fcb-142">INPUTS</span></span>

### <span data-ttu-id="02fcb-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="02fcb-143">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="02fcb-144">출력</span><span class="sxs-lookup"><span data-stu-id="02fcb-144">OUTPUTS</span></span>

### <span data-ttu-id="02fcb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="02fcb-145">System.Boolean</span></span>

## <span data-ttu-id="02fcb-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="02fcb-146">NOTES</span></span>

<span data-ttu-id="02fcb-147">별칭</span><span class="sxs-lookup"><span data-stu-id="02fcb-147">ALIASES</span></span>

<span data-ttu-id="02fcb-148">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="02fcb-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02fcb-149">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02fcb-150">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02fcb-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02fcb-151">INPUTOBJECT <IDatabricksIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="02fcb-151">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="02fcb-152">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="02fcb-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="02fcb-153">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-153">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="02fcb-154">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-154">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="02fcb-155">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-155">The name is case insensitive.</span></span>
  - <span data-ttu-id="02fcb-156">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="02fcb-157">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02fcb-157">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="02fcb-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02fcb-158">RELATED LINKS</span></span>

