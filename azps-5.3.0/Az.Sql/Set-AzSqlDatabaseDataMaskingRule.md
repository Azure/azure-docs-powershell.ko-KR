---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489479"
---
# <span data-ttu-id="9c81d-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9c81d-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="9c81d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c81d-102">SYNOPSIS</span></span>
<span data-ttu-id="9c81d-103">데이터베이스에 대한 데이터 마스킹 규칙의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="9c81d-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c81d-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c81d-105">설명</span><span class="sxs-lookup"><span data-stu-id="9c81d-105">DESCRIPTION</span></span>
<span data-ttu-id="9c81d-106">**Set-AzSqlDatabaseDataMaskingRule** cmdlet은 Azure SQL 데이터베이스에 대한 데이터 마스킹 규칙을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="9c81d-107">cmdlet을 사용하려면 *ResourceGroupName,* *ServerName,* *DatabaseName* 및 *RuleId* 매개 변수를 입력하여 규칙을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-107">To use the cmdlet, provide the *ResourceGroupName*, *ServerName*, *DatabaseName*, and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="9c81d-108">*SchemaName,* *TableName* 및 *ColumnName의* 매개 변수를 입력하여 규칙을 다시 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-108">You can provide any of the parameters of *SchemaName*, *TableName*, and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="9c81d-109">*MaskingFunction* 매개 변수를 지정하여 데이터가 마스킹되는 방법을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="9c81d-110">*MaskingFunction에* 대한 숫자 또는 텍스트 값을 지정하는 경우 숫자 마스킹에 *대한 NumberFrom* 및 *NumberTo* 매개 변수 또는 텍스트 마스킹에 대한 *PrefixSize,* *ReplacementString* 및 *SuffixSize* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-110">If you specify a value of Number or Text for *MaskingFunction*, you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize*, *ReplacementString*, and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="9c81d-111">명령이 성공하고 *PassThru* 매개 변수를 지정하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명하는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="9c81d-112">규칙 식별자는 **ResourceGroupName,** **ServerName, DatabaseName** 및 RuleId를 포함하지만 **제한되지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="9c81d-112">Rule identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, **DatabaseName**, and **RuleId**.</span></span>
<span data-ttu-id="9c81d-113">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="9c81d-114">예제</span><span class="sxs-lookup"><span data-stu-id="9c81d-114">EXAMPLES</span></span>

### <span data-ttu-id="9c81d-115">예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경</span><span class="sxs-lookup"><span data-stu-id="9c81d-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="9c81d-116">이 명령은 ID Rule17이 있는 데이터 마스킹 규칙을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="9c81d-117">이 규칙은 Server01의 Database01 데이터베이스에서 작동됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="9c81d-118">이 명령은 난수가 마스킹된 값으로 생성되는 간격의 경계를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="9c81d-119">새 범위는 23에서 42 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="9c81d-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="9c81d-120">Example 2</span></span>

<span data-ttu-id="9c81d-121">데이터베이스에 대한 데이터 마스킹 규칙의 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="9c81d-122">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="9c81d-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="9c81d-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c81d-123">PARAMETERS</span></span>

