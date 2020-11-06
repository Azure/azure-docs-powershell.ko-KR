---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 26EC220C-5123-4CEF-8CC6-5FFD08F33481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverrecommendedactionstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerRecommendedActionState.md
ms.openlocfilehash: 5155b2f292b21af9696bee3ca70fca50850a7e73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526536"
---
# <span data-ttu-id="66f85-101">Set-AzureRmSqlServerRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f85-101">Set-AzureRmSqlServerRecommendedActionState</span></span>

## <span data-ttu-id="66f85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66f85-102">SYNOPSIS</span></span>
<span data-ttu-id="66f85-103">Azure SQL Server 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-103">Updates the state of an Azure SQL Server recommended action.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="66f85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="66f85-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerRecommendedActionState -RecommendedActionName <String> -State <RecommendedActionState>
 -ServerName <String> -AdvisorName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66f85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="66f85-105">DESCRIPTION</span></span>
<span data-ttu-id="66f85-106">Azure SQL Server 권장 작업의 **Set-AzureRmSqlServerRecommendedActionState** cmdlet 업데이트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-106">The **Set-AzureRmSqlServerRecommendedActionState** cmdlet updates state of an Azure SQL Server recommended action.</span></span>
<span data-ttu-id="66f85-107">이 cmdlet은 새 상태에 따라 권장 작업을 적용 하거나, 취소 하거나, 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-107">This cmdlet applies, reverts, or discards the recommended action based on the new state.</span></span>

## <span data-ttu-id="66f85-108">예제의</span><span class="sxs-lookup"><span data-stu-id="66f85-108">EXAMPLES</span></span>

### <span data-ttu-id="66f85-109">Example1: 지정 된 권장 작업의 상태를 보류 중으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-109">Example1: Update the state of the specified recommended action to Pending</span></span>
```
PS C:\>Set-AzureRmSqlServerRecommendedActionState -ResourceGroupName "WIRunnersProd" -ServerName "wi-runner-australia-east" -AdvisorName "CreateIndex" -RecommendedActionName "IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893" -State Pending
ResourceGroupName          : WIRunnersProd
ServerName                 : wi-runner-australia-east
AdvisorName                : CreateIndex
RecommendedActionName      : IR_[test_schema]_[test_table_0.0361551]_6C7AE8CC9C87E7FD5893
Details                    : {[indexName, nci_wi_test_table_0.0361551_6C7AE8CC9C87E7FD5893], [indexType, 
                             NONCLUSTERED], [schema, [test_schema]], [table, [test_table_0.0361551]]...} 
ErrorDetails               : Microsoft.Azure.Management.Sql.Models.RecommendedActionErrorInfo
EstimatedImpact            : {ActionDuration, SpaceChange}
ExecuteActionDuration      : PT1M
ExecuteActionInitiatedBy   : User
ExecuteActionInitiatedTime : 4/21/2016 3:24:47 PM
ExecuteActionStartTime     : 4/21/2016 3:24:47 PM
ImplementationDetails      : Microsoft.Azure.Management.Sql.Models.RecommendedActionImplementationInfo
IsArchivedAction           : False
IsExecutableAction         : True
IsRevertableAction         : True
LastRefresh                : 4/21/2016 3:24:47 PM
LinkedObjects              : {}
ObservedImpact             : {CpuUtilization, LogicalReads, LogicalWrites, QueriesWithImprovedPerformance...} 
RecommendationReason       : 
RevertActionDuration       : 
RevertActionInitiatedBy    : 
RevertActionInitiatedTime  : 
RevertActionStartTime      : 
Score                      : 2
State                      : Microsoft.Azure.Management.Sql.Models.RecommendedActionStateInfo
TimeSeries                 : {}
ValidSince                 : 4/21/2016 3:24:47 PM
```

<span data-ttu-id="66f85-110">"IR_ \[ test_schema \] _ \[ test_table_0 .0361551 \] _6C7AE8CC9C87E7FD5893"이 "보류 중" 인 서버 권장 작업의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-110">Updates state of server recommended action named "IR_\[test_schema\]_\[test_table_0.0361551\]_6C7AE8CC9C87E7FD5893" to "Pending"</span></span>

## <span data-ttu-id="66f85-111">변수</span><span class="sxs-lookup"><span data-stu-id="66f85-111">PARAMETERS</span></span>

