---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BC8C0D59-662F-47D2-8619-9F69D78B171D
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlelasticpooladvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolAdvisor.md
ms.openlocfilehash: 9c9a6b2b95f5126ecdc214db2227c46b01c5725c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999536"
---
# <span data-ttu-id="8019c-101">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="8019c-101">Get-AzSqlElasticPoolAdvisor</span></span>

## <span data-ttu-id="8019c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8019c-102">SYNOPSIS</span></span>
<span data-ttu-id="8019c-103">Azure SQL 탄력적 풀에 대한 하나 이상의 SQL 합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-103">Gets one or more Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="8019c-104">구문</span><span class="sxs-lookup"><span data-stu-id="8019c-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 -ElasticPoolName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8019c-105">설명</span><span class="sxs-lookup"><span data-stu-id="8019c-105">DESCRIPTION</span></span>
<span data-ttu-id="8019c-106">**Get-AzSqlElasticPoolAdvisor** cmdlet은 Azure SQL 탄력적 풀에 대한 하나 이상의 Azure SQL 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-106">The **Get-AzSqlElasticPoolAdvisor** cmdlet gets one or more Azure SQL Elastic Pool Advisors for an Azure SQL Elastic Pool.</span></span>

## <span data-ttu-id="8019c-107">예제</span><span class="sxs-lookup"><span data-stu-id="8019c-107">EXAMPLES</span></span>

### <span data-ttu-id="8019c-108">예제 1: 지정된 탄력적 풀에 대한 모든 어드바이저 나열</span><span class="sxs-lookup"><span data-stu-id="8019c-108">Example 1: List all the advisors for the specified elastic pool</span></span>
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

<span data-ttu-id="8019c-109">명령은 WIRunnerPool이라는 탄력적 풀에 대한 모든 어드바이저를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-109">The command gets lists all the advisors for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="8019c-110">예제 2: 지정된 탄력적 풀에 대한 단일 고문을 얻다</span><span class="sxs-lookup"><span data-stu-id="8019c-110">Example 2: Get a single advisor for the specified elastic pool</span></span>
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

<span data-ttu-id="8019c-111">이 명령은 WIRunnerPool이라는 탄력적 풀에 대해 CreateIndex라는 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-111">This command gets the Advisor named CreateIndex for the elastic pool named WIRunnerPool.</span></span>

### <span data-ttu-id="8019c-112">예제 3: 응답에 포함된 권장 작업과 함께 모든 고문 나열</span><span class="sxs-lookup"><span data-stu-id="8019c-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="8019c-113">이 명령은 응답에 포함된 권장 작업을 사용하여 탄력적 풀에 대한 모든 어드바이저를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-113">This command gets all the advisors for the elastic pool with their recommended actions included in the response.</span></span>

### <span data-ttu-id="8019c-114">예제 4: 응답에 포함된 권장 작업으로 단일 고문을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-114">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="8019c-115">이 명령은 응답에 포함된 권장 작업을 사용하여 wi-runner-australia-east라는 서버에서 CreateIndex라는 어드바이저를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-115">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="8019c-116">예제 5: 필터링을 사용하여 지정된 탄력적 풀에 대한 모든 어드바이저 나열</span><span class="sxs-lookup"><span data-stu-id="8019c-116">Example 5: List all the advisors for the specified elastic pool using filtering</span></span>
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

<span data-ttu-id="8019c-117">명령은 "d"로 시작하는 WIRunnerPool이라는 탄력적 풀에 대한 모든 어드바이저를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-117">The command gets lists all the advisors for the elastic pool named WIRunnerPool that start with the letter "d".</span></span>

## <span data-ttu-id="8019c-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8019c-118">PARAMETERS</span></span>

### <span data-ttu-id="8019c-119">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="8019c-119">-AdvisorName</span></span>
<span data-ttu-id="8019c-120">이 cmdlet이 도착하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-120">Specifies the name of the Advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8019c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8019c-121">-DefaultProfile</span></span>
<span data-ttu-id="8019c-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8019c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8019c-123">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8019c-123">-ElasticPoolName</span></span>
<span data-ttu-id="8019c-124">이 cmdlet에서 Advisor를 요청하는 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-124">Specifies the name of the elastic pool for which this cmdlet requests the Advisor.</span></span>

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

### <span data-ttu-id="8019c-125">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="8019c-125">-ExpandRecommendedActions</span></span>
<span data-ttu-id="8019c-126">cmdlet에 응답에서 Advisor의 권장된 작업이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-126">Indicates that the cmdlet includes the recommended actions of the Advisor in the response.</span></span>

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

### <span data-ttu-id="8019c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8019c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8019c-128">이 탄력적 풀을 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-128">Specifies the name of the resource group of the server that contains this elastic pool.</span></span>

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

### <span data-ttu-id="8019c-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8019c-129">-ServerName</span></span>
<span data-ttu-id="8019c-130">탄력적 풀이 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-130">Specifies the name of the server the elastic pool is in.</span></span>

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

### <span data-ttu-id="8019c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8019c-131">CommonParameters</span></span>
<span data-ttu-id="8019c-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8019c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8019c-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8019c-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8019c-134">입력</span><span class="sxs-lookup"><span data-stu-id="8019c-134">INPUTS</span></span>

### <span data-ttu-id="8019c-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8019c-135">System.String</span></span>

### <span data-ttu-id="8019c-136">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8019c-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8019c-137">출력</span><span class="sxs-lookup"><span data-stu-id="8019c-137">OUTPUTS</span></span>

### <span data-ttu-id="8019c-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="8019c-138">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlElasticPoolAdvisorModel</span></span>

## <span data-ttu-id="8019c-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8019c-139">NOTES</span></span>
* <span data-ttu-id="8019c-140">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, elasticpool, mssql, 고문</span><span class="sxs-lookup"><span data-stu-id="8019c-140">Keywords: azure, azurerm, arm, resource, management, manager, sql, elasticpool, mssql, advisor</span></span>

## <span data-ttu-id="8019c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8019c-141">RELATED LINKS</span></span>

[<span data-ttu-id="8019c-142">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="8019c-142">Get-AzSqlServerAdvisor</span></span>](./Get-AzSqlServerAdvisor.md)

[<span data-ttu-id="8019c-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="8019c-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="8019c-144">Get-AzSqlElasticPoolRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="8019c-144">Get-AzSqlElasticPoolRecommendedAction</span></span>](./Get-AzSqlElasticPoolRecommendedAction.md)

[<span data-ttu-id="8019c-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="8019c-145">Set-AzSqlElasticPoolAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlElasticPoolAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="8019c-146">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8019c-146">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
