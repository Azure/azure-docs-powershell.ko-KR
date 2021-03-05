---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b453c11d7a6e63e5365bca5cd186002f66ed13cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995862"
---
# <span data-ttu-id="ce2c3-101">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce2c3-101">New-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="ce2c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce2c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2c3-103">데이터베이스에 대한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-103">Creates a data masking rule for a database.</span></span>

## <span data-ttu-id="ce2c3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce2c3-104">SYNTAX</span></span>

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce2c3-105">설명</span><span class="sxs-lookup"><span data-stu-id="ce2c3-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2c3-106">**New-AzSqlDatabaseDataMaskingRule** cmdlet은 Azure SQL 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-106">The **New-AzSqlDatabaseDataMaskingRule** cmdlet creates a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="ce2c3-107">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 규칙을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-107">To use the cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the rule.</span></span>
<span data-ttu-id="ce2c3-108">*TableName* 및 *ColumnName을* 제공하여 규칙의 대상 및 *MaskingFunction* 매개 변수를 지정하여 데이터가 마스킹되는 방법을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-108">Provide the *TableName* and *ColumnName* to specify the target of the rule and the *MaskingFunction* parameter to define how the data is masked.</span></span>
<span data-ttu-id="ce2c3-109">*MaskingFunction에* 숫자 또는 텍스트 값이 있는 경우 *NumberFrom* 및 *NumberTo* 매개 변수, 숫자 마스킹 또는 접두사Size , *ReplacementString* 및 텍스트 마스킹에 대한 *접미사Size를* 지정할 수 있습니다. </span><span class="sxs-lookup"><span data-stu-id="ce2c3-109">If *MaskingFunction* has a value of Number or Text, you can specify the *NumberFrom* and *NumberTo* parameters, for number masking, or the *PrefixSize*, *ReplacementString*, and *SuffixSize* for text masking.</span></span>
<span data-ttu-id="ce2c3-110">명령이 성공하고 *PassThru* 매개 변수가 사용되는 경우 cmdlet은 규칙 식별자 외에도 데이터 마스킹 규칙 속성을 설명하는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-110">If the command succeeds and the *PassThru* parameter is used, the cmdlet returns an object describing the data masking rule properties in addition to the rule identifiers.</span></span>
<span data-ttu-id="ce2c3-111">규칙 식별자는 *ResourceGroupName,* *ServerName,* *DatabaseName* 및 RuleID를 포함하지만 *제한되지 않습니다.*</span><span class="sxs-lookup"><span data-stu-id="ce2c3-111">Rule identifiers include, but are not limited to, *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleID*.</span></span>
<span data-ttu-id="ce2c3-112">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ce2c3-113">예제</span><span class="sxs-lookup"><span data-stu-id="ce2c3-113">EXAMPLES</span></span>

### <span data-ttu-id="ce2c3-114">예제 1: 데이터베이스의 숫자 열에 대한 데이터 마스킹 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="ce2c3-114">Example 1: Create a data masking rule for a number column in a database</span></span>
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

<span data-ttu-id="ce2c3-115">이 명령은 Schema01이라는 schemama의 Table01이라는 테이블에 Column01이라는 열에 대한 데이터 마스킹 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-115">This command creates a data masking rule for the column named Column01 in the table named Table01 in the schema named Schema01.</span></span>
<span data-ttu-id="ce2c3-116">Database01이라는 데이터베이스에는 이러한 모든 항목이 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-116">The database named Database01 contains all these items.</span></span>
<span data-ttu-id="ce2c3-117">규칙은 5에서 14 사이의 난수로 마스크 값으로 사용하는 숫자 마스킹 규칙입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-117">The rule is a number masking rule that uses a random number between 5 and 14 as the mask value.</span></span>

## <span data-ttu-id="ce2c3-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce2c3-118">PARAMETERS</span></span>

### <span data-ttu-id="ce2c3-119">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-119">-ColumnName</span></span>
<span data-ttu-id="ce2c3-120">마스킹 규칙에 의해 대상이 지정된 열의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-120">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="ce2c3-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-121">-DatabaseName</span></span>
<span data-ttu-id="ce2c3-122">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-122">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="ce2c3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2c3-123">-DefaultProfile</span></span>
<span data-ttu-id="ce2c3-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ce2c3-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce2c3-125">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="ce2c3-125">-MaskingFunction</span></span>
<span data-ttu-id="ce2c3-126">규칙에서 사용하는 마스킹 함수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-126">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="ce2c3-127">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-127">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce2c3-128">기본값</span><span class="sxs-lookup"><span data-stu-id="ce2c3-128">Default</span></span>
- <span data-ttu-id="ce2c3-129">NoMasking</span><span class="sxs-lookup"><span data-stu-id="ce2c3-129">NoMasking</span></span>
- <span data-ttu-id="ce2c3-130">텍스트</span><span class="sxs-lookup"><span data-stu-id="ce2c3-130">Text</span></span>
- <span data-ttu-id="ce2c3-131">번호</span><span class="sxs-lookup"><span data-stu-id="ce2c3-131">Number</span></span>
- <span data-ttu-id="ce2c3-132">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="ce2c3-132">SocialSecurityNumber</span></span>
- <span data-ttu-id="ce2c3-133">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="ce2c3-133">CreditCardNumber</span></span>
- <span data-ttu-id="ce2c3-134">전자 메일 기본값은 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-134">Email The default value is Default.</span></span>

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