### <span data-ttu-id="66f85-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="66f85-112">-AdvisorName</span></span>
<span data-ttu-id="66f85-113">권장 작업을 포함 하는 관리자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-113">Specifies the name of the advisor that contains the recommended action.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66f85-114">-DefaultProfile</span></span>
<span data-ttu-id="66f85-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="66f85-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-116">-RecommendedActionName</span><span class="sxs-lookup"><span data-stu-id="66f85-116">-RecommendedActionName</span></span>
<span data-ttu-id="66f85-117">이 cmdlet이 상태를 업데이트 하는 데 권장 되는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-117">Specifies the name of the recommended action for which this cmdlet updates the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66f85-118">-ResourceGroupName</span></span>
<span data-ttu-id="66f85-119">서버의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-119">Specifies the name of the resource group of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="66f85-120">-ServerName</span></span>
<span data-ttu-id="66f85-121">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-121">Specifies the name of the server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-122">-상태</span><span class="sxs-lookup"><span data-stu-id="66f85-122">-State</span></span>
<span data-ttu-id="66f85-123">이 cmdlet이 권장 동작 상태를 업데이트 하는 새 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-123">Specifies the new value to which this cmdlet updates the recommended action state.</span></span>

<span data-ttu-id="66f85-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="66f85-125">활성</span><span class="sxs-lookup"><span data-stu-id="66f85-125">Active</span></span>
- <span data-ttu-id="66f85-126">중일</span><span class="sxs-lookup"><span data-stu-id="66f85-126">Pending</span></span>
- <span data-ttu-id="66f85-127">PendingRevert</span><span class="sxs-lookup"><span data-stu-id="66f85-127">PendingRevert</span></span>
- <span data-ttu-id="66f85-128">RevertCancelled</span><span class="sxs-lookup"><span data-stu-id="66f85-128">RevertCancelled</span></span>
- <span data-ttu-id="66f85-129">무시할</span><span class="sxs-lookup"><span data-stu-id="66f85-129">Ignored</span></span>
- <span data-ttu-id="66f85-130">됨으로</span><span class="sxs-lookup"><span data-stu-id="66f85-130">Resolved</span></span>

```yaml
Type: RecommendedActionState
Parameter Sets: (All)
Aliases:
Accepted values: Active, Pending, PendingRevert, RevertCancelled, Ignored, Resolved

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-131">-확인</span><span class="sxs-lookup"><span data-stu-id="66f85-131">-Confirm</span></span>
<span data-ttu-id="66f85-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66f85-133">-WhatIf</span></span>
<span data-ttu-id="66f85-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66f85-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66f85-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66f85-136">CommonParameters</span></span>
<span data-ttu-id="66f85-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66f85-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66f85-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66f85-139">입력</span><span class="sxs-lookup"><span data-stu-id="66f85-139">INPUTS</span></span>

### <span data-ttu-id="66f85-140">않아야</span><span class="sxs-lookup"><span data-stu-id="66f85-140">None</span></span>
<span data-ttu-id="66f85-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66f85-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="66f85-142">출력</span><span class="sxs-lookup"><span data-stu-id="66f85-142">OUTPUTS</span></span>

### <span data-ttu-id="66f85-143">RecommendedAction. AzureSqlServerRecommendedActionModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="66f85-143">Microsoft.Azure.Commands.Sql.RecommendedAction.Model.AzureSqlServerRecommendedActionModel</span></span>

## <span data-ttu-id="66f85-144">상속자</span><span class="sxs-lookup"><span data-stu-id="66f85-144">NOTES</span></span>
* <span data-ttu-id="66f85-145">키워드: azure, azurerm, arm, resource, 관리, manager, sql, server, mssql, advisor, recommendedaction</span><span class="sxs-lookup"><span data-stu-id="66f85-145">Keywords: azure, azurerm, arm, resource, management, manager, sql, server, mssql, advisor, recommendedaction</span></span>

## <span data-ttu-id="66f85-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66f85-146">RELATED LINKS</span></span>

[<span data-ttu-id="66f85-147">Get-AzureRmSqlServerAdvisor</span><span class="sxs-lookup"><span data-stu-id="66f85-147">Get-AzureRmSqlServerAdvisor</span></span>](./Get-AzureRmSqlServerAdvisor.md)

[<span data-ttu-id="66f85-148">Get-AzureRmSqlServerRecommendedAction</span><span class="sxs-lookup"><span data-stu-id="66f85-148">Get-AzureRmSqlServerRecommendedAction</span></span>](./Get-AzureRmSqlServerRecommendedAction.md)

[<span data-ttu-id="66f85-149">Set-AzureRmSqlDatabaseRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f85-149">Set-AzureRmSqlDatabaseRecommendedActionState</span></span>](./Set-AzureRmSqlDatabaseRecommendedActionState.md)

[<span data-ttu-id="66f85-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span><span class="sxs-lookup"><span data-stu-id="66f85-150">Set-AzureRmSqlElasticPoolRecommendedActionState</span></span>](./Set-AzureRmSqlElasticPoolRecommendedActionState.md)

[<span data-ttu-id="66f85-151">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="66f85-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
