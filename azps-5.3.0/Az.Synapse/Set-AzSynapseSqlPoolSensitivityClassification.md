---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: bb47d791f23df044e5a4677835f85b6f107f2822
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383195"
---
# <span data-ttu-id="a8dfd-101">Set-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="a8dfd-101">Set-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="a8dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="a8dfd-103">SQL 풀에 있는 열의 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-103">Sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="a8dfd-104">구문</span><span class="sxs-lookup"><span data-stu-id="a8dfd-104">SYNTAX</span></span>

### <span data-ttu-id="a8dfd-105">ClassificationObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a8dfd-105">ClassificationObjectParameterSet (Default)</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8dfd-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8dfd-106">ColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 [-ResourceGroupName] <String> [-WorkspaceName] <String> [-SqlPoolName] <String> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8dfd-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8dfd-107">SqlPoolObjectColumnParameterSet</span></span>
```
Set-AzSynapseSqlPoolSensitivityClassification [-SensitivityLabel <String>] [-InformationType <String>]
 -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8dfd-108">설명</span><span class="sxs-lookup"><span data-stu-id="a8dfd-108">DESCRIPTION</span></span>
<span data-ttu-id="a8dfd-109">Set-AzSynapseSqlPoolSensitivityClassification cmdlet은 SQL 풀에 있는 열의 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-109">The Set-AzSynapseSqlPoolSensitivityClassification cmdlet sets the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="a8dfd-110">예제</span><span class="sxs-lookup"><span data-stu-id="a8dfd-110">EXAMPLES</span></span>

### <span data-ttu-id="a8dfd-111">예제 1: Azure Synapse 풀에서 열의 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-111">Example 1: Set information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Set-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

### <span data-ttu-id="a8dfd-112">예제 2: Azure Synapse 풀에서 권장되는 정보 유형 및 민감도 레이블을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-112">Example 2: Set recommended information types and sensitivity labels of columns in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="a8dfd-113">예제 3: 파이핑을 사용하여 Azure Synapse SQL 열의 정보 유형 및 민감도 레이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-113">Example 3: Set information type and sensitivity label of a column in an Azure Synapse SQL pool, using piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Set-AzSynapseSqlPoolSensitivityClassification  -SchemaName schema -TableName table -ColumnName column -InformationType informationType -SensitivityLabel label
```

## <span data-ttu-id="a8dfd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8dfd-114">PARAMETERS</span></span>

### <span data-ttu-id="a8dfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8dfd-115">-AsJob</span></span>
<span data-ttu-id="a8dfd-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a8dfd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8dfd-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="a8dfd-117">-ClassificationObject</span></span>
<span data-ttu-id="a8dfd-118">풀 민감도 SQL 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel
Parameter Sets: ClassificationObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfd-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-119">-ColumnName</span></span>
<span data-ttu-id="a8dfd-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-120">Name of column.</span></span>

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

### <span data-ttu-id="a8dfd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8dfd-121">-DefaultProfile</span></span>
<span data-ttu-id="a8dfd-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8dfd-123">-InformationType</span><span class="sxs-lookup"><span data-stu-id="a8dfd-123">-InformationType</span></span>
<span data-ttu-id="a8dfd-124">열에 저장된 데이터의 정보 형식을 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-124">A name that describes the information type of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a8dfd-125">-PassThru</span></span>
<span data-ttu-id="a8dfd-126">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-126">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a8dfd-127">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-127">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a8dfd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-128">-ResourceGroupName</span></span>
<span data-ttu-id="a8dfd-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-129">Resource group name.</span></span>

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

### <span data-ttu-id="a8dfd-130">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-130">-SchemaName</span></span>
<span data-ttu-id="a8dfd-131">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-131">Name of schema.</span></span>

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

### <span data-ttu-id="a8dfd-132">-SensitivityLabel</span><span class="sxs-lookup"><span data-stu-id="a8dfd-132">-SensitivityLabel</span></span>
<span data-ttu-id="a8dfd-133">열에 저장된 데이터의 민감도를 설명하는 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-133">A name that describes the sensitivity of the data stored in the column.</span></span>

```yaml
Type: System.String
Parameter Sets: ColumnParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a8dfd-134">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-134">-SqlPoolName</span></span>
<span data-ttu-id="a8dfd-135">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-135">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="a8dfd-136">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="a8dfd-136">-SqlPoolObject</span></span>
<span data-ttu-id="a8dfd-137">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-137">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="a8dfd-138">-TableName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-138">-TableName</span></span>
<span data-ttu-id="a8dfd-139">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-139">Name of table.</span></span>

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

### <span data-ttu-id="a8dfd-140">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a8dfd-140">-WorkspaceName</span></span>
<span data-ttu-id="a8dfd-141">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-141">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="a8dfd-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a8dfd-142">-Confirm</span></span>
<span data-ttu-id="a8dfd-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8dfd-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8dfd-144">-WhatIf</span></span>
<span data-ttu-id="a8dfd-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a8dfd-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8dfd-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8dfd-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8dfd-147">CommonParameters</span></span>
<span data-ttu-id="a8dfd-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8dfd-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a8dfd-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8dfd-150">입력</span><span class="sxs-lookup"><span data-stu-id="a8dfd-150">INPUTS</span></span>

### <span data-ttu-id="a8dfd-151">System.String</span><span class="sxs-lookup"><span data-stu-id="a8dfd-151">System.String</span></span>

### <span data-ttu-id="a8dfd-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="a8dfd-152">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="a8dfd-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="a8dfd-153">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="a8dfd-154">출력</span><span class="sxs-lookup"><span data-stu-id="a8dfd-154">OUTPUTS</span></span>

### <span data-ttu-id="a8dfd-155">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a8dfd-155">System.Boolean</span></span>

## <span data-ttu-id="a8dfd-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a8dfd-156">NOTES</span></span>

## <span data-ttu-id="a8dfd-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a8dfd-157">RELATED LINKS</span></span>