### <span data-ttu-id="9c81d-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="9c81d-124">-ColumnName</span></span>
<span data-ttu-id="9c81d-125">마스킹 규칙에 의해 대상이 지정된 열의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="9c81d-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c81d-126">-DatabaseName</span></span>
<span data-ttu-id="9c81d-127">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="9c81d-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c81d-128">-DefaultProfile</span></span>
<span data-ttu-id="9c81d-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9c81d-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c81d-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="9c81d-130">-MaskingFunction</span></span>
<span data-ttu-id="9c81d-131">규칙에서 사용하는 마스킹 함수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="9c81d-132">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="9c81d-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9c81d-133">기본값</span><span class="sxs-lookup"><span data-stu-id="9c81d-133">Default</span></span>
- <span data-ttu-id="9c81d-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="9c81d-134">NoMasking</span></span>
- <span data-ttu-id="9c81d-135">텍스트</span><span class="sxs-lookup"><span data-stu-id="9c81d-135">Text</span></span>
- <span data-ttu-id="9c81d-136">숫자</span><span class="sxs-lookup"><span data-stu-id="9c81d-136">Number</span></span>
- <span data-ttu-id="9c81d-137">SocialSecurityNumber</span><span class="sxs-lookup"><span data-stu-id="9c81d-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="9c81d-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="9c81d-138">CreditCardNumber</span></span>
- <span data-ttu-id="9c81d-139">전자 메일의 기본값은 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-139">Email The default value is Default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c81d-140">-NumberFrom</span><span class="sxs-lookup"><span data-stu-id="9c81d-140">-NumberFrom</span></span>
<span data-ttu-id="9c81d-141">임의 값이 선택된 간격의 하한 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="9c81d-142">*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9c81d-143">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-143">The default value is 0.</span></span>

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

### <span data-ttu-id="9c81d-144">-NumberTo</span><span class="sxs-lookup"><span data-stu-id="9c81d-144">-NumberTo</span></span>
<span data-ttu-id="9c81d-145">임의 값이 선택된 간격의 상한 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="9c81d-146">*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9c81d-147">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-147">The default value is 0.</span></span>

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

### <span data-ttu-id="9c81d-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c81d-148">-PassThru</span></span>
<span data-ttu-id="9c81d-149">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9c81d-150">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9c81d-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="9c81d-151">-PrefixSize</span></span>
<span data-ttu-id="9c81d-152">마스킹되지 않은 텍스트의 시작에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="9c81d-153">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9c81d-154">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-154">The default value is 0.</span></span>

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

### <span data-ttu-id="9c81d-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="9c81d-155">-ReplacementString</span></span>
<span data-ttu-id="9c81d-156">마스킹되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="9c81d-157">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9c81d-158">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-158">The default value is 0.</span></span>

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

### <span data-ttu-id="9c81d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c81d-159">-ResourceGroupName</span></span>
<span data-ttu-id="9c81d-160">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9c81d-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="9c81d-161">-SchemaName</span></span>
<span data-ttu-id="9c81d-162">스마마의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="9c81d-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9c81d-163">-ServerName</span></span>
<span data-ttu-id="9c81d-164">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="9c81d-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="9c81d-165">-SuffixSize</span></span>
<span data-ttu-id="9c81d-166">마스킹되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="9c81d-167">*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="9c81d-168">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-168">The default value is 0.</span></span>

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

### <span data-ttu-id="9c81d-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="9c81d-169">-TableName</span></span>
<span data-ttu-id="9c81d-170">마스킹된 열이 포함된 데이터베이스 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="9c81d-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c81d-171">-Confirm</span></span>
<span data-ttu-id="9c81d-172">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c81d-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c81d-173">-WhatIf</span></span>
<span data-ttu-id="9c81d-174">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9c81d-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c81d-175">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c81d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c81d-176">CommonParameters</span></span>
<span data-ttu-id="9c81d-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c81d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c81d-178">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c81d-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c81d-179">입력</span><span class="sxs-lookup"><span data-stu-id="9c81d-179">INPUTS</span></span>

### <span data-ttu-id="9c81d-180">System.String</span><span class="sxs-lookup"><span data-stu-id="9c81d-180">System.String</span></span>

### <span data-ttu-id="9c81d-181">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c81d-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9c81d-182">System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9c81d-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="9c81d-183">출력</span><span class="sxs-lookup"><span data-stu-id="9c81d-183">OUTPUTS</span></span>

### <span data-ttu-id="9c81d-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span><span class="sxs-lookup"><span data-stu-id="9c81d-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="9c81d-185">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c81d-185">NOTES</span></span>

## <span data-ttu-id="9c81d-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c81d-186">RELATED LINKS</span></span>

[<span data-ttu-id="9c81d-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9c81d-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9c81d-188">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9c81d-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9c81d-189">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="9c81d-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="9c81d-190">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9c81d-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


