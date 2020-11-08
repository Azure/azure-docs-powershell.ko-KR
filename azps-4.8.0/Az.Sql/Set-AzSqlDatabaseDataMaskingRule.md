---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213885"
---
# <span data-ttu-id="58bd4-101">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="58bd4-101">Set-AzSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="58bd4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58bd4-102">SYNOPSIS</span></span>
<span data-ttu-id="58bd4-103">데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-103">Sets the properties of a data masking rule for a database.</span></span>

## <span data-ttu-id="58bd4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58bd4-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="58bd4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58bd4-105">DESCRIPTION</span></span>
<span data-ttu-id="58bd4-106">**AzSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-106">The **Set-AzSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="58bd4-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 제공 하 여 규칙을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="58bd4-108">*SchemaName* , *TableName* , *ColumnName* 의 매개 변수를 제공 하 여 규칙의 대상을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="58bd4-109">*MaskingFunction* 매개 변수를 지정 하 여 데이터 마스크 방법을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>
<span data-ttu-id="58bd4-110">Number 또는 *MaskingFunction* 에 대 한 텍스트 값을 지정 *하는 경우* 숫자 마스킹에 대 한 매개 변수 및 번호 *를* 지정할 수 있으며, 텍스트 마스킹에 대 한 *PrefixSize* , *ReplacementString* 및 *SuffixSize* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="58bd4-111">명령이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="58bd4-112">규칙 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** , **RuleId** 이 포함 되지만이에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>
<span data-ttu-id="58bd4-113">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="58bd4-114">예제의</span><span class="sxs-lookup"><span data-stu-id="58bd4-114">EXAMPLES</span></span>

### <span data-ttu-id="58bd4-115">예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경</span><span class="sxs-lookup"><span data-stu-id="58bd4-115">Example 1: Change the range of a data masking rule in a database</span></span>
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="58bd4-116">이 명령은 ID Rule17 인 데이터 마스킹 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="58bd4-117">이 규칙은 서버 Server01의 Database01 라는 데이터베이스에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="58bd4-118">이 명령은 임의의 숫자가 마스킹된 값으로 생성 되는 간격의 경계를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="58bd4-119">새 범위는 23 ~ 42입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-119">The new range is between 23 and 42.</span></span>

### <span data-ttu-id="58bd4-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="58bd4-120">Example 2</span></span>

<span data-ttu-id="58bd4-121">데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-121">Sets the properties of a data masking rule for a database.</span></span> <span data-ttu-id="58bd4-122">생성</span><span class="sxs-lookup"><span data-stu-id="58bd4-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## <span data-ttu-id="58bd4-123">변수</span><span class="sxs-lookup"><span data-stu-id="58bd4-123">PARAMETERS</span></span>

### <span data-ttu-id="58bd4-124">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="58bd4-124">-ColumnName</span></span>
<span data-ttu-id="58bd4-125">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-125">Specifies the name of the column targeted by the masking rule.</span></span>

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

### <span data-ttu-id="58bd4-126">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="58bd4-126">-DatabaseName</span></span>
<span data-ttu-id="58bd4-127">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-127">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="58bd4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58bd4-128">-DefaultProfile</span></span>
<span data-ttu-id="58bd4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="58bd4-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58bd4-130">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="58bd4-130">-MaskingFunction</span></span>
<span data-ttu-id="58bd4-131">규칙에서 사용 하는 마스킹 기능을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-131">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="58bd4-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="58bd4-133">기본값</span><span class="sxs-lookup"><span data-stu-id="58bd4-133">Default</span></span>
- <span data-ttu-id="58bd4-134">NoMasking</span><span class="sxs-lookup"><span data-stu-id="58bd4-134">NoMasking</span></span>
- <span data-ttu-id="58bd4-135">본문</span><span class="sxs-lookup"><span data-stu-id="58bd4-135">Text</span></span>
- <span data-ttu-id="58bd4-136">숫자로</span><span class="sxs-lookup"><span data-stu-id="58bd4-136">Number</span></span>
- <span data-ttu-id="58bd4-137">사회 Alsecurity번호</span><span class="sxs-lookup"><span data-stu-id="58bd4-137">SocialSecurityNumber</span></span>
- <span data-ttu-id="58bd4-138">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="58bd4-138">CreditCardNumber</span></span>
- <span data-ttu-id="58bd4-139">전자 메일 기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-139">Email The default value is Default.</span></span>

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

