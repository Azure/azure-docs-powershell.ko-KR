---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: a278b316a62639c6c33d4f05491e314a2b9a1e85
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383349"
---
# <span data-ttu-id="f98da-101">Remove-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="f98da-101">Remove-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="f98da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f98da-102">SYNOPSIS</span></span>
<span data-ttu-id="f98da-103">데이터 풀에서 열의 정보 형식 및 민감도 레이블을 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-103">Removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="f98da-104">구문</span><span class="sxs-lookup"><span data-stu-id="f98da-104">SYNTAX</span></span>

### <span data-ttu-id="f98da-105">ClassificationObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f98da-105">ClassificationObjectParameterSet (Default)</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -ClassificationObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98da-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98da-106">ColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f98da-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f98da-107">SqlPoolObjectColumnParameterSet</span></span>
```
Remove-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f98da-108">설명</span><span class="sxs-lookup"><span data-stu-id="f98da-108">DESCRIPTION</span></span>
<span data-ttu-id="f98da-109">Remove-AzSynapseSqlPoolSensitivityClassification cmdlet은 SQL 풀에 있는 열의 정보 형식 및 민감도 레이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-109">The Remove-AzSynapseSqlPoolSensitivityClassification cmdlet removes the information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="f98da-110">예제</span><span class="sxs-lookup"><span data-stu-id="f98da-110">EXAMPLES</span></span>

### <span data-ttu-id="f98da-111">예제 1: Azure Synapse 풀에서 열의 정보 유형 및 민감도 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-111">Example 1: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Remove-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f98da-112">예제 2: Piping을 사용하여 Azure Synapse SQL 열의 현재 정보 유형 및 민감도 레이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-112">Example 2: Remove current information types and sensitivity labels of columns in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification
```

### <span data-ttu-id="f98da-113">예제 3: Piping을 사용하여 Azure Synapse SQL 열의 정보 유형 및 민감도 레이블을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-113">Example 3: Remove information type and sensitivity label of a column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Remove-AzSynapseSqlPoolSensitivityClassification -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f98da-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f98da-114">PARAMETERS</span></span>

### <span data-ttu-id="f98da-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f98da-115">-AsJob</span></span>
<span data-ttu-id="f98da-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f98da-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f98da-117">-ClassificationObject</span><span class="sxs-lookup"><span data-stu-id="f98da-117">-ClassificationObject</span></span>
<span data-ttu-id="f98da-118">풀 민감도 SQL 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-118">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f98da-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f98da-119">-ColumnName</span></span>
<span data-ttu-id="f98da-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-120">Name of column.</span></span>

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

### <span data-ttu-id="f98da-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f98da-121">-DefaultProfile</span></span>
<span data-ttu-id="f98da-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f98da-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f98da-123">-PassThru</span></span>
<span data-ttu-id="f98da-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f98da-125">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f98da-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f98da-126">-ResourceGroupName</span></span>
<span data-ttu-id="f98da-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-127">Resource group name.</span></span>

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

### <span data-ttu-id="f98da-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f98da-128">-SchemaName</span></span>
<span data-ttu-id="f98da-129">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-129">Name of schema.</span></span>

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

### <span data-ttu-id="f98da-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="f98da-130">-SqlPoolName</span></span>
<span data-ttu-id="f98da-131">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f98da-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="f98da-132">-SqlPoolObject</span></span>
<span data-ttu-id="f98da-133">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f98da-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="f98da-134">-TableName</span></span>
<span data-ttu-id="f98da-135">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-135">Name of table.</span></span>

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

### <span data-ttu-id="f98da-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f98da-136">-WorkspaceName</span></span>
<span data-ttu-id="f98da-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f98da-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f98da-138">-Confirm</span></span>
<span data-ttu-id="f98da-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f98da-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f98da-140">-WhatIf</span></span>
<span data-ttu-id="f98da-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f98da-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f98da-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f98da-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f98da-143">CommonParameters</span></span>
<span data-ttu-id="f98da-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f98da-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f98da-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f98da-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f98da-146">입력</span><span class="sxs-lookup"><span data-stu-id="f98da-146">INPUTS</span></span>

### <span data-ttu-id="f98da-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f98da-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="f98da-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f98da-148">System.String</span></span>

### <span data-ttu-id="f98da-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f98da-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f98da-150">출력</span><span class="sxs-lookup"><span data-stu-id="f98da-150">OUTPUTS</span></span>

### <span data-ttu-id="f98da-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f98da-151">System.Boolean</span></span>

## <span data-ttu-id="f98da-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f98da-152">NOTES</span></span>

## <span data-ttu-id="f98da-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f98da-153">RELATED LINKS</span></span>
