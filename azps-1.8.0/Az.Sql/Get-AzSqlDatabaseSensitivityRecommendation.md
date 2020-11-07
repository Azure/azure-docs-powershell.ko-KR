---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseSensitivityRecommendation.md
ms.openlocfilehash: ba8229bcddf27a2a14d50efc2cbd32e6e47015c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699013"
---
# <span data-ttu-id="81d29-101">Get-AzSqlDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="81d29-101">Get-AzSqlDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="81d29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81d29-102">SYNOPSIS</span></span>
<span data-ttu-id="81d29-103">데이터베이스의 열에 대 한 권장 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-103">Gets the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="81d29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81d29-104">SYNTAX</span></span>

### <span data-ttu-id="81d29-105">DatabaseObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="81d29-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="81d29-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="81d29-106">DatabaseParameterSet</span></span>
```
Get-AzSqlDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-ServerName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d29-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81d29-107">DESCRIPTION</span></span>
<span data-ttu-id="81d29-108">Get-AzSqlDatabaseSensitivityRecommendation cmdlet은 데이터베이스의 열에 대 한 권장 정보 유형 및 민감도 레이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-108">The Get-AzSqlDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the database.</span></span>

## <span data-ttu-id="81d29-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81d29-109">EXAMPLES</span></span>

### <span data-ttu-id="81d29-110">예제 1: Azure SQL 데이터베이스의 권장 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL database.</span></span>
```powershell
PS C:\> Get-AzSqlDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -ServerName server -DatabaseName database

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

### <span data-ttu-id="81d29-111">예제 2: 파이핑을 사용 하 여 Azure SQL 데이터베이스의 추천 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlDatabase -ResourceGroupName resourceGroup -ServerName server -DatabaseName database | Get-AzSqlDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
ServerName        : server
DatabaseName      : database
SensitivityLabels : {{
                        SchemaName: schema1,
                        TableName: table1,
                        ColumnName: column1,
                        SensitivityLabel: label1,
                        InformationType: informationType1,
                    }, {
                        SchemaName: schema2,
                        TableName: table2,
                        ColumnName: column2,
                        SensitivityLabel: label2,
                    }, {
                        SchemaName: schema3,
                        TableName: table3,
                        ColumnName: column3,
                        SensitivityLabel: label3,
                    }}
```

## <span data-ttu-id="81d29-112">변수</span><span class="sxs-lookup"><span data-stu-id="81d29-112">PARAMETERS</span></span>

### <span data-ttu-id="81d29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="81d29-113">-AsJob</span></span>
<span data-ttu-id="81d29-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="81d29-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="81d29-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="81d29-115">-DatabaseName</span></span>
<span data-ttu-id="81d29-116">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-116">The name of the Azure SQL database.</span></span>

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

### <span data-ttu-id="81d29-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="81d29-117">-DatabaseObject</span></span>
<span data-ttu-id="81d29-118">SQL 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-118">The SQL database object.</span></span>

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

### <span data-ttu-id="81d29-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d29-119">-DefaultProfile</span></span>
<span data-ttu-id="81d29-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81d29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d29-121">-ResourceGroupName</span></span>
<span data-ttu-id="81d29-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="81d29-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="81d29-123">-ServerName</span></span>
<span data-ttu-id="81d29-124">SQL server 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-124">SQL server name.</span></span>

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

### <span data-ttu-id="81d29-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d29-125">CommonParameters</span></span>
<span data-ttu-id="81d29-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81d29-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d29-127">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="81d29-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d29-128">입력</span><span class="sxs-lookup"><span data-stu-id="81d29-128">INPUTS</span></span>

### <span data-ttu-id="81d29-129">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="81d29-129">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="81d29-130">출력</span><span class="sxs-lookup"><span data-stu-id="81d29-130">OUTPUTS</span></span>

### <span data-ttu-id="81d29-131">DataClassification. SqlDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="81d29-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.SqlDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="81d29-132">상속자</span><span class="sxs-lookup"><span data-stu-id="81d29-132">NOTES</span></span>

## <span data-ttu-id="81d29-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81d29-133">RELATED LINKS</span></span>

[<span data-ttu-id="81d29-134">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="81d29-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
