---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: f002dca1c91ada808acc81108d3f06e9376a8b3f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191121"
---
# <span data-ttu-id="89bbc-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="89bbc-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="89bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="89bbc-103">데이터베이스의 열에 대한 권장 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="89bbc-104">구문</span><span class="sxs-lookup"><span data-stu-id="89bbc-104">SYNTAX</span></span>

### <span data-ttu-id="89bbc-105">DatabaseObjectParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="89bbc-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89bbc-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="89bbc-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89bbc-107">설명</span><span class="sxs-lookup"><span data-stu-id="89bbc-107">DESCRIPTION</span></span>
<span data-ttu-id="89bbc-108">Get-AzSqlDatabaseSensitivityRecommendation cmdlet은 데이터베이스에 있는 열의 권장 정보 유형 및 민감도 레이블을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="89bbc-109">예제</span><span class="sxs-lookup"><span data-stu-id="89bbc-109">EXAMPLES</span></span>

### <span data-ttu-id="89bbc-110">예제 1: Azure SQL 데이터베이스의 권장 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
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

### <span data-ttu-id="89bbc-111">예제 2: Piping을 사용하여 Azure SQL 데이터베이스의 권장 정보 유형 및 민감도 레이블을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
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

## <span data-ttu-id="89bbc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89bbc-112">PARAMETERS</span></span>

### <span data-ttu-id="89bbc-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="89bbc-113">-AsJob</span></span>
<span data-ttu-id="89bbc-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="89bbc-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="89bbc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="89bbc-115">-DatabaseName</span></span>
<span data-ttu-id="89bbc-116">Azure SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-116">The name of the Azure SQL database.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbc-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="89bbc-117">-DatabaseObject</span></span>
<span data-ttu-id="89bbc-118">SQL 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-118">The SQL database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89bbc-119">-DefaultProfile</span></span>
<span data-ttu-id="89bbc-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89bbc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89bbc-121">-ResourceGroupName</span></span>
<span data-ttu-id="89bbc-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-122">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbc-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="89bbc-123">-ServerName</span></span>
<span data-ttu-id="89bbc-124">SQL 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-124">SQL server name.</span></span>

```yaml
Type: System.String
Parameter Sets: DatabaseParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89bbc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89bbc-125">CommonParameters</span></span>
<span data-ttu-id="89bbc-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89bbc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89bbc-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89bbc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89bbc-128">입력</span><span class="sxs-lookup"><span data-stu-id="89bbc-128">INPUTS</span></span>

### <span data-ttu-id="89bbc-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="89bbc-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="89bbc-130">출력</span><span class="sxs-lookup"><span data-stu-id="89bbc-130">OUTPUTS</span></span>

### <span data-ttu-id="89bbc-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span><span class="sxs-lookup"><span data-stu-id="89bbc-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="89bbc-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89bbc-132">NOTES</span></span>

## <span data-ttu-id="89bbc-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89bbc-133">RELATED LINKS</span></span>

[<span data-ttu-id="89bbc-134">Azure SQL 데이터베이스 데이터 검색 및 분류에 대해 자세히 알아보기</span><span class="sxs-lookup"><span data-stu-id="89bbc-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
