---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 848A6972-AB29-46FB-8E03-FF2ADB113A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: c5cf2d8611238706bb9725101a320c79eb099570
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703795"
---
# <span data-ttu-id="1c005-101">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1c005-101">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="1c005-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c005-102">SYNOPSIS</span></span>
<span data-ttu-id="1c005-103">데이터베이스에서 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-103">Gets the data masking rules from a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c005-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c005-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseDataMaskingRule [-SchemaName <String>] [-TableName <String>] [-ColumnName <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c005-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c005-105">DESCRIPTION</span></span>
<span data-ttu-id="1c005-106">**AzureRmSqlDatabaseDataMaskingRule** cmdlet은 특정 데이터 마스킹 규칙 또는 Azure SQL 데이터베이스에 대 한 모든 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-106">The **Get-AzureRmSqlDatabaseDataMaskingRule** cmdlet gets either a specific data masking rule or all of the data masking rules for an Azure SQL database.</span></span>
<span data-ttu-id="1c005-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 하 고 *RuleId* 매개 변수를 사용 하 여이 cmdlet이 반환 하는 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database, and the *RuleId* parameter to specify which rule this cmdlet returns.</span></span>
<span data-ttu-id="1c005-108">*RuleId* 를 제공 하지 않으면 해당 Azure SQL 데이터베이스에 대 한 모든 데이터 마스킹 규칙이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-108">If you do not provide *RuleId* , all the data masking rules for that Azure SQL database are returned.</span></span>
<span data-ttu-id="1c005-109">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-109">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="1c005-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1c005-110">EXAMPLES</span></span>

### <span data-ttu-id="1c005-111">예제 1: 데이터베이스에서 모든 데이터 마스킹 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="1c005-111">Example 1: Get all data masking rules from a database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
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

### <span data-ttu-id="1c005-112">예제 2: 스키마 "dbo", 테이블 "table1" 및 열 "column1"에 정의 된 데이터 마스킹 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-112">Example 2: Get the data masking rule defined on schema "dbo", table "table1" and column "column1".</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -SchemaName "dbo" -TableName  "table1" -ColumnName "column1"
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

## <span data-ttu-id="1c005-113">변수</span><span class="sxs-lookup"><span data-stu-id="1c005-113">PARAMETERS</span></span>

### <span data-ttu-id="1c005-114">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="1c005-114">-ColumnName</span></span>
<span data-ttu-id="1c005-115">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-115">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="1c005-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1c005-116">-DatabaseName</span></span>
<span data-ttu-id="1c005-117">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-117">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="1c005-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c005-118">-DefaultProfile</span></span>
<span data-ttu-id="1c005-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1c005-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c005-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c005-120">-ResourceGroupName</span></span>
<span data-ttu-id="1c005-121">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-121">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1c005-122">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="1c005-122">-SchemaName</span></span>
<span data-ttu-id="1c005-123">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-123">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="1c005-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1c005-124">-ServerName</span></span>
<span data-ttu-id="1c005-125">서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-125">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="1c005-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="1c005-126">-TableName</span></span>
<span data-ttu-id="1c005-127">Azure SQL 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="1c005-128">-확인</span><span class="sxs-lookup"><span data-stu-id="1c005-128">-Confirm</span></span>
<span data-ttu-id="1c005-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c005-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c005-130">-WhatIf</span></span>
<span data-ttu-id="1c005-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c005-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c005-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c005-133">CommonParameters</span></span>
<span data-ttu-id="1c005-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c005-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c005-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c005-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c005-136">입력</span><span class="sxs-lookup"><span data-stu-id="1c005-136">INPUTS</span></span>

### <span data-ttu-id="1c005-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1c005-137">System.String</span></span>

## <span data-ttu-id="1c005-138">출력</span><span class="sxs-lookup"><span data-stu-id="1c005-138">OUTPUTS</span></span>

### <span data-ttu-id="1c005-139">DataMasking. DatabaseDataMaskingRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="1c005-139">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="1c005-140">상속자</span><span class="sxs-lookup"><span data-stu-id="1c005-140">NOTES</span></span>

## <span data-ttu-id="1c005-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c005-141">RELATED LINKS</span></span>

[<span data-ttu-id="1c005-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1c005-142">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1c005-143">새로운 AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1c005-143">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1c005-144">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1c005-144">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="1c005-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="1c005-145">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="1c005-146">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="1c005-146">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)


