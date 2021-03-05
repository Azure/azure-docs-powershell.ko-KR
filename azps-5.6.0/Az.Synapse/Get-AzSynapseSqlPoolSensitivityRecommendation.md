---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsesqlpoolsensitivityrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseSqlPoolSensitivityRecommendation.md
ms.openlocfilehash: d2949bf2d366dc64b0e55b82d0c90979042ea294
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985502"
---
# <span data-ttu-id="5d0f4-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="5d0f4-101">Get-AzSynapseSqlPoolSensitivityRecommendation</span></span>

## <span data-ttu-id="5d0f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="5d0f4-103">권장되는 정보 형식 및 열의 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-103">Gets the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="5d0f4-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d0f4-104">SYNTAX</span></span>

### <span data-ttu-id="5d0f4-105">SqlPoolObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="5d0f4-105">SqlPoolObjectParameterSet (Default)</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation -SqlPoolObject <PSSynapseSqlPool> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d0f4-106">SqlPoolParameterSet</span><span class="sxs-lookup"><span data-stu-id="5d0f4-106">SqlPoolParameterSet</span></span>
```
Get-AzSynapseSqlPoolSensitivityRecommendation [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SqlPoolName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d0f4-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d0f4-107">DESCRIPTION</span></span>
<span data-ttu-id="5d0f4-108">Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet은 SQL 열의 권장 정보 유형 및 민감도 레이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-108">The Get-AzSynapseSqlPoolSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the SQL pool.</span></span>

## <span data-ttu-id="5d0f4-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d0f4-109">EXAMPLES</span></span>

### <span data-ttu-id="5d0f4-110">예제 1: Azure Synapse 풀의 권장 정보 유형 및 민감도 레이블을 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-110">Example 1: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool.</span></span>
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

### <span data-ttu-id="5d0f4-111">예제 2: Piping을 사용하여 Azure Synapse SQL 풀의 권장 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-111">Example 2: Get recommended information types and sensitivity labels of an Azure Synapse SQL pool using Piping.</span></span>
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

## <span data-ttu-id="5d0f4-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5d0f4-112">PARAMETERS</span></span>

### <span data-ttu-id="5d0f4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d0f4-113">-AsJob</span></span>
<span data-ttu-id="5d0f4-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5d0f4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5d0f4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d0f4-115">-DefaultProfile</span></span>
<span data-ttu-id="5d0f4-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d0f4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d0f4-117">-ResourceGroupName</span></span>
<span data-ttu-id="5d0f4-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-118">Resource group name.</span></span>

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

### <span data-ttu-id="5d0f4-119">-SqlPoolName</span><span class="sxs-lookup"><span data-stu-id="5d0f4-119">-SqlPoolName</span></span>
<span data-ttu-id="5d0f4-120">Synapse SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-120">Name of Synapse SQL pool.</span></span>

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

### <span data-ttu-id="5d0f4-121">-SqlPoolObject</span><span class="sxs-lookup"><span data-stu-id="5d0f4-121">-SqlPoolObject</span></span>
<span data-ttu-id="5d0f4-122">SQL 입력 개체를 입력합니다. 일반적으로 파이프라인을 통해 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-122">SQL pool input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="5d0f4-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5d0f4-123">-WorkspaceName</span></span>
<span data-ttu-id="5d0f4-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="5d0f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d0f4-125">CommonParameters</span></span>
<span data-ttu-id="5d0f4-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d0f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d0f4-127">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5d0f4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d0f4-128">입력</span><span class="sxs-lookup"><span data-stu-id="5d0f4-128">INPUTS</span></span>

### <span data-ttu-id="5d0f4-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5d0f4-129">System.String</span></span>

### <span data-ttu-id="5d0f4-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span><span class="sxs-lookup"><span data-stu-id="5d0f4-130">Microsoft.Azure.Commands.Synapse.Models.PSSynapseSqlPool</span></span>

## <span data-ttu-id="5d0f4-131">출력</span><span class="sxs-lookup"><span data-stu-id="5d0f4-131">OUTPUTS</span></span>

### <span data-ttu-id="5d0f4-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="5d0f4-132">Microsoft.Azure.Commands.Synapse.Models.DataClassification.SqlPoolSensitivityClassificationModel</span></span>

## <span data-ttu-id="5d0f4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d0f4-133">NOTES</span></span>

## <span data-ttu-id="5d0f4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d0f4-134">RELATED LINKS</span></span>
