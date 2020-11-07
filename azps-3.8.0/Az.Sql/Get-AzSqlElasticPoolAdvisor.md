---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 3032824d51e7892c21830decbdb1c92d03d7a2e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879641"
---
# <span data-ttu-id="c1de8-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="c1de8-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="c1de8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1de8-102">SYNOPSIS</span></span>
<span data-ttu-id="c1de8-103">Azure SQL 탄력적 풀에 대 한 하나 이상의 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="c1de8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1de8-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c1de8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1de8-105">DESCRIPTION</span></span>
<span data-ttu-id="c1de8-106">**AzSqlElasticPoolAdvisor** Cmdlet은 Azure Sql 탄력적 풀에 대 한 하나 이상의 Azure Sql 탄력적인 풀 확인 프로그램을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="c1de8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1de8-107">EXAMPLES</span></span>

### <span data-ttu-id="c1de8-108">예제 1: 지정 된 탄력적 풀의 모든 관리자 목록 표시</span><span class="sxs-lookup"><span data-stu-id="c1de8-108">Example 1: List all the advisors for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:01:41 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="c1de8-109">명령에 WIRunnerPool 이라는 탄력적 풀에 대 한 모든 관리자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="c1de8-110">예제 2: 지정 된 탄력적 풀에 대 한 단일 관리자 가져오기</span><span class="sxs-lookup"><span data-stu-id="c1de8-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex"
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="c1de8-111">이 명령은 WIRunnerPool 이라는 탄력적 풀에 대 한 CreateIndex 라는 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="c1de8-112">예제 3: 응답에 포함 된 모든 관리자의 추천 작업 나열</span><span class="sxs-lookup"><span data-stu-id="c1de8-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...} 

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0288891]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.140264]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.412191]_38724E1DCF2178318957, 
                                 IR_[test_schema]_[test_table_0.442075]_38724E1DCF2178318957...} 

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : SchemaIssue
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 8/1/2016 3:04:26 PM
RecommendationsStatus          : SchemaIsConsistent
RecommendedActions             : {}
```

<span data-ttu-id="c1de8-113">이 명령은 응답에 포함 된 권장 작업과 함께 탄력적 풀에 대 한 모든 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="c1de8-114">예제 4: 응답에 포함 된 권장 작업으로 단일 도우미 가져오기</span><span class="sxs-lookup"><span data-stu-id="c1de8-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName "CreateIndex" -ExpandRecommendedActions
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.236046]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.239359]_6C7AE8CC9C87E7FD5893, 
                                 IR_[test_schema]_[test_table_0.437714]_6C7AE8CC9C87E7FD5893...}
```

<span data-ttu-id="c1de8-115">이 명령은 이름에 wi-러너-호주 서버 로부터 CreateIndex 라는 이름을 제공 하며 응답에는 권장 작업이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="c1de8-116">예제 5: 필터링을 사용 하 여 지정 된 탄력적 풀의 모든 관리자 목록 표시</span><span class="sxs-lookup"><span data-stu-id="c1de8-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
```
PS C:\>Get-AzSqlElasticPoolAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ElasticPoolName "WIRunnerPool" -AdvisorName d*
ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ElasticPoolName                : WIRunnerPool
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
```

<span data-ttu-id="c1de8-117">명령에는 "d" 문자로 시작 하는 WIRunnerPool 이라는 탄력적 풀에 대 한 모든 관리자가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="c1de8-118">변수</span><span class="sxs-lookup"><span data-stu-id="c1de8-118">PARAMETERS</span></span>

### <span data-ttu-id="c1de8-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="c1de8-119">-AdvisorName</span></span>
<span data-ttu-id="c1de8-120">이 cmdlet이 가져오는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1de8-121">-DefaultProfile</span></span>
<span data-ttu-id="c1de8-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c1de8-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1de8-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="c1de8-123">-ElasticPoolName</span></span>
<span data-ttu-id="c1de8-124">이 cmdlet이 관리자를 요청 하는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de8-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="c1de8-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="c1de8-126">Cmdlet에 해당 응답의 관리자에 대 한 권장 작업이 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1de8-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1de8-128">이 탄력적 풀을 포함 하는 서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de8-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c1de8-129">-ServerName</span></span>
<span data-ttu-id="c1de8-130">탄력적 풀이 있는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-130">Specifies the name of the server the elastic pool is in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1de8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1de8-131">CommonParameters</span></span>
<span data-ttu-id="c1de8-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1de8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1de8-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1de8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1de8-134">입력</span><span class="sxs-lookup"><span data-stu-id="c1de8-134">INPUTS</span></span>

### <span data-ttu-id="c1de8-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1de8-135">System.String</span></span>

### <span data-ttu-id="c1de8-136">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c1de8-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c1de8-137">출력</span><span class="sxs-lookup"><span data-stu-id="c1de8-137">OUTPUTS</span></span>

### <span data-ttu-id="c1de8-138">AzureSqlElasticPoolAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="c1de8-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="c1de8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c1de8-139">NOTES</span></span>
* <span data-ttu-id="c1de8-140">키워드: azure, azurerm, arm, resource, 관리, manager, sql, elasticpool, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="c1de8-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="c1de8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1de8-141">RELATED LINKS</span></span>

[<span data-ttu-id="c1de8-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="c1de8-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="c1de8-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="c1de8-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="c1de8-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="c1de8-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="c1de8-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="c1de8-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="c1de8-146">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="c1de8-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
