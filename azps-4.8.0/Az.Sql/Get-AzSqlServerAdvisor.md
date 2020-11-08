---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: DAEF11C1-281B-4BED-9283-2296E0B57018
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserveradvisor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerAdvisor.md
ms.openlocfilehash: 1d487c4397d1a7c29f0b415ee973d01e4dc6f1a1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048669"
---
# <span data-ttu-id="f68e2-101">Get-AzSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="f68e2-101">Get-AzSqlServerAdvisor</span></span>

## <span data-ttu-id="f68e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f68e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f68e2-103">Azure SQL Server에 대 한 하나 이상의 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-103">Gets one or more Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="f68e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f68e2-104">SYNTAX</span></span>

```
Get-AzSqlServerAdvisor [-AdvisorName <String>] [-ExpandRecommendedActions] -ServerName <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f68e2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f68e2-105">DESCRIPTION</span></span>
<span data-ttu-id="f68e2-106">**AzSqlServerAdvisor** Cmdlet은 azure sql server에 대 한 하나 이상의 Azure sql server 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-106">The **Get-AzSqlServerAdvisor** cmdlet gets one or more Azure SQL Server Advisors for an Azure SQL Server.</span></span>

## <span data-ttu-id="f68e2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f68e2-107">EXAMPLES</span></span>

### <span data-ttu-id="f68e2-108">예제 1: 서버의 모든 관리자 목록 표시</span><span class="sxs-lookup"><span data-stu-id="f68e2-108">Example 1: List all the advisors for the server</span></span>
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

<span data-ttu-id="f68e2-109">이 명령은 WIRunnersProd 이라는 리소스 그룹에 속하는 wi-러너-오스트레일리아-동부 서버에 대 한 모든 관리자의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-109">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd.</span></span>

### <span data-ttu-id="f68e2-110">예제 2: 서버에 대 한 단일 관리자 가져오기</span><span class="sxs-lookup"><span data-stu-id="f68e2-110">Example 2: Get a single advisor for the server</span></span>
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

<span data-ttu-id="f68e2-111">이 명령은 wi-러너-동부 라는 서버의 CreateIndex 라는 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-111">This command gets the advisor named CreateIndex for the server named wi-runner-australia-east.</span></span>

### <span data-ttu-id="f68e2-112">예제 3: 응답에 포함 된 모든 관리자의 추천 작업 나열</span><span class="sxs-lookup"><span data-stu-id="f68e2-112">Example 3: List all the advisors with their recommended actions included in the response</span></span>
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

<span data-ttu-id="f68e2-113">이 명령은 wi-러너-오스트레일리아 라는 서버에 대 한 모든 관리자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-113">This command gets all the advisors for the server named wi-runner-australia-east.</span></span>
<span data-ttu-id="f68e2-114">명령이 *ExpandRecommendedActions* 매개 변수를 사용 하기 때문에 cmdlet은 응답에 포함 된 관리자 권장 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-114">Since the command uses the *ExpandRecommendedActions* parameter, the cmdlet gets the advisors recommended actions included in the response.</span></span>

### <span data-ttu-id="f68e2-115">예제 4: 응답에 포함 된 권장 작업으로 단일 도우미 가져오기</span><span class="sxs-lookup"><span data-stu-id="f68e2-115">Example 4: Get a single advisor with its recommended actions included in the response</span></span>
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

<span data-ttu-id="f68e2-116">이 명령은 이름에 wi-러너-호주 서버 로부터 CreateIndex 라는 이름을 제공 하며 응답에는 권장 작업이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-116">This command gets advisor named CreateIndex from the server named wi-runner-australia-east with its recommended actions included in the response.</span></span>

### <span data-ttu-id="f68e2-117">예제 5: 필터링을 사용 하 여 서버의 모든 관리자 목록 표시</span><span class="sxs-lookup"><span data-stu-id="f68e2-117">Example 5: List all the advisors for the server using filtering</span></span>
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

<span data-ttu-id="f68e2-118">이 명령은 "d" 문자로 시작 하는 WIRunnersProd 이라는 리소스 그룹에 속하는 wi-러너-오스트레일리아-동부 서버의 모든 관리자 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-118">This command gets a list of all the advisors for the server named wi-runner-australia-east that belongs to the resource group named WIRunnersProd that start with the letter "d".</span></span>

## <span data-ttu-id="f68e2-119">변수</span><span class="sxs-lookup"><span data-stu-id="f68e2-119">PARAMETERS</span></span>

### <span data-ttu-id="f68e2-120">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="f68e2-120">-AdvisorName</span></span>
<span data-ttu-id="f68e2-121">이 cmdlet이 가져오는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-121">Specifies the name of the advisor that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f68e2-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f68e2-122">-DefaultProfile</span></span>
<span data-ttu-id="f68e2-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f68e2-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f68e2-124">-ExpandRecommendedActions</span><span class="sxs-lookup"><span data-stu-id="f68e2-124">-ExpandRecommendedActions</span></span>
<span data-ttu-id="f68e2-125">Cmdlet에 응답에 포함 된 관리자의 권장 작업이 포함 되어 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-125">Indicates that the cmdlet includes the recommended actions of the advisors that are included in the response.</span></span>

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

### <span data-ttu-id="f68e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f68e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="f68e2-127">서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-127">Specifies name of the resource group of the server.</span></span>

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

### <span data-ttu-id="f68e2-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f68e2-128">-ServerName</span></span>
<span data-ttu-id="f68e2-129">이 cmdlet이 요청 하는 관리자에 대 한 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-129">Specifies the name of the server for the advisor that this cmdlet requests.</span></span>

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

### <span data-ttu-id="f68e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f68e2-130">CommonParameters</span></span>
<span data-ttu-id="f68e2-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f68e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f68e2-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f68e2-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f68e2-133">입력</span><span class="sxs-lookup"><span data-stu-id="f68e2-133">INPUTS</span></span>

### <span data-ttu-id="f68e2-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f68e2-134">System.String</span></span>

### <span data-ttu-id="f68e2-135">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f68e2-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f68e2-136">출력</span><span class="sxs-lookup"><span data-stu-id="f68e2-136">OUTPUTS</span></span>

### <span data-ttu-id="f68e2-137">AzureSqlServerAdvisorModel을 (를).</span><span class="sxs-lookup"><span data-stu-id="f68e2-137">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlServerAdvisorModel</span></span>

## <span data-ttu-id="f68e2-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f68e2-138">NOTES</span></span>
* <span data-ttu-id="f68e2-139">키워드: azure, azurerm, arm, resource, 관리, manager, sql, server, mssql, advisor</span><span class="sxs-lookup"><span data-stu-id="f68e2-139">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor</span></span>

## <span data-ttu-id="f68e2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f68e2-140">RELATED LINKS</span></span>

[<span data-ttu-id="f68e2-141">Get-AzSqlElasticPoolAdvisor</span><span class="sxs-lookup"><span data-stu-id="f68e2-141">Get-AzSqlElasticPoolAdvisor</span></span>](./Get-AzSqlElasticPoolAdvisor.md)

[<span data-ttu-id="f68e2-142">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="f68e2-142">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="f68e2-143">Get-AzSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="f68e2-143">Get-AzSqlServerRecommendedAction</span></span>](./Get-AzSqlServerRecommendedAction.md)

[<span data-ttu-id="f68e2-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="f68e2-144">Set-AzSqlServerAdvisorAutoExecuteStatus</span></span>](./Set-AzSqlServerAdvisorAutoExecuteStatus.md)

[<span data-ttu-id="f68e2-145">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f68e2-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

