---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 8813d405ebc8fadafa037afb884240dcdbb95383
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216689"
---
# <span data-ttu-id="9fe92-101">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9fe92-101">Get-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="9fe92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fe92-102">SYNOPSIS</span></span>
<span data-ttu-id="9fe92-103">데이터베이스에서 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-103">Gets the data masking rules from a database.</span></span>

## <span data-ttu-id="9fe92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9fe92-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fe92-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9fe92-105">DESCRIPTION</span></span>
<span data-ttu-id="9fe92-106">**AzSqlDatabaseDataMaskingRule** cmdlet은 특정 데이터 마스킹 규칙 또는 Azure SQL 데이터베이스에 대 한 모든 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-106">The **Get-AzSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="9fe92-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 하 고 *RuleId* 매개 변수를 사용 하 여이 cmdlet이 반환 하는 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="9fe92-108">*RuleId* 를 제공 하지 않으면 해당 Azure SQL 데이터베이스에 대 한 모든 데이터 마스킹 규칙이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="9fe92-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9fe92-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9fe92-110">EXAMPLES</span></span>

### <span data-ttu-id="9fe92-111">예제 1: 데이터베이스에서 모든 데이터 마스킹 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="9fe92-111">Example 1: Get all data masking rules from a database</span></span>
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

### <span data-ttu-id="9fe92-112">예제 2: 스키마 "dbo", 테이블 "table1" 및 열 "column1"에 정의 된 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
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

## <span data-ttu-id="9fe92-113">변수</span><span class="sxs-lookup"><span data-stu-id="9fe92-113">PARAMETERS</span></span>

### <span data-ttu-id="9fe92-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9fe92-114">-ColumnName</span></span>
<span data-ttu-id="9fe92-115">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="9fe92-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9fe92-116">-DatabaseName</span></span>
<span data-ttu-id="9fe92-117">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="9fe92-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fe92-118">-DefaultProfile</span></span>
<span data-ttu-id="9fe92-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9fe92-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9fe92-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fe92-120">-ResourceGroupName</span></span>
<span data-ttu-id="9fe92-121">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9fe92-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9fe92-122">-SchemaName</span></span>
<span data-ttu-id="9fe92-123">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="9fe92-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9fe92-124">-ServerName</span></span>
<span data-ttu-id="9fe92-125">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="9fe92-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="9fe92-126">-TableName</span></span>
<span data-ttu-id="9fe92-127">Azure SQL 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="9fe92-128">-확인</span><span class="sxs-lookup"><span data-stu-id="9fe92-128">-Confirm</span></span>
<span data-ttu-id="9fe92-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9fe92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fe92-130">-WhatIf</span></span>
<span data-ttu-id="9fe92-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9fe92-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9fe92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fe92-133">CommonParameters</span></span>
<span data-ttu-id="9fe92-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9fe92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fe92-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9fe92-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fe92-136">입력</span><span class="sxs-lookup"><span data-stu-id="9fe92-136">INPUTS</span></span>

### <span data-ttu-id="9fe92-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9fe92-137">System.String</span></span>

## <span data-ttu-id="9fe92-138">출력</span><span class="sxs-lookup"><span data-stu-id="9fe92-138">OUTPUTS</span></span>

### <span data-ttu-id="9fe92-139">DataMasking. DatabaseDataMaskingRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9fe92-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="9fe92-140">상속자</span><span class="sxs-lookup"><span data-stu-id="9fe92-140">NOTES</span></span>

## <span data-ttu-id="9fe92-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9fe92-141">RELATED LINKS</span></span>

[<span data-ttu-id="9fe92-142">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="9fe92-142">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="9fe92-143">새로운 AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9fe92-143">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9fe92-144">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9fe92-144">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9fe92-145">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="9fe92-145">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="9fe92-146">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9fe92-146">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


