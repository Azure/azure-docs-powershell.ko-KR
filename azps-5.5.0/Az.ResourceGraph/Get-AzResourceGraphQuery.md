---
external help file: ''
Module Name: Az.ResourceGraph
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcegraph/get-azresourcegraphquery
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceGraph/ResourceGraph/help/Get-AzResourceGraphQuery.md
ms.openlocfilehash: 6d7dbb9acbcc03f266d698d1f9d8ce89f320d04b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176420"
---
# <span data-ttu-id="34e10-101">Get-AzResourceGraphQuery</span><span class="sxs-lookup"><span data-stu-id="34e10-101">Get-AzResourceGraphQuery</span></span>

## <span data-ttu-id="34e10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34e10-102">SYNOPSIS</span></span>
<span data-ttu-id="34e10-103">resourceName으로 단일 그래프 쿼리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-103">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="34e10-104">구문</span><span class="sxs-lookup"><span data-stu-id="34e10-104">SYNTAX</span></span>

### <span data-ttu-id="34e10-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="34e10-105">List (Default)</span></span>
```
Get-AzResourceGraphQuery -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="34e10-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="34e10-106">Get</span></span>
```
Get-AzResourceGraphQuery -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="34e10-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="34e10-107">GetViaIdentity</span></span>
```
Get-AzResourceGraphQuery -InputObject <IResourceGraphIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="34e10-108">설명</span><span class="sxs-lookup"><span data-stu-id="34e10-108">DESCRIPTION</span></span>
<span data-ttu-id="34e10-109">resourceName으로 단일 그래프 쿼리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-109">Get a single graph query by its resourceName.</span></span>

## <span data-ttu-id="34e10-110">예제</span><span class="sxs-lookup"><span data-stu-id="34e10-110">EXAMPLES</span></span>

### <span data-ttu-id="34e10-111">예제 1: 리소스 그룹에서 모든 리소스 그래프 쿼리를 얻게</span><span class="sxs-lookup"><span data-stu-id="34e10-111">Example 1: Get all resource graph query under a resource group</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="34e10-112">이 명령은 리소스 그룹에서 모든 리소스 그래프 쿼리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-112">This command gets all resource graph query under a resource group.</span></span>

### <span data-ttu-id="34e10-113">예제 2: 이름으로 리소스 그래프 쿼리를 구합니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-113">Example 2: Get a resource graph query by name</span></span>
```powershell
PS C:\> Get-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name SharedQuery-t01

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="34e10-114">이 명령은 이름으로 리소스 그래프 쿼리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-114">This command gets a resource graph query by name.</span></span>

### <span data-ttu-id="34e10-115">예제 2: objecy를 통해 리소스 그래프 쿼리를 구합니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-115">Example 2: Get a resource graph query by objecy</span></span>
```powershell
PS C:\> $query = New-AzResourceGraphQuery -ResourceGroupName azure-rg-test -Name query-t03 -Location 'global' -Query 'project id, name, type, location' -Description 'test'
PS C:\> Get-AzResourceGraphQuery -InputObject $query

Location Name            Type
-------- ----            ----
     global   SharedQuery-t01 microsoft.resourcegraph/queries
```

<span data-ttu-id="34e10-116">이 명령은 개체에 따라 리소스 그래프 쿼리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-116">This command gets a resource graph query by object.</span></span>

## <span data-ttu-id="34e10-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34e10-117">PARAMETERS</span></span>

### <span data-ttu-id="34e10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34e10-118">-DefaultProfile</span></span>
<span data-ttu-id="34e10-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34e10-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="34e10-120">-InputObject</span></span>
<span data-ttu-id="34e10-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="34e10-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="34e10-122">-Name</span><span class="sxs-lookup"><span data-stu-id="34e10-122">-Name</span></span>
<span data-ttu-id="34e10-123">그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-123">The name of the Graph Query resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34e10-124">-ResourceGroupName</span></span>
<span data-ttu-id="34e10-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e10-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="34e10-126">-SubscriptionId</span></span>
<span data-ttu-id="34e10-127">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-127">The Azure subscription Id.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34e10-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34e10-128">CommonParameters</span></span>
<span data-ttu-id="34e10-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34e10-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34e10-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34e10-131">입력</span><span class="sxs-lookup"><span data-stu-id="34e10-131">INPUTS</span></span>

### <span data-ttu-id="34e10-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span><span class="sxs-lookup"><span data-stu-id="34e10-132">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.IResourceGraphIdentity</span></span>

## <span data-ttu-id="34e10-133">출력</span><span class="sxs-lookup"><span data-stu-id="34e10-133">OUTPUTS</span></span>

### <span data-ttu-id="34e10-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span><span class="sxs-lookup"><span data-stu-id="34e10-134">Microsoft.Azure.PowerShell.Cmdlets.ResourceGraph.Models.Api20180901Preview.IGraphQueryResource</span></span>

## <span data-ttu-id="34e10-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34e10-135">NOTES</span></span>

<span data-ttu-id="34e10-136">별칭</span><span class="sxs-lookup"><span data-stu-id="34e10-136">ALIASES</span></span>

<span data-ttu-id="34e10-137">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="34e10-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="34e10-138">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="34e10-139">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="34e10-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="34e10-140">INPUTOBJECT: <IResourceGraphIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="34e10-140">INPUTOBJECT <IResourceGraphIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="34e10-141">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="34e10-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="34e10-142">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-142">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="34e10-143">`[ResourceName <String>]`: 그래프 쿼리 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-143">`[ResourceName <String>]`: The name of the Graph Query resource.</span></span>
  - <span data-ttu-id="34e10-144">`[SubscriptionId <String>]`: Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="34e10-144">`[SubscriptionId <String>]`: The Azure subscription Id.</span></span>

## <span data-ttu-id="34e10-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34e10-145">RELATED LINKS</span></span>

