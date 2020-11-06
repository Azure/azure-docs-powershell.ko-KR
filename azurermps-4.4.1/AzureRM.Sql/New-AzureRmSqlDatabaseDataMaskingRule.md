---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 6facaef4255d37ccaa0e2c192c40c8888d485357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536924"
---
# <span data-ttu-id="39636-101">New-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="39636-101">New-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="39636-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39636-102">SYNOPSIS</span></span>
<span data-ttu-id="39636-103">데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39636-103">Creates a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39636-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39636-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39636-105">설명은</span><span class="sxs-lookup"><span data-stu-id="39636-105">DESCRIPTION</span></span>
<span data-ttu-id="39636-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39636-106">The **New-AzureRmSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="39636-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 사용 하 여 규칙을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-107">To use the cmdlet, use the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="39636-108">*TableName* 및 *ColumnName* 을 제공 하 여 규칙의 대상을 지정 하 고 *MaskingFunction* 매개 변수를 입력 하 여 데이터 마스크 방법을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>

<span data-ttu-id="39636-109">*MaskingFunction* 에 Number 또는 text 값이 있으면 숫자 *의 시작* 및 *번호를* 매개 변수로 지정 하거나, 숫자 마스킹 또는 *PrefixSize* , *ReplacementString* , 텍스트 마스킹에 *SuffixSize* 을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39636-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize* , *ReplacementString* , and *SuffixSize* for text masking.</span></span>

<span data-ttu-id="39636-110">명령이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 cmdlet은 규칙 식별자 외에도 데이터 마스킹 규칙 속성에 대해 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="39636-111">규칙 식별자에는 *ResourceGroupName* , *ServerName* , *DatabaseName* , *RuleID* 이 포함 되지만이에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39636-111">Rule identifiers include, but are not limited to, *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleID*.</span></span>

<span data-ttu-id="39636-112">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39636-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="39636-113">예제의</span><span class="sxs-lookup"><span data-stu-id="39636-113">EXAMPLES</span></span>

### <span data-ttu-id="39636-114">예제 1: 데이터베이스의 숫자 열에 대 한 데이터 마스킹 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="39636-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="39636-115">이 명령은 Schema01 이라는 스키마의 Table01 테이블에서 Column01 이라는 열에 대 한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="39636-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="39636-116">Database01 라는 데이터베이스에는 이러한 항목이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39636-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="39636-117">규칙은 5와 14 사이의 난수를 마스크 값으로 사용 하는 숫자 마스킹 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>
<span data-ttu-id="39636-118">규칙의 이름은 Rule01입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-118">The rule is named Rule01.</span></span>

## <span data-ttu-id="39636-119">변수</span><span class="sxs-lookup"><span data-stu-id="39636-119">PARAMETERS</span></span>

### <span data-ttu-id="39636-120">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="39636-120">-ColumnName</span></span>
<span data-ttu-id="39636-121">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-121">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="39636-122">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39636-122">-DatabaseName</span></span>
<span data-ttu-id="39636-123">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-123">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="39636-124">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="39636-124">-MaskingFunction</span></span>
<span data-ttu-id="39636-125">규칙에서 사용 하는 마스킹 기능을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-125">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="39636-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="39636-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="39636-127">기본값</span><span class="sxs-lookup"><span data-stu-id="39636-127">Default</span></span>
- <span data-ttu-id="39636-128">NoMasking</span><span class="sxs-lookup"><span data-stu-id="39636-128">NoMasking</span></span>
- <span data-ttu-id="39636-129">본문</span><span class="sxs-lookup"><span data-stu-id="39636-129">Text</span></span>
- <span data-ttu-id="39636-130">숫자로</span><span class="sxs-lookup"><span data-stu-id="39636-130">Number</span></span>
- <span data-ttu-id="39636-131">사회 Alsecurity번호</span><span class="sxs-lookup"><span data-stu-id="39636-131">SocialSecurityNumber</span></span>
- <span data-ttu-id="39636-132">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="39636-132">CreditCardNumber</span></span>
- <span data-ttu-id="39636-133">메일 주소</span><span class="sxs-lookup"><span data-stu-id="39636-133">Email</span></span>

<span data-ttu-id="39636-134">기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-134">The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39636-135">-번호</span><span class="sxs-lookup"><span data-stu-id="39636-135">-NumberFrom</span></span>
<span data-ttu-id="39636-136">임의의 값이 선택 되는 간격의 하한값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="39636-137">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="39636-138">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-138">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39636-139">-번호를</span><span class="sxs-lookup"><span data-stu-id="39636-139">-NumberTo</span></span>
<span data-ttu-id="39636-140">임의 값이 선택 된 간격의 상한 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="39636-141">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="39636-142">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-142">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39636-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="39636-143">-PassThru</span></span>
<span data-ttu-id="39636-144">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="39636-145">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39636-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="39636-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="39636-146">-PrefixSize</span></span>
<span data-ttu-id="39636-147">마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="39636-148">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="39636-149">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-149">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39636-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="39636-150">-ReplacementString</span></span>
<span data-ttu-id="39636-151">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="39636-152">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="39636-153">기본값은 빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="39636-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39636-154">-ResourceGroupName</span></span>
<span data-ttu-id="39636-155">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="39636-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="39636-156">-SchemaName</span></span>
<span data-ttu-id="39636-157">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="39636-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="39636-158">-ServerName</span></span>
<span data-ttu-id="39636-159">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="39636-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="39636-160">-SuffixSize</span></span>
<span data-ttu-id="39636-161">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="39636-162">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="39636-163">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-163">The default value is 0.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39636-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="39636-164">-TableName</span></span>
<span data-ttu-id="39636-165">마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="39636-166">-확인</span><span class="sxs-lookup"><span data-stu-id="39636-166">-Confirm</span></span>
<span data-ttu-id="39636-167">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39636-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39636-168">-WhatIf</span></span>
<span data-ttu-id="39636-169">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="39636-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39636-170">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39636-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39636-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39636-171">-DefaultProfile</span></span>
<span data-ttu-id="39636-172">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="39636-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="39636-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39636-173">CommonParameters</span></span>
<span data-ttu-id="39636-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39636-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39636-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39636-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39636-176">입력</span><span class="sxs-lookup"><span data-stu-id="39636-176">INPUTS</span></span>

###  
<span data-ttu-id="39636-177">않아야.</span><span class="sxs-lookup"><span data-stu-id="39636-177">None.</span></span>

## <span data-ttu-id="39636-178">출력</span><span class="sxs-lookup"><span data-stu-id="39636-178">OUTPUTS</span></span>

### <span data-ttu-id="39636-179">DatabaseDataMaskingRuleModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="39636-179">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="39636-180">상속자</span><span class="sxs-lookup"><span data-stu-id="39636-180">NOTES</span></span>

## <span data-ttu-id="39636-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39636-181">RELATED LINKS</span></span>

[<span data-ttu-id="39636-182">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="39636-182">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="39636-183">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="39636-183">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="39636-184">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="39636-184">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="39636-185">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="39636-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


