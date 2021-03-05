---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 0942373dc3ad741f10d5a87d7b4713413f9db4f3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010139"
---
# <span data-ttu-id="da047-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="da047-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="da047-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da047-102">SYNOPSIS</span></span>
<span data-ttu-id="da047-103">현재 정보 형식 및 열의 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="da047-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="da047-104">구문</span><span class="sxs-lookup"><span data-stu-id="da047-104">SYNTAX</span></span>

### <span data-ttu-id="da047-105">SqlPoolObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="da047-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da047-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="da047-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da047-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="da047-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="da047-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="da047-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da047-109">설명</span><span class="sxs-lookup"><span data-stu-id="da047-109">DESCRIPTION</span></span>
<span data-ttu-id="da047-110">Get-AzSynapseSqlPoolSensitivityClassification cmdlet은 Azure Synapse SQL 열의 현재 정보 형식 및 민감도 레이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="da047-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="da047-111">예제</span><span class="sxs-lookup"><span data-stu-id="da047-111">EXAMPLES</span></span>

### <span data-ttu-id="da047-112">예제 1: Azure Synapse 풀의 현재 정보 유형 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="da047-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="da047-113">예제 2: Piping을 사용하여 Azure Synapse SQL 풀의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da047-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailBody,
                        InformationType: Contact Info
                    }, {
                        SchemaName: dbo,
                        TableName: Report,
                        ColumnName: ReportEmailSubject,
                        SensitivityLabel: Confidential,
                        Rank: Medium
                    }, {
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="da047-114">예제 3: Azure Synapse 풀의 특정 열의 현재 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="da047-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityClassification -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

### <span data-ttu-id="da047-115">예제 4: Piping을 사용하여 Azure Synapse SQL 열의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="da047-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityClassification -SchemaName dbo -TableName EMailLog -ColumnName BounceEmailSubject

ResourceGroupName : ContosoResourceGroup
WorkspaceName        : ContosoWorkspace
SqlPoolName      : ContosoSqlPool
SensitivityLabels : {{
                        SchemaName: dbo,
                        TableName: EMailLog,
                        ColumnName: BounceEmailSubject,
                        SensitivityLabel: Confidential,
                        InformationType: Contact Info,
                        Rank: Medium
                    }}
```

## <span data-ttu-id="da047-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="da047-116">PARAMETERS</span></span>

### <span data-ttu-id="da047-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="da047-117">-AsJob</span></span>
<span data-ttu-id="da047-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="da047-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="da047-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="da047-119">-ColumnName</span></span>
<span data-ttu-id="da047-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-120">Name of column.</span></span>

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

### <span data-ttu-id="da047-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da047-121">-DefaultProfile</span></span>
<span data-ttu-id="da047-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da047-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da047-123">-ResourceGroupName</span></span>
<span data-ttu-id="da047-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da047-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="da047-125">-SchemaName</span></span>
<span data-ttu-id="da047-126">Schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-126">Name of schema.</span></span>

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

### <span data-ttu-id="da047-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="da047-127">-SqlPoolName</span></span>
<span data-ttu-id="da047-128">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-128">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da047-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="da047-129">-SqlPoolObject</span></span>
<span data-ttu-id="da047-130">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="da047-130">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet, SqlPoolObjectColumnParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="da047-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="da047-131">-TableName</span></span>
<span data-ttu-id="da047-132">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-132">Name of table.</span></span>

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

### <span data-ttu-id="da047-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="da047-133">-WorkspaceName</span></span>
<span data-ttu-id="da047-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="da047-134">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet, ColumnParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da047-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da047-135">CommonParameters</span></span>
<span data-ttu-id="da047-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="da047-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da047-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="da047-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da047-138">입력</span><span class="sxs-lookup"><span data-stu-id="da047-138">INPUTS</span></span>

### <span data-ttu-id="da047-139">System.String</span><span class="sxs-lookup"><span data-stu-id="da047-139">System.String</span></span>

### <span data-ttu-id="da047-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="da047-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="da047-141">출력</span><span class="sxs-lookup"><span data-stu-id="da047-141">OUTPUTS</span></span>

### <span data-ttu-id="da047-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="da047-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="da047-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="da047-143">NOTES</span></span>

## <span data-ttu-id="da047-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="da047-144">RELATED LINKS</span></span>
