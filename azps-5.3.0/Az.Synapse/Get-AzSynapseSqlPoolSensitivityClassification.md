---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityClassification.md
ms.openlocfilehash: 6affe94fdbfa7a698ad7d666d1847365fc8e25ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383839"
---
# <span data-ttu-id="9f82a-101">Get-AzSynapseSqlPoolSensitivityClassification</span><span class="sxs-lookup"><span data-stu-id="9f82a-101">Get-AzSynapseSqlPoolSensitivityClassification</span></span>

## <span data-ttu-id="9f82a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f82a-102">SYNOPSIS</span></span>
<span data-ttu-id="9f82a-103">SQL 풀에 있는 열의 현재 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="9f82a-103">Gets the current information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="9f82a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9f82a-104">SYNTAX</span></span>

### <span data-ttu-id="9f82a-105">SqlPoolObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9f82a-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f82a-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f82a-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f82a-107">ColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f82a-107">ColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> -SchemaName <String> -TableName <String> -ColumnName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9f82a-108">SqlPoolObjectColumnParameterSet</span><span class="sxs-lookup"><span data-stu-id="9f82a-108">SqlPoolObjectColumnParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityClassification -SqlPoolObject <PSSynapseSqlPool> -SchemaName <String>
 -TableName <String> -ColumnName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9f82a-109">설명</span><span class="sxs-lookup"><span data-stu-id="9f82a-109">DESCRIPTION</span></span>
<span data-ttu-id="9f82a-110">Get-AzSynapseSqlPoolSensitivityClassification cmdlet은 Azure Synapse SQL 풀에 있는 열의 현재 정보 유형 및 민감도 레이블을 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-110">The Get-AzSynapseSqlPoolSensitivityClassification cmdlet returns the current information types and sensitivity labels of columns in the Azure Synapse SQL pool.</span></span>

## <span data-ttu-id="9f82a-111">예제</span><span class="sxs-lookup"><span data-stu-id="9f82a-111">EXAMPLES</span></span>

### <span data-ttu-id="9f82a-112">예제 1: Azure Synapse 풀의 현재 정보 유형 및 민감도 레이블을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-112">Example 1: Get current information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="9f82a-113">예제 2: Piping을 사용하여 Azure Synapse SQL 풀의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-113">Example 2: Get current information types and sensitivity labels of an Azure Synapse SQL pool with Piping.</span></span>
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

### <span data-ttu-id="9f82a-114">예제 3: Azure Synapse 풀의 특정 열에 대한 현재 정보 유형 및 민감도 SQL.</span><span class="sxs-lookup"><span data-stu-id="9f82a-114">Example 3: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="9f82a-115">예제 4: Piping을 사용하여 Azure Synapse SQL 열의 현재 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-115">Example 4: Get current information type and sensitivity label of a specific column of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="9f82a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9f82a-116">PARAMETERS</span></span>

### <span data-ttu-id="9f82a-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9f82a-117">-AsJob</span></span>
<span data-ttu-id="9f82a-118">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9f82a-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9f82a-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9f82a-119">-ColumnName</span></span>
<span data-ttu-id="9f82a-120">열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-120">Name of column.</span></span>

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

### <span data-ttu-id="9f82a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f82a-121">-DefaultProfile</span></span>
<span data-ttu-id="9f82a-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9f82a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f82a-123">-ResourceGroupName</span></span>
<span data-ttu-id="9f82a-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-124">Resource group name.</span></span>

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

### <span data-ttu-id="9f82a-125">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9f82a-125">-SchemaName</span></span>
<span data-ttu-id="9f82a-126">schema의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-126">Name of schema.</span></span>

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

### <span data-ttu-id="9f82a-127">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="9f82a-127">-SqlPoolName</span></span>
<span data-ttu-id="9f82a-128">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-128">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="9f82a-129">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="9f82a-129">-SqlPoolObject</span></span>
<span data-ttu-id="9f82a-130">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-130">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9f82a-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="9f82a-131">-TableName</span></span>
<span data-ttu-id="9f82a-132">테이블의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-132">Name of table.</span></span>

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

### <span data-ttu-id="9f82a-133">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9f82a-133">-WorkspaceName</span></span>
<span data-ttu-id="9f82a-134">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-134">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9f82a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f82a-135">CommonParameters</span></span>
<span data-ttu-id="9f82a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9f82a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f82a-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9f82a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f82a-138">입력</span><span class="sxs-lookup"><span data-stu-id="9f82a-138">INPUTS</span></span>

### <span data-ttu-id="9f82a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9f82a-139">System.String</span></span>

### <span data-ttu-id="9f82a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="9f82a-140">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="9f82a-141">출력</span><span class="sxs-lookup"><span data-stu-id="9f82a-141">OUTPUTS</span></span>

### <span data-ttu-id="9f82a-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="9f82a-142">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="9f82a-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9f82a-143">NOTES</span></span>

## <span data-ttu-id="9f82a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f82a-144">RELATED LINKS</span></span>