### <span data-ttu-id="58bd4-140">-번호</span><span class="sxs-lookup"><span data-stu-id="58bd4-140">-NumberFrom</span></span>
<span data-ttu-id="58bd4-141">임의의 값이 선택 되는 간격의 하한값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-141">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="58bd4-142">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-142">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="58bd4-143">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-143">The default value is 0.</span></span>

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

### <span data-ttu-id="58bd4-144">-번호를</span><span class="sxs-lookup"><span data-stu-id="58bd4-144">-NumberTo</span></span>
<span data-ttu-id="58bd4-145">임의 값이 선택 된 간격의 상한 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-145">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="58bd4-146">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-146">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="58bd4-147">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-147">The default value is 0.</span></span>

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

### <span data-ttu-id="58bd4-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58bd4-148">-PassThru</span></span>
<span data-ttu-id="58bd4-149">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-149">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="58bd4-150">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-150">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58bd4-151">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="58bd4-151">-PrefixSize</span></span>
<span data-ttu-id="58bd4-152">마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-152">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="58bd4-153">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-153">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="58bd4-154">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-154">The default value is 0.</span></span>

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

### <span data-ttu-id="58bd4-155">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="58bd4-155">-ReplacementString</span></span>
<span data-ttu-id="58bd4-156">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-156">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="58bd4-157">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-157">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="58bd4-158">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-158">The default value is 0.</span></span>

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

### <span data-ttu-id="58bd4-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58bd4-159">-ResourceGroupName</span></span>
<span data-ttu-id="58bd4-160">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-160">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="58bd4-161">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="58bd4-161">-SchemaName</span></span>
<span data-ttu-id="58bd4-162">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-162">Specifies the name of a schema.</span></span>

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

### <span data-ttu-id="58bd4-163">-ServerName</span><span class="sxs-lookup"><span data-stu-id="58bd4-163">-ServerName</span></span>
<span data-ttu-id="58bd4-164">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-164">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="58bd4-165">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="58bd4-165">-SuffixSize</span></span>
<span data-ttu-id="58bd4-166">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-166">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="58bd4-167">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-167">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="58bd4-168">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-168">The default value is 0.</span></span>

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

### <span data-ttu-id="58bd4-169">-TableName</span><span class="sxs-lookup"><span data-stu-id="58bd4-169">-TableName</span></span>
<span data-ttu-id="58bd4-170">마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-170">Specifies the name of the database table that contains the masked column.</span></span>

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

### <span data-ttu-id="58bd4-171">-확인</span><span class="sxs-lookup"><span data-stu-id="58bd4-171">-Confirm</span></span>
<span data-ttu-id="58bd4-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58bd4-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58bd4-173">-WhatIf</span></span>
<span data-ttu-id="58bd4-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58bd4-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58bd4-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58bd4-176">CommonParameters</span></span>
<span data-ttu-id="58bd4-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58bd4-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58bd4-178">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58bd4-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58bd4-179">입력</span><span class="sxs-lookup"><span data-stu-id="58bd4-179">INPUTS</span></span>

### <span data-ttu-id="58bd4-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58bd4-180">System.String</span></span>

### <span data-ttu-id="58bd4-181">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58bd4-181">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="58bd4-182">시스템 Null 허용 ' 1 [[4.0.0.0] [[System.webserver, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="58bd4-182">System.Nullable\`1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="58bd4-183">출력</span><span class="sxs-lookup"><span data-stu-id="58bd4-183">OUTPUTS</span></span>

### <span data-ttu-id="58bd4-184">DataMasking. DatabaseDataMaskingRuleModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="58bd4-184">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="58bd4-185">상속자</span><span class="sxs-lookup"><span data-stu-id="58bd4-185">NOTES</span></span>

## <span data-ttu-id="58bd4-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58bd4-186">RELATED LINKS</span></span>

[<span data-ttu-id="58bd4-187">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="58bd4-187">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="58bd4-188">새로운 AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="58bd4-188">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="58bd4-189">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="58bd4-189">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="58bd4-190">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="58bd4-190">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


