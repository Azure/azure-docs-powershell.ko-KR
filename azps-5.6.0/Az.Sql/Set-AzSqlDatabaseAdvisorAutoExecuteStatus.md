---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 50E09DF7-F5B5-4668-9520-73D562E91800
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabaseadvisorautoexecutestatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseAdvisorAutoExecuteStatus.md
ms.openlocfilehash: 214fe4c32ed49433aa57752508604d0179334401
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995017"
---
# <span data-ttu-id="90480-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="90480-101">Set-AzSqlDatabaseAdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="90480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90480-102">SYNOPSIS</span></span>
<span data-ttu-id="90480-103">Azure 데이터베이스 Advisor의 자동 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-103">Modifies auto execute status of an Azure SQL Database Advisor.</span></span>

## <span data-ttu-id="90480-104">구문</span><span class="sxs-lookup"><span data-stu-id="90480-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseAdvisorAutoExecuteStatus -AdvisorName <String> -AutoExecuteStatus <AdvisorAutoExecuteStatus>
 -ServerName <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90480-105">설명</span><span class="sxs-lookup"><span data-stu-id="90480-105">DESCRIPTION</span></span>
<span data-ttu-id="90480-106">**Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet은 Azure SQL 데이터베이스 어드바이저에 대한 자동 실행 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-106">The **Set-AzSqlDatabaseAdvisorAutoExecuteStatus** cmdlet modifies the auto execute property for an Azure SQL Database Advisor.</span></span>
<span data-ttu-id="90480-107">현재 이 cmdlet은 사용 가능, 비활성화 및 기본값 값을 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-107">Currently, this cmdlet supports the values Enabled, Disabled, and Default.</span></span>

## <span data-ttu-id="90480-108">예제</span><span class="sxs-lookup"><span data-stu-id="90480-108">EXAMPLES</span></span>

### <span data-ttu-id="90480-109">예제 1: 고문에 대해 자동 실행 사용</span><span class="sxs-lookup"><span data-stu-id="90480-109">Example 1: Enable auto execute for an advisor</span></span>
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

<span data-ttu-id="90480-110">이 명령은 CreateIndex라는 어드바이저의 자동 실행 상태를 사용하도록 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-110">This command changes the auto execute status of an advisor named CreateIndex to Enabled.</span></span>

## <span data-ttu-id="90480-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90480-111">PARAMETERS</span></span>

### <span data-ttu-id="90480-112">-AdvisorName</span><span class="sxs-lookup"><span data-stu-id="90480-112">-AdvisorName</span></span>
<span data-ttu-id="90480-113">이 cmdlet이 상태를 수정하는 어드바이저의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-113">Specifies the name of the advisor for which this cmdlet modifies the status.</span></span>

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

### <span data-ttu-id="90480-114">-AutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="90480-114">-AutoExecuteStatus</span></span>
<span data-ttu-id="90480-115">상태에 대한 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-115">Specifies the value for the status.</span></span>
<span data-ttu-id="90480-116">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="90480-116">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="90480-117">사용 가능</span><span class="sxs-lookup"><span data-stu-id="90480-117">Enabled</span></span> 
- <span data-ttu-id="90480-118">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="90480-118">Disabled</span></span> 
- <span data-ttu-id="90480-119">기본값</span><span class="sxs-lookup"><span data-stu-id="90480-119">Default</span></span>

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

### <span data-ttu-id="90480-120">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="90480-120">-DatabaseName</span></span>
<span data-ttu-id="90480-121">이 cmdlet이 상태를 수정하는 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-121">Specifies the name of the database for which this cmdlet modifies status.</span></span>

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

### <span data-ttu-id="90480-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90480-122">-DefaultProfile</span></span>
<span data-ttu-id="90480-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="90480-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90480-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90480-124">-ResourceGroupName</span></span>
<span data-ttu-id="90480-125">이 데이터베이스를 포함하는 서버의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-125">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="90480-126">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90480-126">-ServerName</span></span>
<span data-ttu-id="90480-127">데이터베이스에 대한 서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-127">Specifies the name of the server for the database.</span></span>

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

### <span data-ttu-id="90480-128">-확인</span><span class="sxs-lookup"><span data-stu-id="90480-128">-Confirm</span></span>
<span data-ttu-id="90480-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="90480-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90480-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90480-130">-WhatIf</span></span>
<span data-ttu-id="90480-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="90480-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90480-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90480-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90480-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90480-133">CommonParameters</span></span>
<span data-ttu-id="90480-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90480-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90480-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90480-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90480-136">입력</span><span class="sxs-lookup"><span data-stu-id="90480-136">INPUTS</span></span>

### <span data-ttu-id="90480-137">System.String</span><span class="sxs-lookup"><span data-stu-id="90480-137">System.String</span></span>

### <span data-ttu-id="90480-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span><span class="sxs-lookup"><span data-stu-id="90480-138">Microsoft.Azure.Commands.Sql.Advisor.Cmdlet.AdvisorAutoExecuteStatus</span></span>

## <span data-ttu-id="90480-139">출력</span><span class="sxs-lookup"><span data-stu-id="90480-139">OUTPUTS</span></span>

### <span data-ttu-id="90480-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span><span class="sxs-lookup"><span data-stu-id="90480-140">Microsoft.Azure.Commands.Sql.Advisor.Model.AzureSqlDatabaseAdvisorModel</span></span>

## <span data-ttu-id="90480-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90480-141">NOTES</span></span>

## <span data-ttu-id="90480-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90480-142">RELATED LINKS</span></span>

[<span data-ttu-id="90480-143">Get-AzSqlDatabaseAdvisor</span><span class="sxs-lookup"><span data-stu-id="90480-143">Get-AzSqlDatabaseAdvisor</span></span>](./Get-AzSqlDatabaseAdvisor.md)

[<span data-ttu-id="90480-144">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="90480-144">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

