---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98350102"
---
# <span data-ttu-id="dee99-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="dee99-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="dee99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dee99-102">SYNOPSIS</span></span>
<span data-ttu-id="dee99-103">Azure 리소스에 대한 하나 이상의 Advisor를 SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dee99-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="dee99-104">구문</span><span class="sxs-lookup"><span data-stu-id="dee99-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dee99-105">설명</span><span class="sxs-lookup"><span data-stu-id="dee99-105">DESCRIPTION</span></span>
<span data-ttu-id="dee99-106">**Get-AzSqlServerAdvisor** cmdlet은 하나 이상의 Azure SQL Server Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dee99-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="dee99-107">예제</span><span class="sxs-lookup"><span data-stu-id="dee99-107">EXAMPLES</span></span>

### <span data-ttu-id="dee99-108">예제 1: 서버에 대한 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="dee99-108">Example 1: List all the advisors for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east"
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}

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

<span data-ttu-id="dee99-109">이 명령은 WIRunnersProd라는 리소스 그룹에 속하는 wi-runner-australia-east 서버의 모든 Advisor 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="dee99-110">예제 2: 서버에 대한 단일 Advisor를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-110">Example 2: Get a single advisor for the server</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex"
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

<span data-ttu-id="dee99-111">이 명령은 wi-runner-australia-east라는 서버에 대해 CreateIndex라는 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="dee99-112">예제 3: 응답에 포함된 권장 작업과 함께 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="dee99-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
```
PS C:\>Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -ExpandRecommendedActions
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

ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DbParameterization
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Default
LastChecked                    : 7/31/2016 2:46:58 PM
RecommendationsStatus          : NoDbParameterizationIssue
RecommendedActions             : {}
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

<span data-ttu-id="dee99-113">이 명령은 wi-runner-australia-east라는 서버에 대한 모든 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="dee99-114">이 명령은 *ExpandRecommendedActions* 매개 변수를 사용하기 때문에 cmdlet은 응답에 포함된 Advisor 권장 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="dee99-115">예제 4: 응답에 포함된 권장 작업을 통해 단일 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -ExpandRecommendedActions
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

<span data-ttu-id="dee99-116">이 명령은 응답에 포함된 권장 작업을 사용하여 wi-runner-australia-east라는 서버에서 CreateIndex라는 Advisor를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="dee99-117">예제 5: 필터링을 사용하여 서버에 대한 모든 Advisor 나열</span><span class="sxs-lookup"><span data-stu-id="dee99-117">Example 5: List all the advisors for the server using filtering</span></span>
```
PS C:\> Get-AzSqlServerAdvisor -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName d*
ResourceGroupName              : WIRunnersProd
ServerName                     : wi-runner-australia-east
AdvisorName                    : DropIndex
AdvisorStatus                  : PublicPreview
AutoExecuteStatus              : Disabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 7/31/2016 8:41:19 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}

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

<span data-ttu-id="dee99-118">이 명령은 문자 "d"로 시작하는 WIRunnersProd라는 리소스 그룹에 속하는 wi-runner-australia-east이라는 서버에 대한 모든 Advisor 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="dee99-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dee99-119">PARAMETERS</span></span>

### <span data-ttu-id="dee99-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="dee99-120">-AdvisorName</span></span>
<span data-ttu-id="dee99-121">이 cmdlet이 얻을 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="dee99-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dee99-122">-DefaultProfile</span></span>
<span data-ttu-id="dee99-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dee99-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dee99-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="dee99-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="dee99-125">cmdlet이 응답에 포함된 Advisor의 권장 작업을 포함함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="dee99-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dee99-126">-ResourceGroupName</span></span>
<span data-ttu-id="dee99-127">서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="dee99-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dee99-128">-ServerName</span></span>
<span data-ttu-id="dee99-129">이 cmdlet이 요청하는 Advisor의 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="dee99-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dee99-130">CommonParameters</span></span>
<span data-ttu-id="dee99-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dee99-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dee99-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dee99-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dee99-133">입력</span><span class="sxs-lookup"><span data-stu-id="dee99-133">INPUTS</span></span>

### <span data-ttu-id="dee99-134">System.String</span><span class="sxs-lookup"><span data-stu-id="dee99-134">System.String</span></span>

### <span data-ttu-id="dee99-135">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dee99-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="dee99-136">출력</span><span class="sxs-lookup"><span data-stu-id="dee99-136">OUTPUTS</span></span>

### <span data-ttu-id="dee99-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="dee99-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="dee99-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dee99-138">NOTES</span></span>
* <span data-ttu-id="dee99-139">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, sql, 서버, mssql, 관리자</span><span class="sxs-lookup"><span data-stu-id="dee99-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="dee99-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dee99-140">RELATED LINKS</span></span>

[<span data-ttu-id="dee99-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="dee99-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="dee99-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="dee99-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="dee99-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="dee99-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="dee99-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="dee99-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="dee99-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="dee99-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

