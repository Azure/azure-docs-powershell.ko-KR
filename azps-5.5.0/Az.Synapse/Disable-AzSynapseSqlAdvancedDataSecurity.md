---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqladvanceddatasecurity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlAdvancedDataSecurity.md
ms.openlocfilehash: 2cbc79314d9e5fc7dac524786b8ba0bfa349573b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197420"
---
# <span data-ttu-id="0668b-101">Disable-AzSynapseSqlAdvancedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="0668b-101">Disable-AzSynapseSqlAdvancedDataSecurity</span></span>

## <span data-ttu-id="0668b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0668b-102">SYNOPSIS</span></span>
<span data-ttu-id="0668b-103">작업 영역의 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-103">Disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="0668b-104">구문</span><span class="sxs-lookup"><span data-stu-id="0668b-104">SYNTAX</span></span>

### <span data-ttu-id="0668b-105">DisableByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0668b-105">DisableByNameParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity [-ResourceGroupName <String>] -WorkspaceName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0668b-106">DisableByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0668b-106">DisableByInputObjectParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -InputObject <PSSynapseWorkspace> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0668b-107">DisableByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0668b-107">DisableByResourceIdParameterSet</span></span>
```
Disable-AzSynapseSqlAdvancedDataSecurity -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0668b-108">설명</span><span class="sxs-lookup"><span data-stu-id="0668b-108">DESCRIPTION</span></span>
<span data-ttu-id="0668b-109">**Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet은 작업 영역의 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-109">The **Disable-AzSynapseSqlAdvancedDataSecurity** cmdlet disables Advanced Data Security on a workspace.</span></span>

## <span data-ttu-id="0668b-110">예제</span><span class="sxs-lookup"><span data-stu-id="0668b-110">EXAMPLES</span></span>

### <span data-ttu-id="0668b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0668b-111">Example 1</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlAdvancedDataSecurity -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="0668b-112">이 명령은 ContosoWorkspace라는 작업 영역의 Advanced Data Security를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-112">This command disables Advanced Data Security on the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="0668b-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0668b-113">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseWorkspace -Name ContosoWorkspace | Disable-AzSynapseSqlAdvancedDataSecurity
```

<span data-ttu-id="0668b-114">이 명령은 파이프라인을 통해 ContosoWorkspace라는 작업 영역의 고급 데이터 보안을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-114">This command disables Advanced Data Security on the workspace named ContosoWorkspace through pipeline.</span></span>

## <span data-ttu-id="0668b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0668b-115">PARAMETERS</span></span>

### <span data-ttu-id="0668b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0668b-116">-AsJob</span></span>
<span data-ttu-id="0668b-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0668b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0668b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0668b-118">-DefaultProfile</span></span>
<span data-ttu-id="0668b-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0668b-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0668b-120">-InputObject</span></span>
<span data-ttu-id="0668b-121">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-121">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: DisableByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0668b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0668b-122">-ResourceGroupName</span></span>
<span data-ttu-id="0668b-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0668b-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0668b-124">-ResourceId</span></span>
<span data-ttu-id="0668b-125">Synapse 작업 영역의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-125">Resource identifier of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0668b-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0668b-126">-WorkspaceName</span></span>
<span data-ttu-id="0668b-127">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-127">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0668b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0668b-128">-Confirm</span></span>
<span data-ttu-id="0668b-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0668b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0668b-130">-WhatIf</span></span>
<span data-ttu-id="0668b-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0668b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0668b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0668b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0668b-133">CommonParameters</span></span>
<span data-ttu-id="0668b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0668b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0668b-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0668b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0668b-136">입력</span><span class="sxs-lookup"><span data-stu-id="0668b-136">INPUTS</span></span>

### <span data-ttu-id="0668b-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="0668b-137">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="0668b-138">출력</span><span class="sxs-lookup"><span data-stu-id="0668b-138">OUTPUTS</span></span>

### <span data-ttu-id="0668b-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="0668b-139">Microsoft.Azure.Commands.Synapse.Models.WorkspaceAdvancedDataSecurityPolicy</span></span>

## <span data-ttu-id="0668b-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0668b-140">NOTES</span></span>

## <span data-ttu-id="0668b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0668b-141">RELATED LINKS</span></span>
