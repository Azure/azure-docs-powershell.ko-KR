---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpooltransparentdataencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolTransparentDataEncryption.md
ms.openlocfilehash: 5e127388b756c19422990bf27ee40e351bfc2581
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190633"
---
# <span data-ttu-id="4d053-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4d053-101">Get-AzSynapseSqlPoolTransparentDataEncryption</span></span>

## <span data-ttu-id="4d053-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d053-102">SYNOPSIS</span></span>
<span data-ttu-id="4d053-103">SQL 풀에 대한 TDE 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-103">Gets the TDE state for a SQL pool.</span></span>

## <span data-ttu-id="4d053-104">구문</span><span class="sxs-lookup"><span data-stu-id="4d053-104">SYNTAX</span></span>

### <span data-ttu-id="4d053-105">GetByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4d053-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption [-ResourceGroupName <String>] -WorkspaceName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d053-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d053-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -Name <String> -WorkspaceObject <PSSynapseWorkspace>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d053-107">GetByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d053-107">GetByInputObjectParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -InputObject <PSSynapseSqlPool>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d053-108">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d053-108">GetByResourceIdParameterSet</span></span>
```
Get-AzSynapseSqlPoolTransparentDataEncryption -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d053-109">설명</span><span class="sxs-lookup"><span data-stu-id="4d053-109">DESCRIPTION</span></span>
<span data-ttu-id="4d053-110">**Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet은 Azure Synapse Analytics SQL 풀에 대한 TDE(투명한 데이터 암호화) 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-110">The **Get-AzSynapseSqlPoolTransparentDataEncryption** cmdlet gets the state of Transparent Data Encryption (TDE) for an Azure Synapse Analytics SQL pool.</span></span>

## <span data-ttu-id="4d053-111">예제</span><span class="sxs-lookup"><span data-stu-id="4d053-111">EXAMPLES</span></span>

### <span data-ttu-id="4d053-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d053-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolTransparentDataEncryption -WorkspaceName ContosoWorkspace -Name ContosoSqlPool
```

<span data-ttu-id="4d053-113">이 명령은 ContosoWorkspace라는 작업 SQL ContosoSqlPool이라는 SQL 풀에 대한 TDE의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-113">This command gets the status of TDE for the SQL pool named ContosoSqlPool under the workspace named ContosoWorkspace.</span></span>

## <span data-ttu-id="4d053-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d053-114">PARAMETERS</span></span>

### <span data-ttu-id="4d053-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d053-115">-DefaultProfile</span></span>
<span data-ttu-id="4d053-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d053-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d053-117">-InputObject</span></span>
<span data-ttu-id="4d053-118">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-118">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d053-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4d053-119">-Name</span></span>
<span data-ttu-id="4d053-120">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="4d053-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d053-121">-ResourceGroupName</span></span>
<span data-ttu-id="4d053-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-122">Resource group name.</span></span>

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

### <span data-ttu-id="4d053-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d053-123">-ResourceId</span></span>
<span data-ttu-id="4d053-124">Synapse SQL 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-124">Resource identifier of Synapse SQL Pool.</span></span>

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

### <span data-ttu-id="4d053-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d053-125">-WorkspaceName</span></span>
<span data-ttu-id="4d053-126">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-126">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="4d053-127">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d053-127">-WorkspaceObject</span></span>
<span data-ttu-id="4d053-128">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-128">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="4d053-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d053-129">CommonParameters</span></span>
<span data-ttu-id="4d053-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4d053-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d053-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4d053-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d053-132">입력</span><span class="sxs-lookup"><span data-stu-id="4d053-132">INPUTS</span></span>

### <span data-ttu-id="4d053-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d053-133">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="4d053-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="4d053-134">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="4d053-135">출력</span><span class="sxs-lookup"><span data-stu-id="4d053-135">OUTPUTS</span></span>

### <span data-ttu-id="4d053-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span><span class="sxs-lookup"><span data-stu-id="4d053-136">Microsoft.Azure.Commands.Synapse.Models.PSTransparentDataEncryption</span></span>

## <span data-ttu-id="4d053-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4d053-137">NOTES</span></span>

## <span data-ttu-id="4d053-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d053-138">RELATED LINKS</span></span>
