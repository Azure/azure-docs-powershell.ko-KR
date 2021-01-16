---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334029"
---
# <span data-ttu-id="34f4c-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34f4c-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="34f4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34f4c-102">SYNOPSIS</span></span>
<span data-ttu-id="34f4c-103">Synapse Analytics 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="34f4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="34f4c-104">SYNTAX</span></span>

### <span data-ttu-id="34f4c-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="34f4c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34f4c-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34f4c-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34f4c-107">설명</span><span class="sxs-lookup"><span data-stu-id="34f4c-107">DESCRIPTION</span></span>
<span data-ttu-id="34f4c-108">**Get-AzSynapseWorkspace** cmdlet은 Azure Synapse Analytics 작업 영역 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="34f4c-109">예제</span><span class="sxs-lookup"><span data-stu-id="34f4c-109">EXAMPLES</span></span>

### <span data-ttu-id="34f4c-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="34f4c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="34f4c-111">이 명령은 현재 구독에서 모든 Azure Synapse Analytics 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="34f4c-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="34f4c-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="34f4c-113">이 명령은 현재 구독에서 모든 Azure Synapse Analytics 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="34f4c-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="34f4c-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="34f4c-115">이 명령은 지정된 이름으로 Azure Synapse Analytics 작업 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="34f4c-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="34f4c-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="34f4c-117">이 명령은 지정된 리소스 ID를 사용하여 Azure Synapse Analytics 작업 영역이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="34f4c-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34f4c-118">PARAMETERS</span></span>

### <span data-ttu-id="34f4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34f4c-119">-DefaultProfile</span></span>
<span data-ttu-id="34f4c-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f4c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="34f4c-121">-Name</span></span>
<span data-ttu-id="34f4c-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-122">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: WorkspaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f4c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34f4c-123">-ResourceGroupName</span></span>
<span data-ttu-id="34f4c-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f4c-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34f4c-125">-ResourceId</span></span>
<span data-ttu-id="34f4c-126">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-126">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34f4c-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34f4c-127">CommonParameters</span></span>
<span data-ttu-id="34f4c-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34f4c-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34f4c-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34f4c-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34f4c-130">입력</span><span class="sxs-lookup"><span data-stu-id="34f4c-130">INPUTS</span></span>

### <span data-ttu-id="34f4c-131">없음</span><span class="sxs-lookup"><span data-stu-id="34f4c-131">None</span></span>

## <span data-ttu-id="34f4c-132">출력</span><span class="sxs-lookup"><span data-stu-id="34f4c-132">OUTPUTS</span></span>

### <span data-ttu-id="34f4c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34f4c-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="34f4c-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34f4c-134">NOTES</span></span>

## <span data-ttu-id="34f4c-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34f4c-135">RELATED LINKS</span></span>
