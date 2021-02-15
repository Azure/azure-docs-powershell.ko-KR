---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/enable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Enable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 52abddf2db18a6e70a1b876629feff0761bed014
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197401"
---
# <span data-ttu-id="94999-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="94999-101">Enable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="94999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94999-102">SYNOPSIS</span></span>
<span data-ttu-id="94999-103">기본 풀에서 열에 대한 민감도 권장 사항(기본적으로 모든 열에서 권장 사항 사용)SQL 활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="94999-103">Enables sensitivity recommendations on columns (recommendations are enabled by default on all columns) in the SQL pool.</span></span>

## <span data-ttu-id="94999-104">구문</span><span class="sxs-lookup"><span data-stu-id="94999-104">SYNTAX</span></span>

### <span data-ttu-id="94999-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="94999-105">InputObjectParameterSet (Default)</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94999-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="94999-106">ColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94999-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="94999-107">SqlPoolObjectColumnParameterSet</span></span>
```
Enable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94999-108">설명</span><span class="sxs-lookup"><span data-stu-id="94999-108">DESCRIPTION</span></span>
<span data-ttu-id="94999-109">Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet을 사용하면 SQL 풀의 열에 대한 민감도 권장 사항을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94999-109">The Enable-AzSynapseSqlPoolSensitivityRecommendation cmdlet enables sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="94999-110">예제</span><span class="sxs-lookup"><span data-stu-id="94999-110">EXAMPLES</span></span>

### <span data-ttu-id="94999-111">예제 1: Azure Synapse 풀의 주어진 열에 대해 민감도 권장 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94999-111">Example 1: Enable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Enable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="94999-112">예제 2: Piping을 사용하여 Azure Synapse SQL 열에 대해 민감도 권장 사항을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="94999-112">Example 2: Enable sensitivity recommendations on a given column Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Enable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="94999-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94999-113">PARAMETERS</span></span>

### <span data-ttu-id="94999-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94999-114">-AsJob</span></span>
<span data-ttu-id="94999-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="94999-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94999-116">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="94999-116">-ColumnName</span></span>
<span data-ttu-id="94999-117">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-117">Name of column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94999-118">-DefaultProfile</span></span>
<span data-ttu-id="94999-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94999-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94999-120">-InputObject</span></span>
<span data-ttu-id="94999-121">풀 민감도 SQL 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-121">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: InputObjectParameterSet
Aliases: ClassificationObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94999-122">-PassThru</span></span>
<span data-ttu-id="94999-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94999-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="94999-124">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="94999-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="94999-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94999-125">-ResourceGroupName</span></span>
<span data-ttu-id="94999-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="94999-127">-SchemaName</span></span>
<span data-ttu-id="94999-128">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-128">Name of schema.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-129">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="94999-129">-SqlPoolName</span></span>
<span data-ttu-id="94999-130">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-130">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-131">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="94999-131">-SqlPoolObject</span></span>
<span data-ttu-id="94999-132">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="94999-132">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-133">-TableName</span><span class="sxs-lookup"><span data-stu-id="94999-133">-TableName</span></span>
<span data-ttu-id="94999-134">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-134">Name of table.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94999-135">-WorkspaceName</span></span>
<span data-ttu-id="94999-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94999-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94999-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94999-137">-Confirm</span></span>
<span data-ttu-id="94999-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94999-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94999-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94999-139">-WhatIf</span></span>
<span data-ttu-id="94999-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94999-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94999-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94999-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94999-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94999-142">CommonParameters</span></span>
<span data-ttu-id="94999-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94999-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94999-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94999-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94999-145">입력</span><span class="sxs-lookup"><span data-stu-id="94999-145">INPUTS</span></span>

### <span data-ttu-id="94999-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="94999-146">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="94999-147">System.String</span><span class="sxs-lookup"><span data-stu-id="94999-147">System.String</span></span>

### <span data-ttu-id="94999-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="94999-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="94999-149">출력</span><span class="sxs-lookup"><span data-stu-id="94999-149">OUTPUTS</span></span>

### <span data-ttu-id="94999-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94999-150">System.Boolean</span></span>

## <span data-ttu-id="94999-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94999-151">NOTES</span></span>

## <span data-ttu-id="94999-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94999-152">RELATED LINKS</span></span>
