---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqladvanceddatasecuritypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlAdvancedDataSecurityPolicy.md
ms.openlocfilehash: b0d21c8d59d2a33671fead2e88d402779f99fb7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383937"
---
# <span data-ttu-id="ab8bd-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab8bd-101">Get-AzSynapseSqlAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ab8bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab8bd-102">SYNOPSIS</span></span>
<span data-ttu-id="ab8bd-103">작업 영역의 고급 데이터 보안 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-103">Gets Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="ab8bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="ab8bd-104">SYNTAX</span></span>

### <span data-ttu-id="ab8bd-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ab8bd-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy [-ResourceGroupName <String>] -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8bd-106">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8bd-106">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -InputObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ab8bd-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ab8bd-107">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlAdvancedDataSecurityPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ab8bd-108">설명</span><span class="sxs-lookup"><span data-stu-id="ab8bd-108">DESCRIPTION</span></span>
<span data-ttu-id="ab8bd-109">**Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet은 작업 영역의 고급 데이터 보안 정책을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-109">The **Get-AzSynapseSqlAdvancedDataSecurityPolicy** cmdlet retrieves the Advanced Data Security policy of a workspace.</span></span>

## <span data-ttu-id="ab8bd-110">예제</span><span class="sxs-lookup"><span data-stu-id="ab8bd-110">EXAMPLES</span></span>

### <span data-ttu-id="ab8bd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ab8bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlAdvancedDataSecurityPolicy -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="ab8bd-112">이 명령은 ContosoWorkspace라는 작업 영역의 Advanced Data Security를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-112">This command gets Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="ab8bd-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ab8bd-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Get-AzSynapseSqlAdvancedDataSecurityPolicy
```

<span data-ttu-id="ab8bd-114">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 Advanced Data Security를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-114">This command gets Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="ab8bd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab8bd-115">PARAMETERS</span></span>

### <span data-ttu-id="ab8bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab8bd-116">-DefaultProfile</span></span>
<span data-ttu-id="ab8bd-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab8bd-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab8bd-118">-InputObject</span></span>
<span data-ttu-id="ab8bd-119">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-119">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab8bd-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab8bd-120">-ResourceGroupName</span></span>
<span data-ttu-id="ab8bd-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-121">Resource group name.</span></span>

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

### <span data-ttu-id="ab8bd-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab8bd-122">-ResourceId</span></span>
<span data-ttu-id="ab8bd-123">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-123">Resource identifier of Synapse workspace.</span></span>

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

### <span data-ttu-id="ab8bd-124">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ab8bd-124">-WorkspaceName</span></span>
<span data-ttu-id="ab8bd-125">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-125">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab8bd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab8bd-126">CommonParameters</span></span>
<span data-ttu-id="ab8bd-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab8bd-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ab8bd-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab8bd-129">입력</span><span class="sxs-lookup"><span data-stu-id="ab8bd-129">INPUTS</span></span>

### <span data-ttu-id="ab8bd-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="ab8bd-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="ab8bd-131">출력</span><span class="sxs-lookup"><span data-stu-id="ab8bd-131">OUTPUTS</span></span>

### <span data-ttu-id="ab8bd-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="ab8bd-132">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="ab8bd-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ab8bd-133">NOTES</span></span>

## <span data-ttu-id="ab8bd-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ab8bd-134">RELATED LINKS</span></span>
