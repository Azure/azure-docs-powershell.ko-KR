---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/disable-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Disable-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 72ee99f3d62470c4a3a62719006152a5f52cd8d1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491127"
---
# <span data-ttu-id="f84d9-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="f84d9-101">Disable-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="f84d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f84d9-102">SYNOPSIS</span></span>
<span data-ttu-id="f84d9-103">SQL 풀의 열에 대한 민감도 권장 사항을 사용하지 않도록 설정(해제)합니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-103">Disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f84d9-104">구문</span><span class="sxs-lookup"><span data-stu-id="f84d9-104">SYNTAX</span></span>

### <span data-ttu-id="f84d9-105">InputObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f84d9-105">InputObjectParameterSet (Default)</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -InputObject <SqlPoolSensitivityClassificationModel>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84d9-106">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84d9-106">ColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f84d9-107">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="f84d9-107">SqlPoolObjectColumnParameterSet</span></span>
```
Disable-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f84d9-108">설명</span><span class="sxs-lookup"><span data-stu-id="f84d9-108">DESCRIPTION</span></span>
<span data-ttu-id="f84d9-109">Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet은 SQL 풀의 열에 대한 민감도 권장 사항을 사용하지 않도록 설정(해제)합니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-109">The Disable-AzSynapseSqlPoolSensitivityRecommendation cmdlet disables (dismisses) sensitivity recommendations on columns in the SQL pool.</span></span>

## <span data-ttu-id="f84d9-110">예제</span><span class="sxs-lookup"><span data-stu-id="f84d9-110">EXAMPLES</span></span>

### <span data-ttu-id="f84d9-111">예제 1: Azure Synapse 풀의 주어진 열에서 민감도 권장 사항을 SQL 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-111">Example 1: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Disable-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName schema -TableName table -ColumnName column
```

### <span data-ttu-id="f84d9-112">예제 2: Piping을 사용하여 Azure Synapse 및 풀에서 민감도 권장 사항이 있는 열에 대한 민감도 SQL 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="f84d9-112">Example 2: Disable sensitivity recommendations on columns which have sensitivity recommendations in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation
```

### <span data-ttu-id="f84d9-113">예제 3: Piping을 사용하여 Azure Synapse SQL 열에 대한 민감도 권장 사항을 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="f84d9-113">Example 3: Disable sensitivity recommendations on a given column in an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Disable-AzSynapseSqlPoolSensitivityRecommendation -SchemaName schema -TableName table -ColumnName column
```

## <span data-ttu-id="f84d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f84d9-114">PARAMETERS</span></span>

### <span data-ttu-id="f84d9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f84d9-115">-AsJob</span></span>
<span data-ttu-id="f84d9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f84d9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f84d9-117">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="f84d9-117">-ColumnName</span></span>
<span data-ttu-id="f84d9-118">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-118">Name of column.</span></span>

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

### <span data-ttu-id="f84d9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84d9-119">-DefaultProfile</span></span>
<span data-ttu-id="f84d9-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f84d9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f84d9-121">-InputObject</span></span>
<span data-ttu-id="f84d9-122">풀 민감도 SQL 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-122">An object representing a SQL Pool Sensitivity Classification.</span></span>

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

### <span data-ttu-id="f84d9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f84d9-123">-PassThru</span></span>
<span data-ttu-id="f84d9-124">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-124">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="f84d9-125">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-125">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="f84d9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84d9-126">-ResourceGroupName</span></span>
<span data-ttu-id="f84d9-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-127">Resource group name.</span></span>

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

### <span data-ttu-id="f84d9-128">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="f84d9-128">-SchemaName</span></span>
<span data-ttu-id="f84d9-129">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-129">Name of schema.</span></span>

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

### <span data-ttu-id="f84d9-130">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="f84d9-130">-SqlPoolName</span></span>
<span data-ttu-id="f84d9-131">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-131">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="f84d9-132">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="f84d9-132">-SqlPoolObject</span></span>
<span data-ttu-id="f84d9-133">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-133">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="f84d9-134">-TableName</span><span class="sxs-lookup"><span data-stu-id="f84d9-134">-TableName</span></span>
<span data-ttu-id="f84d9-135">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-135">Name of table.</span></span>

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

### <span data-ttu-id="f84d9-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f84d9-136">-WorkspaceName</span></span>
<span data-ttu-id="f84d9-137">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-137">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="f84d9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f84d9-138">-Confirm</span></span>
<span data-ttu-id="f84d9-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f84d9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f84d9-140">-WhatIf</span></span>
<span data-ttu-id="f84d9-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f84d9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f84d9-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f84d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84d9-143">CommonParameters</span></span>
<span data-ttu-id="f84d9-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f84d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84d9-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f84d9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84d9-146">입력</span><span class="sxs-lookup"><span data-stu-id="f84d9-146">INPUTS</span></span>

### <span data-ttu-id="f84d9-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="f84d9-147">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

### <span data-ttu-id="f84d9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="f84d9-148">System.String</span></span>

### <span data-ttu-id="f84d9-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="f84d9-149">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="f84d9-150">출력</span><span class="sxs-lookup"><span data-stu-id="f84d9-150">OUTPUTS</span></span>

### <span data-ttu-id="f84d9-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f84d9-151">System.Boolean</span></span>

## <span data-ttu-id="f84d9-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f84d9-152">NOTES</span></span>

## <span data-ttu-id="f84d9-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f84d9-153">RELATED LINKS</span></span>
