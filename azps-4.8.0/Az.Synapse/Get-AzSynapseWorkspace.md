---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseWorkspace.md
ms.openlocfilehash: d95892068b92745fa09419d83d3bdb001f0bdead
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204680"
---
# <span data-ttu-id="030b4-101">Get-AzSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="030b4-101">Get-AzSynapseWorkspace</span></span>

## <span data-ttu-id="030b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="030b4-102">SYNOPSIS</span></span>
<span data-ttu-id="030b4-103">Synapse Analytics 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-103">Gets a Synapse Analytics workspace.</span></span>

## <span data-ttu-id="030b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="030b4-104">SYNTAX</span></span>

### <span data-ttu-id="030b4-105">GetByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="030b4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseWorkspace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="030b4-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="030b4-106">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseWorkspace -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="030b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="030b4-107">DESCRIPTION</span></span>
<span data-ttu-id="030b4-108">**AzSynapseWorkspace** Cmdlet은 Azure Synapse Analytics 작업 영역에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-108">The **Get-AzSynapseWorkspace** cmdlet gets information about an Azure Synapse Analytics workspace.</span></span>

## <span data-ttu-id="030b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="030b4-109">EXAMPLES</span></span>

### <span data-ttu-id="030b4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="030b4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace
```

<span data-ttu-id="030b4-111">이 명령은 현재 구독 아래에 있는 모든 Azure Synapse Analytics 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-111">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="030b4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="030b4-112">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceGroupName ContosoResourceGroup
```

<span data-ttu-id="030b4-113">이 명령은 현재 구독 아래에 있는 모든 Azure Synapse Analytics 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-113">This command gets all the Azure Synapse Analytics workspaces under the current subscription.</span></span>

### <span data-ttu-id="030b4-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="030b4-114">Example 3</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace
```

<span data-ttu-id="030b4-115">이 명령은 지정 된 이름을 사용 하 여 Azure Synapse Analytics 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-115">This command gets the Azure Synapse Analytics workspace with the specified name.</span></span>

### <span data-ttu-id="030b4-116">예제 4</span><span class="sxs-lookup"><span data-stu-id="030b4-116">Example 4</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -ResourceId /subscriptions/21686af7-58ec-4f4d-9c68-f431f4db4edd/resourceGroups/ContosoResourceGroup/providers/Microsoft.Synapse/workspaces/ContosoWorkspace
```

<span data-ttu-id="030b4-117">이 명령은 지정 된 리소스 ID를 사용 하 여 Azure Synapse Analytics 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-117">This command gets the Azure Synapse Analytics workspace with the specified resource ID.</span></span>

## <span data-ttu-id="030b4-118">변수</span><span class="sxs-lookup"><span data-stu-id="030b4-118">PARAMETERS</span></span>

### <span data-ttu-id="030b4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="030b4-119">-DefaultProfile</span></span>
<span data-ttu-id="030b4-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="030b4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="030b4-121">-Name</span></span>
<span data-ttu-id="030b4-122">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-122">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="030b4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="030b4-123">-ResourceGroupName</span></span>
<span data-ttu-id="030b4-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-124">Resource group name.</span></span>

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

### <span data-ttu-id="030b4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="030b4-125">-ResourceId</span></span>
<span data-ttu-id="030b4-126">Synapse workspace의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-126">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="030b4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="030b4-127">CommonParameters</span></span>
<span data-ttu-id="030b4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="030b4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="030b4-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="030b4-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="030b4-130">입력</span><span class="sxs-lookup"><span data-stu-id="030b4-130">INPUTS</span></span>

### <span data-ttu-id="030b4-131">않아야</span><span class="sxs-lookup"><span data-stu-id="030b4-131">None</span></span>

## <span data-ttu-id="030b4-132">출력</span><span class="sxs-lookup"><span data-stu-id="030b4-132">OUTPUTS</span></span>

### <span data-ttu-id="030b4-133">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="030b4-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="030b4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="030b4-134">NOTES</span></span>

## <span data-ttu-id="030b4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="030b4-135">RELATED LINKS</span></span>
