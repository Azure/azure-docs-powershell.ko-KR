---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: 89b9b5df2f8233254d4c1cb430a80f0a8a91c13b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383818"
---
# <span data-ttu-id="7598c-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="7598c-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="7598c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7598c-102">SYNOPSIS</span></span>
<span data-ttu-id="7598c-103">SQL 풀에 있는 열의 권장 정보 유형 및 민감도 레이블을 SQL.</span><span class="sxs-lookup"><span data-stu-id="7598c-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7598c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7598c-104">SYNTAX</span></span>

### <span data-ttu-id="7598c-105">SqlPoolObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7598c-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7598c-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="7598c-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7598c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7598c-107">DESCRIPTION</span></span>
<span data-ttu-id="7598c-108">Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet은 SQL 풀에 있는 열의 권장 정보 유형 및 민감도 레이블을 SQL 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="7598c-109">예제</span><span class="sxs-lookup"><span data-stu-id="7598c-109">EXAMPLES</span></span>

### <span data-ttu-id="7598c-110">예제 1: Azure Synapse 풀의 권장 정보 유형 및 민감도 레이블을 SQL 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPoolSensitivityRecommendation -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -SqlPoolName ContosoSqlPool

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

### <span data-ttu-id="7598c-111">예제 2: Piping을 사용하여 Azure Synapse SQL 권장되는 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
```powershell
PS C:\> Get-AzSynapseSqlPool -ResourceGroupName ContosoResourceGroup -WorkspaceName ContosoWorkspace -Name ContosoSqlPool | Get-AzSynapseSqlPoolSensitivityRecommendation

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

## <span data-ttu-id="7598c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7598c-112">PARAMETERS</span></span>

### <span data-ttu-id="7598c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7598c-113">-AsJob</span></span>
<span data-ttu-id="7598c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7598c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7598c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7598c-115">-DefaultProfile</span></span>
<span data-ttu-id="7598c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7598c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7598c-117">-ResourceGroupName</span></span>
<span data-ttu-id="7598c-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-118">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7598c-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="7598c-119">-SqlPoolName</span></span>
<span data-ttu-id="7598c-120">Synapse SQL 풀입니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-120">Name of Synapse SQL pool.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7598c-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="7598c-121">-SqlPoolObject</span></span>
<span data-ttu-id="7598c-122">SQL 풀 입력 개체를 만듭니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-122">SQL pool input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool
Parameter Sets: SqlPoolObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7598c-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7598c-123">-WorkspaceName</span></span>
<span data-ttu-id="7598c-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SqlPoolParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7598c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7598c-125">CommonParameters</span></span>
<span data-ttu-id="7598c-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7598c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7598c-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7598c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7598c-128">입력</span><span class="sxs-lookup"><span data-stu-id="7598c-128">INPUTS</span></span>

### <span data-ttu-id="7598c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="7598c-129">System.String</span></span>

### <span data-ttu-id="7598c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="7598c-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="7598c-131">출력</span><span class="sxs-lookup"><span data-stu-id="7598c-131">OUTPUTS</span></span>

### <span data-ttu-id="7598c-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="7598c-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="7598c-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7598c-133">NOTES</span></span>

## <span data-ttu-id="7598c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7598c-134">RELATED LINKS</span></span>
