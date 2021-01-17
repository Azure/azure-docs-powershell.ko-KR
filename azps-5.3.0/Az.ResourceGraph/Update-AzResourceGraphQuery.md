---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/update-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Update-AzResourceGraphQuery.md
ms.openlocfilehash: 6ae44183a368babb43a93063518dfbf4f3d15e18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377896"
---
# <span data-ttu-id="5b4f8-101">Update-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="5b4f8-101">Update-AzResourceGraphQuery</span></span>

## <span data-ttu-id="5b4f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b4f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5b4f8-103">이미 추가된 그래프 쿼리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-103">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="5b4f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b4f8-104">SYNTAX</span></span>

### <span data-ttu-id="5b4f8-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5b4f8-105">UpdateExpanded (Default)</span></span>
```
Update-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-File <String>] [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5b4f8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5b4f8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-Description <String>] [-File <String>]
 [-Query <String>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5b4f8-107">설명</span><span class="sxs-lookup"><span data-stu-id="5b4f8-107">DESCRIPTION</span></span>
<span data-ttu-id="5b4f8-108">이미 추가된 그래프 쿼리를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-108">Updates a graph query that has already been added.</span></span>

## <span data-ttu-id="5b4f8-109">예제</span><span class="sxs-lookup"><span data-stu-id="5b4f8-109">EXAMPLES</span></span>

### <span data-ttu-id="5b4f8-110">예제 1: 이름에 따라 매개 변수 쿼리 및 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b4f8-110">Example 1: Update the parameter query and tag by name</span></span>
```powershell
PS C:\>  Update-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 -Query "project id, name, type, location, tags"  -Tag @{'key1'=1;'key2'=2}

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="5b4f8-111">이 명령은 매개 변수 쿼리 및 태그를 이름으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-111">This command updates the parameter query and tag by name.</span></span>

### <span data-ttu-id="5b4f8-112">예제 2: 개체에 따라 매개 변수 파일 업데이트</span><span class="sxs-lookup"><span data-stu-id="5b4f8-112">Example 2: Update the parameter file by object</span></span>
```powershell
PS C:\> $query =  Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t05 
PS C:\> Update-AzResourceGraphQuery -InputObject $query -File './Query.kql'

Location Name      Type
-------- ----      ----
     global   query-t05 microsoft.resourcegraph/queries
```

<span data-ttu-id="5b4f8-113">이 명령은 개체에 따라 매개 변수 쿼리 및 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-113">This command updates the parameter query and tag by object.</span></span>

## <span data-ttu-id="5b4f8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b4f8-114">PARAMETERS</span></span>

### <span data-ttu-id="5b4f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b4f8-115">-DefaultProfile</span></span>
<span data-ttu-id="5b4f8-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b4f8-117">-Description</span><span class="sxs-lookup"><span data-stu-id="5b4f8-117">-Description</span></span>
<span data-ttu-id="5b4f8-118">그래프 쿼리에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-118">The description of a graph query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-119">-File</span><span class="sxs-lookup"><span data-stu-id="5b4f8-119">-File</span></span>
<span data-ttu-id="5b4f8-120">파일의 콘텐츠가 쿼리 매개 변수에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-120">The content of the file will be passed to the query parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5b4f8-121">-InputObject</span></span>
<span data-ttu-id="5b4f8-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5b4f8-123">-Name</span></span>
<span data-ttu-id="5b4f8-124">그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-124">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-125">-Query</span><span class="sxs-lookup"><span data-stu-id="5b4f8-125">-Query</span></span>
<span data-ttu-id="5b4f8-126">그래프가 될 KQL 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-126">KQL query that will be graph.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b4f8-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b4f8-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-128">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5b4f8-129">-SubscriptionId</span></span>
<span data-ttu-id="5b4f8-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-130">The Azure subscription Id.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="5b4f8-131">-Tag</span></span>
<span data-ttu-id="5b4f8-132">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="5b4f8-132">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b4f8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b4f8-133">-Confirm</span></span>
<span data-ttu-id="5b4f8-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b4f8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b4f8-135">-WhatIf</span></span>
<span data-ttu-id="5b4f8-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5b4f8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b4f8-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b4f8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b4f8-138">CommonParameters</span></span>
<span data-ttu-id="5b4f8-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b4f8-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b4f8-141">입력</span><span class="sxs-lookup"><span data-stu-id="5b4f8-141">INPUTS</span></span>

### <span data-ttu-id="5b4f8-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="5b4f8-142">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="5b4f8-143">출력</span><span class="sxs-lookup"><span data-stu-id="5b4f8-143">OUTPUTS</span></span>

### <span data-ttu-id="5b4f8-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="5b4f8-144">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="5b4f8-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b4f8-145">NOTES</span></span>

<span data-ttu-id="5b4f8-146">별칭</span><span class="sxs-lookup"><span data-stu-id="5b4f8-146">ALIASES</span></span>

<span data-ttu-id="5b4f8-147">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5b4f8-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5b4f8-148">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5b4f8-149">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5b4f8-150">INPUTOBJECT: <IResourceGraphIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b4f8-150">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5b4f8-151">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5b4f8-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5b4f8-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="5b4f8-153">`[ResourceName <String>]`: 그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-153">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="5b4f8-154">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5b4f8-154">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="5b4f8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b4f8-155">RELATED LINKS</span></span>

