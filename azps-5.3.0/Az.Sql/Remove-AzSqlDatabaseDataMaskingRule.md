---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4695AFEA-D244-4FCB-AF36-D8CDEBFB392C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 02a6090a98a80300f886e8bbbd8e2622aa7981d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380997"
---
# <span data-ttu-id="71930-101">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="71930-101">Remove-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="71930-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71930-102">SYNOPSIS</span></span>
<span data-ttu-id="71930-103">데이터베이스에서 데이터 마스킹 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-103">Removes a data masking rule from a database.</span></span>

## <span data-ttu-id="71930-104">구문</span><span class="sxs-lookup"><span data-stu-id="71930-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseDataMaskingRule [-PassThru] [-Force] -SchemaName <String> -TableName <String>
 -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71930-105">설명</span><span class="sxs-lookup"><span data-stu-id="71930-105">DESCRIPTION</span></span>
<span data-ttu-id="71930-106">**Remove-AzSqlDatabaseDataMaskingRule** cmdlet은 Azure SQL 데이터베이스에서 특정 데이터 마스킹 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-106">The **Remove-AzSqlDatabaseDataMaskingRule** cmdlet removes a specific data masking rule from an Azure SQL database.</span></span>
<span data-ttu-id="71930-107">*ResourceGroupName,* *ServerName,* *DatabaseName* 및 *RuleId* 매개 변수를 사용하여 데이터 마스킹 규칙을 제거하여 이 cmdlet이 제거하는 규칙을 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71930-107">You can remove a data masking rule by using the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule that this cmdlet removes.</span></span>
<span data-ttu-id="71930-108">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="71930-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="71930-109">예제</span><span class="sxs-lookup"><span data-stu-id="71930-109">EXAMPLES</span></span>

### <span data-ttu-id="71930-110">예제 1: 데이터베이스 데이터 마스킹 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="71930-110">Example 1: Remove a database data masking rule</span></span>
```
PS C:\>Remove-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
```

<span data-ttu-id="71930-111">이 명령은 Database01에 대해 정의된 규칙 이름 Rule01을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-111">This command removes rule name Rule01 defined for the database Database01.</span></span>
<span data-ttu-id="71930-112">데이터베이스는 Server01에 있으며 리소스 그룹 ResourceGroup01에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="71930-112">The database is located on Server01 and assigned to resource group ResourceGroup01.</span></span>

## <span data-ttu-id="71930-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="71930-113">PARAMETERS</span></span>

### <span data-ttu-id="71930-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="71930-114">-ColumnName</span></span>
<span data-ttu-id="71930-115">마스킹 규칙에 의해 대상이 지정된 열의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="71930-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="71930-116">-DatabaseName</span></span>
<span data-ttu-id="71930-117">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-117">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71930-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71930-118">-DefaultProfile</span></span>
<span data-ttu-id="71930-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="71930-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="71930-120">-Force</span><span class="sxs-lookup"><span data-stu-id="71930-120">-Force</span></span>
<span data-ttu-id="71930-121">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="71930-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71930-122">-PassThru</span></span>
<span data-ttu-id="71930-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="71930-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71930-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="71930-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="71930-125">-ResourceGroupName</span></span>
<span data-ttu-id="71930-126">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-126">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="71930-127">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="71930-127">-SchemaName</span></span>
<span data-ttu-id="71930-128">스마마의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-128">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="71930-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="71930-129">-ServerName</span></span>
<span data-ttu-id="71930-130">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-130">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71930-131">-TableName</span><span class="sxs-lookup"><span data-stu-id="71930-131">-TableName</span></span>
<span data-ttu-id="71930-132">Azure SQL 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-132">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="71930-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="71930-133">-Confirm</span></span>
<span data-ttu-id="71930-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="71930-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71930-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71930-135">-WhatIf</span></span>
<span data-ttu-id="71930-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="71930-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71930-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71930-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71930-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71930-138">CommonParameters</span></span>
<span data-ttu-id="71930-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="71930-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71930-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="71930-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71930-141">입력</span><span class="sxs-lookup"><span data-stu-id="71930-141">INPUTS</span></span>

### <span data-ttu-id="71930-142">System.String</span><span class="sxs-lookup"><span data-stu-id="71930-142">System.String</span></span>

## <span data-ttu-id="71930-143">출력</span><span class="sxs-lookup"><span data-stu-id="71930-143">OUTPUTS</span></span>

### <span data-ttu-id="71930-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="71930-144">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="71930-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="71930-145">NOTES</span></span>

## <span data-ttu-id="71930-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71930-146">RELATED LINKS</span></span>

[<span data-ttu-id="71930-147">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="71930-147">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="71930-148">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="71930-148">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="71930-149">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="71930-149">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="71930-150">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="71930-150">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


