---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 14814BF3-51AF-4E51-A8A6-661825BD88D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseSensitivityRecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseSensitivityRecommendation.md
ms.openlocfilehash: cf9250080e0d8e079257a4996b7d263bd96a2093
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048676"
---
# <span data-ttu-id="423cf-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span><span class="sxs-lookup"><span data-stu-id="423cf-101">Get-AzSqlInstanceDatabaseSensitivityRecommendation</span></span>

## <span data-ttu-id="423cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="423cf-102">SYNOPSIS</span></span>
<span data-ttu-id="423cf-103">Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 권장 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-103">Gets the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="423cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="423cf-104">SYNTAX</span></span>

### <span data-ttu-id="423cf-105">DatabaseObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="423cf-105">DatabaseObjectParameterSet (Default)</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation -DatabaseObject <AzureSqlManagedDatabaseModel> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="423cf-106">DatabaseParameterSet</span><span class="sxs-lookup"><span data-stu-id="423cf-106">DatabaseParameterSet</span></span>
```
Get-AzSqlInstanceDatabaseSensitivityRecommendation [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DatabaseName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="423cf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="423cf-107">DESCRIPTION</span></span>
<span data-ttu-id="423cf-108">Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet은 Azure SQL 관리 인스턴스 데이터베이스의 열에 대 한 권장 정보 유형 및 민감도 레이블을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-108">The Get-AzSqlInstanceDatabaseSensitivityRecommendation cmdlet returns the recommended information types and sensitivity labels of columns in the Azure SQL managed instance database.</span></span>

## <span data-ttu-id="423cf-109">예제의</span><span class="sxs-lookup"><span data-stu-id="423cf-109">EXAMPLES</span></span>

### <span data-ttu-id="423cf-110">예제 1: Azure SQL 관리 인스턴스 데이터베이스의 권장 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-110">Example 1: Get recommended information types and sensitivity labels of an Azure SQL managed instance database.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseSensitivityRecommendation -ResourceGroupName resourceGroup -InstanceName managedInstance -DatabaseName database

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

### <span data-ttu-id="423cf-111">예제 2: 파이핑을 사용 하 여 Azure SQL 관리 인스턴스 데이터베이스의 권장 정보 유형 및 민감도 레이블을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-111">Example 2: Get recommended information types and sensitivity labels of an Azure SQL managed instance database using Piping.</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabase -ResourceGroupName resourceGroup -InstanceName managedInstance -Name database | Get-AzSqlInstanceDatabaseSensitivityRecommendation

ResourceGroupName : resourceGroup
InstanceName      : managedInstance
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

## <span data-ttu-id="423cf-112">변수</span><span class="sxs-lookup"><span data-stu-id="423cf-112">PARAMETERS</span></span>

### <span data-ttu-id="423cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="423cf-113">-AsJob</span></span>
<span data-ttu-id="423cf-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="423cf-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="423cf-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="423cf-115">-DatabaseName</span></span>
<span data-ttu-id="423cf-116">Azure SQL 관리 인스턴스 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-116">The name of the Azure SQL managed instance database.</span></span>

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

### <span data-ttu-id="423cf-117">-DatabaseObject</span><span class="sxs-lookup"><span data-stu-id="423cf-117">-DatabaseObject</span></span>
<span data-ttu-id="423cf-118">Azure SQL 관리 되는 인스턴스 데이터베이스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-118">The Azure SQL managed instance database object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel
Parameter Sets: DatabaseObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="423cf-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="423cf-119">-DefaultProfile</span></span>
<span data-ttu-id="423cf-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="423cf-121">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="423cf-121">-InstanceName</span></span>
<span data-ttu-id="423cf-122">Azure SQL 관리 되는 인스턴스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-122">Azure SQL managed instance name.</span></span>

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

### <span data-ttu-id="423cf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="423cf-123">-ResourceGroupName</span></span>
<span data-ttu-id="423cf-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="423cf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="423cf-125">CommonParameters</span></span>
<span data-ttu-id="423cf-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="423cf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="423cf-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="423cf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="423cf-128">입력</span><span class="sxs-lookup"><span data-stu-id="423cf-128">INPUTS</span></span>

### <span data-ttu-id="423cf-129">AzureSqlManagedDatabaseModel (. \*. \*)</span><span class="sxs-lookup"><span data-stu-id="423cf-129">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseModel</span></span>

## <span data-ttu-id="423cf-130">출력</span><span class="sxs-lookup"><span data-stu-id="423cf-130">OUTPUTS</span></span>

### <span data-ttu-id="423cf-131">DataClassification. ManagedDatabaseSensitivityClassificationModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="423cf-131">Microsoft.Azure.Commands.Sql.DataClassification.Model.ManagedDatabaseSensitivityClassificationModel</span></span>

## <span data-ttu-id="423cf-132">상속자</span><span class="sxs-lookup"><span data-stu-id="423cf-132">NOTES</span></span>

## <span data-ttu-id="423cf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="423cf-133">RELATED LINKS</span></span>

[<span data-ttu-id="423cf-134">Azure SQL 데이터베이스 데이터 검색 및 분류에 대 한 자세한 정보</span><span class="sxs-lookup"><span data-stu-id="423cf-134">Learn more about Azure SQL Database data discovery and classification</span></span>](https://docs.microsoft.com/en-us/azure/sql-database/sql-database-data-discovery-and-classification)
