---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 1d6348c5ede63dee1f76059277c8f7d142a2c327
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191001"
---
# <span data-ttu-id="76f64-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="76f64-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="76f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76f64-102">SYNOPSIS</span></span>
<span data-ttu-id="76f64-103">Azure SQL Database Advisor의 자동 실행 상태를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="76f64-104">구문</span><span class="sxs-lookup"><span data-stu-id="76f64-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76f64-105">설명</span><span class="sxs-lookup"><span data-stu-id="76f64-105">DESCRIPTION</span></span>
<span data-ttu-id="76f64-106">**Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet은 Azure SQL Database Advisor에 대한 자동 실행 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="76f64-107">현재 이 cmdlet은 Enabled, Disabled 및 Default 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="76f64-108">예제</span><span class="sxs-lookup"><span data-stu-id="76f64-108">EXAMPLES</span></span>

### <span data-ttu-id="76f64-109">예제 1: Advisor에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="76f64-109">Example 1: Enable auto execute for an advisor</span></span>
```
PS C:\>Set-AzSqlDatabaseAdvisorAutoExecuteStatus -ResourceGroupName "ContosoRunnersProd" -ServerName "runner-australia-east" -DatabaseName "ContosoRunner" -AdvisorName "CreateIndex" -AutoExecuteStatus Enabled
DatabaseName                   : ContosoRunner
ResourceGroupName              : ContosoRunnersProd
ServerName                     : runner-australia-east
AdvisorName                    : CreateIndex
AdvisorStatus                  : GA
AutoExecuteStatus              : Enabled
AutoExecuteStatusInheritedFrom : Database
LastChecked                    : 8/1/2016 2:36:47 PM
RecommendationsStatus          : Ok
RecommendedActions             : {}
```

<span data-ttu-id="76f64-110">이 명령은 CreateIndex라는 Advisor의 자동 실행 상태를 Enabled로 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="76f64-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76f64-111">PARAMETERS</span></span>

### <span data-ttu-id="76f64-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="76f64-112">-AdvisorName</span></span>
<span data-ttu-id="76f64-113">이 cmdlet이 상태를 수정하는 Advisor의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="76f64-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="76f64-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="76f64-115">상태에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-115">Specifies the value for the status.</span></span>
<span data-ttu-id="76f64-116">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="76f64-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="76f64-117">사용</span><span class="sxs-lookup"><span data-stu-id="76f64-117">Enabled</span></span> 
- <span data-ttu-id="76f64-118">사용 안</span><span class="sxs-lookup"><span data-stu-id="76f64-118">Disabled</span></span> 
- <span data-ttu-id="76f64-119">기본값</span><span class="sxs-lookup"><span data-stu-id="76f64-119">Default</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled, Default

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76f64-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="76f64-120">-DatabaseName</span></span>
<span data-ttu-id="76f64-121">이 cmdlet이 상태를 수정하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="76f64-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76f64-122">-DefaultProfile</span></span>
<span data-ttu-id="76f64-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="76f64-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76f64-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76f64-124">-ResourceGroupName</span></span>
<span data-ttu-id="76f64-125">이 데이터베이스를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="76f64-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="76f64-126">-ServerName</span></span>
<span data-ttu-id="76f64-127">데이터베이스의 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="76f64-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="76f64-128">-Confirm</span></span>
<span data-ttu-id="76f64-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f64-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76f64-130">-WhatIf</span></span>
<span data-ttu-id="76f64-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="76f64-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76f64-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76f64-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76f64-133">CommonParameters</span></span>
<span data-ttu-id="76f64-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76f64-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76f64-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76f64-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76f64-136">입력</span><span class="sxs-lookup"><span data-stu-id="76f64-136">INPUTS</span></span>

### <span data-ttu-id="76f64-137">System.String</span><span class="sxs-lookup"><span data-stu-id="76f64-137">System.String</span></span>

### <span data-ttu-id="76f64-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="76f64-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="76f64-139">출력</span><span class="sxs-lookup"><span data-stu-id="76f64-139">OUTPUTS</span></span>

### <span data-ttu-id="76f64-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="76f64-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="76f64-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76f64-141">NOTES</span></span>

## <span data-ttu-id="76f64-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76f64-142">RELATED LINKS</span></span>

[<span data-ttu-id="76f64-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="76f64-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="76f64-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="76f64-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

