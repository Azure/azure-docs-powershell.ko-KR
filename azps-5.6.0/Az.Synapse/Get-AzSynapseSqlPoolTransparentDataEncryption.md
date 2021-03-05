---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: cee34e8437048f0cc59df3463b0b7f3cf2de6ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985488"
---
# <span data-ttu-id="bbff3-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="bbff3-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="bbff3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbff3-102">SYNOPSIS</span></span>
<span data-ttu-id="bbff3-103">풀에 대한 TDE SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="bbff3-104">구문</span><span class="sxs-lookup"><span data-stu-id="bbff3-104">SYNTAX</span></span>

### <span data-ttu-id="bbff3-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bbff3-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbff3-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbff3-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbff3-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbff3-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bbff3-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbff3-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bbff3-109">설명</span><span class="sxs-lookup"><span data-stu-id="bbff3-109">DESCRIPTION</span></span>
<span data-ttu-id="bbff3-110">**Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet은 Azure Synapse Analytics 풀에 대한 TDE(투명한 데이터 암호화) SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="bbff3-111">예제</span><span class="sxs-lookup"><span data-stu-id="bbff3-111">EXAMPLES</span></span>

### <span data-ttu-id="bbff3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bbff3-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="bbff3-113">이 명령은 ContosoWorkspace라는 작업 영역 아래에서 ContosoSqlPool이라는 SQL 풀에 대한 TDE 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="bbff3-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bbff3-114">PARAMETERS</span></span>

### <span data-ttu-id="bbff3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbff3-115">-DefaultProfile</span></span>
<span data-ttu-id="bbff3-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bbff3-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbff3-117">-InputObject</span></span>
<span data-ttu-id="bbff3-118">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-118">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: GetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbff3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bbff3-119">-Name</span></span>
<span data-ttu-id="bbff3-120">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bbff3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbff3-121">-ResourceGroupName</span></span>
<span data-ttu-id="bbff3-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-122">Resource group name.</span></span>

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

### <span data-ttu-id="bbff3-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbff3-123">-ResourceId</span></span>
<span data-ttu-id="bbff3-124">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="bbff3-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bbff3-125">-WorkspaceName</span></span>
<span data-ttu-id="bbff3-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="bbff3-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bbff3-127">-WorkspaceObject</span></span>
<span data-ttu-id="bbff3-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-128">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bbff3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbff3-129">CommonParameters</span></span>
<span data-ttu-id="bbff3-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bbff3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbff3-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bbff3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbff3-132">입력</span><span class="sxs-lookup"><span data-stu-id="bbff3-132">INPUTS</span></span>

### <span data-ttu-id="bbff3-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="bbff3-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="bbff3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="bbff3-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="bbff3-135">출력</span><span class="sxs-lookup"><span data-stu-id="bbff3-135">OUTPUTS</span></span>

### <span data-ttu-id="bbff3-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="bbff3-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="bbff3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bbff3-137">NOTES</span></span>

## <span data-ttu-id="bbff3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbff3-138">RELATED LINKS</span></span>