### <span data-ttu-id="ce2c3-135">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="ce2c3-135">-NumberFrom</span></span>
<span data-ttu-id="ce2c3-136">임의 값이 선택된 간격의 하한 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-136">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ce2c3-137">*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-137">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce2c3-138">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-138">The default value is 0.</span></span>

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

### <span data-ttu-id="ce2c3-139">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="ce2c3-139">-NumberTo</span></span>
<span data-ttu-id="ce2c3-140">임의 값이 선택된 간격의 상한 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-140">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="ce2c3-141">*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-141">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce2c3-142">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-142">The default value is 0.</span></span>

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

### <span data-ttu-id="ce2c3-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ce2c3-143">-PassThru</span></span>
<span data-ttu-id="ce2c3-144">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-144">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ce2c3-145">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-145">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ce2c3-146">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="ce2c3-146">-PrefixSize</span></span>
<span data-ttu-id="ce2c3-147">마스크되지 않은 텍스트의 시작에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-147">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="ce2c3-148">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-148">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce2c3-149">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-149">The default value is 0.</span></span>

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

### <span data-ttu-id="ce2c3-150">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="ce2c3-150">-ReplacementString</span></span>
<span data-ttu-id="ce2c3-151">마스크되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-151">Specifies the number of characters in the end of the text that are not masked.</span></span>
<span data-ttu-id="ce2c3-152">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-152">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce2c3-153">기본값은 빈 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-153">The default value is an empty string.</span></span>

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

### <span data-ttu-id="ce2c3-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-154">-ResourceGroupName</span></span>
<span data-ttu-id="ce2c3-155">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-155">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ce2c3-156">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-156">-SchemaName</span></span>
<span data-ttu-id="ce2c3-157">Schema의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-157">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="ce2c3-158">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-158">-ServerName</span></span>
<span data-ttu-id="ce2c3-159">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-159">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="ce2c3-160">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="ce2c3-160">-SuffixSize</span></span>
<span data-ttu-id="ce2c3-161">마스크되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-161">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="ce2c3-162">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-162">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="ce2c3-163">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-163">The default value is 0.</span></span>

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

### <span data-ttu-id="ce2c3-164">-TableName</span><span class="sxs-lookup"><span data-stu-id="ce2c3-164">-TableName</span></span>
<span data-ttu-id="ce2c3-165">마스크된 열을 포함하는 데이터베이스 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-165">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="ce2c3-166">-확인</span><span class="sxs-lookup"><span data-stu-id="ce2c3-166">-Confirm</span></span>
<span data-ttu-id="ce2c3-167">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-167">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce2c3-168">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce2c3-168">-WhatIf</span></span>
<span data-ttu-id="ce2c3-169">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-169">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce2c3-170">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-170">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce2c3-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2c3-171">CommonParameters</span></span>
<span data-ttu-id="ce2c3-172">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2c3-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2c3-173">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce2c3-173">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2c3-174">입력</span><span class="sxs-lookup"><span data-stu-id="ce2c3-174">INPUTS</span></span>

### <span data-ttu-id="ce2c3-175">System.String</span><span class="sxs-lookup"><span data-stu-id="ce2c3-175">System.String</span></span>

### <span data-ttu-id="ce2c3-176">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce2c3-176">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ce2c3-177">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ce2c3-177">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ce2c3-178">출력</span><span class="sxs-lookup"><span data-stu-id="ce2c3-178">OUTPUTS</span></span>

### <span data-ttu-id="ce2c3-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="ce2c3-179">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="ce2c3-180">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce2c3-180">NOTES</span></span>

## <span data-ttu-id="ce2c3-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce2c3-181">RELATED LINKS</span></span>

[<span data-ttu-id="ce2c3-182">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce2c3-182">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce2c3-183">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce2c3-183">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce2c3-184">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ce2c3-184">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ce2c3-185">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ce2c3-185">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


