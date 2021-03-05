---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: ab6bdaac71e13cfe62c054c5dbc01686760505ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967472"
---
# <span data-ttu-id="6ce6a-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6ce6a-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="6ce6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ce6a-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce6a-103">데이터베이스에서 데이터 마스킹 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="6ce6a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ce6a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce6a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6ce6a-105">DESCRIPTION</span></span>
<span data-ttu-id="6ce6a-106">**Get-AzSqlDatabaseDataMaskingRule** cmdlet은 특정 데이터 마스킹 규칙 또는 Azure SQL 마스킹 규칙을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="6ce6a-107">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별하고 *RuleId* 매개 변수를 사용하여 이 cmdlet이 반환하는 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="6ce6a-108">*RuleId를* 제공하지 않는 경우 해당 Azure 데이터베이스의 모든 데이터 마스킹 SQL 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-108">If you do not provide *RuleId*, all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="6ce6a-109">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="6ce6a-110">예제</span><span class="sxs-lookup"><span data-stu-id="6ce6a-110">EXAMPLES</span></span>

### <span data-ttu-id="6ce6a-111">예제 1: 데이터베이스에서 모든 데이터 마스킹 규칙 사용</span><span class="sxs-lookup"><span data-stu-id="6ce6a-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :

DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table2
ColumnName        : column2
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

### <span data-ttu-id="6ce6a-112">예제 2: "dbo", 테이블 "table1" 및 열 "column1"에 정의된 데이터 마스킹 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
DatabaseName      : database01
ResourceGroupName : resourcegroup01
ServerName        : server01
SchemaName        : dbo
TableName         : table1
ColumnName        : column1
MaskingFunction   : Default
PrefixSize        :
SuffixSize        :
ReplacementString :
NumberFrom        :
NumberTo          :
```

## <span data-ttu-id="6ce6a-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ce6a-113">PARAMETERS</span></span>

### <span data-ttu-id="6ce6a-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-114">-ColumnName</span></span>
<span data-ttu-id="6ce6a-115">마스킹 규칙에 의해 대상이 지정된 열의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="6ce6a-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-116">-DatabaseName</span></span>
<span data-ttu-id="6ce6a-117">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="6ce6a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce6a-118">-DefaultProfile</span></span>
<span data-ttu-id="6ce6a-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ce6a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ce6a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-120">-ResourceGroupName</span></span>
<span data-ttu-id="6ce6a-121">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="6ce6a-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-122">-SchemaName</span></span>
<span data-ttu-id="6ce6a-123">Schema의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="6ce6a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-124">-ServerName</span></span>
<span data-ttu-id="6ce6a-125">서버 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="6ce6a-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="6ce6a-126">-TableName</span></span>
<span data-ttu-id="6ce6a-127">Azure 테이블의 이름을 SQL 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="6ce6a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6ce6a-128">-Confirm</span></span>
<span data-ttu-id="6ce6a-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ce6a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce6a-130">-WhatIf</span></span>
<span data-ttu-id="6ce6a-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ce6a-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ce6a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce6a-133">CommonParameters</span></span>
<span data-ttu-id="6ce6a-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ce6a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce6a-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ce6a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce6a-136">입력</span><span class="sxs-lookup"><span data-stu-id="6ce6a-136">INPUTS</span></span>

### <span data-ttu-id="6ce6a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="6ce6a-137">System.String</span></span>

## <span data-ttu-id="6ce6a-138">출력</span><span class="sxs-lookup"><span data-stu-id="6ce6a-138">OUTPUTS</span></span>

### <span data-ttu-id="6ce6a-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="6ce6a-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="6ce6a-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ce6a-140">NOTES</span></span>

## <span data-ttu-id="6ce6a-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ce6a-141">RELATED LINKS</span></span>

[<span data-ttu-id="6ce6a-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="6ce6a-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="6ce6a-143">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6ce6a-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6ce6a-144">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6ce6a-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="6ce6a-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="6ce6a-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="6ce6a-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="6ce6a-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


