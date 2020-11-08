---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/test-azsynapsesparkpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Test-AzSynapseSparkPool.md
ms.openlocfilehash: 6304e730e6b3b0a4f8edc0f42fc024852acbfc12
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047464"
---
# <span data-ttu-id="d78a4-101">Test-AzSynapseSparkPool</span><span class="sxs-lookup"><span data-stu-id="d78a4-101">Test-AzSynapseSparkPool</span></span>

## <span data-ttu-id="d78a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d78a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d78a4-103">Synapse Analytics Spark 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-103">Checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d78a4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d78a4-104">SYNTAX</span></span>

### <span data-ttu-id="d78a4-105">TestByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d78a4-105">TestByNameParameterSet (Default)</span></span>
```
Test-AzSynapseSparkPool [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d78a4-106">TestByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d78a4-106">TestByParentObjectParameterSet</span></span>
```
Test-AzSynapseSparkPool -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d78a4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d78a4-107">DESCRIPTION</span></span>
<span data-ttu-id="d78a4-108">**AzSynapseSparkPool** Cmdlet은 Synapse Analytics Spark 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-108">The **Test-AzSynapseSparkPool** cmdlet checks for the existence of a Synapse Analytics Spark pool.</span></span>

## <span data-ttu-id="d78a4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d78a4-109">EXAMPLES</span></span>

### <span data-ttu-id="d78a4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d78a4-110">Example 1</span></span>
```powershell
PS C:\> Test-AzSynapseSparkPool -WorkspaceName ContosoWorkspace -Name ContosoSparkPool
```

<span data-ttu-id="d78a4-111">이 명령은 지정 된 Spark 풀이 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-111">This command checks the existence of the specified Spark pool.</span></span>

## <span data-ttu-id="d78a4-112">변수</span><span class="sxs-lookup"><span data-stu-id="d78a4-112">PARAMETERS</span></span>

### <span data-ttu-id="d78a4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d78a4-113">-DefaultProfile</span></span>
<span data-ttu-id="d78a4-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d78a4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="d78a4-115">-Name</span></span>
<span data-ttu-id="d78a4-116">Synapse Spark 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-116">Name of Synapse Spark pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78a4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d78a4-117">-ResourceGroupName</span></span>
<span data-ttu-id="d78a4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78a4-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d78a4-119">-WorkspaceName</span></span>
<span data-ttu-id="d78a4-120">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-120">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: TestByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d78a4-121">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="d78a4-121">-WorkspaceObject</span></span>
<span data-ttu-id="d78a4-122">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-122">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: TestByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d78a4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d78a4-123">CommonParameters</span></span>
<span data-ttu-id="d78a4-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d78a4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d78a4-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d78a4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d78a4-126">입력</span><span class="sxs-lookup"><span data-stu-id="d78a4-126">INPUTS</span></span>

### <span data-ttu-id="d78a4-127">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="d78a4-127">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="d78a4-128">출력</span><span class="sxs-lookup"><span data-stu-id="d78a4-128">OUTPUTS</span></span>

### <span data-ttu-id="d78a4-129">System. 개체</span><span class="sxs-lookup"><span data-stu-id="d78a4-129">System.Object</span></span>
## <span data-ttu-id="d78a4-130">상속자</span><span class="sxs-lookup"><span data-stu-id="d78a4-130">NOTES</span></span>

## <span data-ttu-id="d78a4-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d78a4-131">RELATED LINKS</span></span>
