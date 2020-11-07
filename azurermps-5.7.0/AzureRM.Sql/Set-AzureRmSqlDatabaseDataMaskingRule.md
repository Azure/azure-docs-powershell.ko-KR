---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: dd29dd7e58a233d62e3af5260971d56300a43230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702339"
---
# <span data-ttu-id="a11d3-101">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a11d3-101">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>

## <span data-ttu-id="a11d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a11d3-102">SYNOPSIS</span></span>
<span data-ttu-id="a11d3-103">데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-103">Sets the properties of a data masking rule for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a11d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a11d3-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a11d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a11d3-105">DESCRIPTION</span></span>
<span data-ttu-id="a11d3-106">**AzureRmSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-106">The **Set-AzureRmSqlDatabaseDataMaskingRule** cmdlet sets a data masking rule for an Azure SQL database.</span></span>
<span data-ttu-id="a11d3-107">Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 제공 하 여 규칙을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-107">To use the cmdlet, provide the *ResourceGroupName* , *ServerName* , *DatabaseName* , and *RuleId* parameters to identify the rule.</span></span>
<span data-ttu-id="a11d3-108">*SchemaName* , *TableName* , *ColumnName* 의 매개 변수를 제공 하 여 규칙의 대상을 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-108">You can provide any of the parameters of *SchemaName* , *TableName* , and *ColumnName* to retarget the rule.</span></span>
<span data-ttu-id="a11d3-109">*MaskingFunction* 매개 변수를 지정 하 여 데이터 마스크 방법을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-109">Specify the *MaskingFunction* parameter to modify how the data is masked.</span></span>

<span data-ttu-id="a11d3-110">Number 또는 *MaskingFunction* 에 대 한 텍스트 값을 지정 *하는 경우* 숫자 마스킹에 대 한 매개 변수 및 번호 *를* 지정할 수 있으며, 텍스트 마스킹에 대 한 *PrefixSize* , *ReplacementString* 및 *SuffixSize* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-110">If you specify a value of Number or Text for *MaskingFunction* , you can specify the *NumberFrom* and *NumberTo* parameters for number masking or the *PrefixSize* , *ReplacementString* , and *SuffixSize* parameters for text masking.</span></span>
<span data-ttu-id="a11d3-111">명령이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-111">If the command succeeds, and if you specify the *PassThru* parameter, the cmdlet returns an object that describes the data masking rule properties and the rule identifiers.</span></span>
<span data-ttu-id="a11d3-112">규칙 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** , **RuleId** 이 포함 되지만이에 제한 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-112">Rule identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , **DatabaseName** , and **RuleId**.</span></span>

<span data-ttu-id="a11d3-113">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-113">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a11d3-114">예제의</span><span class="sxs-lookup"><span data-stu-id="a11d3-114">EXAMPLES</span></span>

### <span data-ttu-id="a11d3-115">예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경</span><span class="sxs-lookup"><span data-stu-id="a11d3-115">Example 1: Change the range of a data masking rule in a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

<span data-ttu-id="a11d3-116">이 명령은 ID Rule17 인 데이터 마스킹 규칙을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-116">This command modifies a data masking rule that has the ID Rule17.</span></span>
<span data-ttu-id="a11d3-117">이 규칙은 서버 Server01의 Database01 라는 데이터베이스에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-117">That rule operates in the database named Database01 on server Server01.</span></span>
<span data-ttu-id="a11d3-118">이 명령은 임의의 숫자가 마스킹된 값으로 생성 되는 간격의 경계를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-118">This command changes the boundaries for the interval in which a random number is generated as the masked value.</span></span>
<span data-ttu-id="a11d3-119">새 범위는 23 ~ 42입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-119">The new range is between 23 and 42.</span></span>

## <span data-ttu-id="a11d3-120">변수</span><span class="sxs-lookup"><span data-stu-id="a11d3-120">PARAMETERS</span></span>

### <span data-ttu-id="a11d3-121">-ColumnName</span><span class="sxs-lookup"><span data-stu-id="a11d3-121">-ColumnName</span></span>
<span data-ttu-id="a11d3-122">마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-122">Specifies the name of the column targeted by the masking rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-123">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a11d3-123">-DatabaseName</span></span>
<span data-ttu-id="a11d3-124">데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-124">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a11d3-125">-DefaultProfile</span></span>
<span data-ttu-id="a11d3-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a11d3-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-127">-MaskingFunction</span><span class="sxs-lookup"><span data-stu-id="a11d3-127">-MaskingFunction</span></span>
<span data-ttu-id="a11d3-128">규칙에서 사용 하는 마스킹 기능을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-128">Specifies the masking function that the rule uses.</span></span>
<span data-ttu-id="a11d3-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a11d3-130">기본값</span><span class="sxs-lookup"><span data-stu-id="a11d3-130">Default</span></span>
- <span data-ttu-id="a11d3-131">NoMasking</span><span class="sxs-lookup"><span data-stu-id="a11d3-131">NoMasking</span></span>
- <span data-ttu-id="a11d3-132">본문</span><span class="sxs-lookup"><span data-stu-id="a11d3-132">Text</span></span>
- <span data-ttu-id="a11d3-133">숫자로</span><span class="sxs-lookup"><span data-stu-id="a11d3-133">Number</span></span>
- <span data-ttu-id="a11d3-134">사회 Alsecurity번호</span><span class="sxs-lookup"><span data-stu-id="a11d3-134">SocialSecurityNumber</span></span>
- <span data-ttu-id="a11d3-135">CreditCardNumber</span><span class="sxs-lookup"><span data-stu-id="a11d3-135">CreditCardNumber</span></span>
- <span data-ttu-id="a11d3-136">메일 주소</span><span class="sxs-lookup"><span data-stu-id="a11d3-136">Email</span></span>

<span data-ttu-id="a11d3-137">기본값은 기본 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-137">The default value is Default.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-138">-번호</span><span class="sxs-lookup"><span data-stu-id="a11d3-138">-NumberFrom</span></span>
<span data-ttu-id="a11d3-139">임의의 값이 선택 되는 간격의 하한값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-139">Specifies the lower bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a11d3-140">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-140">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a11d3-141">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-141">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-142">-번호를</span><span class="sxs-lookup"><span data-stu-id="a11d3-142">-NumberTo</span></span>
<span data-ttu-id="a11d3-143">임의 값이 선택 된 간격의 상한 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-143">Specifies the upper bound number of the interval from which a random value is selected.</span></span>
<span data-ttu-id="a11d3-144">*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-144">Specify this parameter only if you specify a value of Number for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a11d3-145">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-145">The default value is 0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a11d3-146">-PassThru</span></span>
<span data-ttu-id="a11d3-147">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a11d3-148">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-148">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-149">-PrefixSize</span><span class="sxs-lookup"><span data-stu-id="a11d3-149">-PrefixSize</span></span>
<span data-ttu-id="a11d3-150">마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-150">Specifies the number of characters at the start of the text that are not masked.</span></span>
<span data-ttu-id="a11d3-151">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-151">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a11d3-152">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-152">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-153">-ReplacementString</span><span class="sxs-lookup"><span data-stu-id="a11d3-153">-ReplacementString</span></span>
<span data-ttu-id="a11d3-154">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-154">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="a11d3-155">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-155">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a11d3-156">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-156">The default value is 0.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-157">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a11d3-157">-ResourceGroupName</span></span>
<span data-ttu-id="a11d3-158">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-158">Specifies the name of the resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-159">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="a11d3-159">-SchemaName</span></span>
<span data-ttu-id="a11d3-160">스키마의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-160">Specifies the name of a schema.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-161">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a11d3-161">-ServerName</span></span>
<span data-ttu-id="a11d3-162">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-162">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-163">-SuffixSize</span><span class="sxs-lookup"><span data-stu-id="a11d3-163">-SuffixSize</span></span>
<span data-ttu-id="a11d3-164">마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-164">Specifies the number of characters at the end of the text that are not masked.</span></span>
<span data-ttu-id="a11d3-165">*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-165">Specify this parameter only if you specify a value of Text for the *MaskingFunction* parameter.</span></span>
<span data-ttu-id="a11d3-166">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-166">The default value is 0.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-167">-TableName</span><span class="sxs-lookup"><span data-stu-id="a11d3-167">-TableName</span></span>
<span data-ttu-id="a11d3-168">마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-168">Specifies the name of the database table that contains the masked column.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-169">-확인</span><span class="sxs-lookup"><span data-stu-id="a11d3-169">-Confirm</span></span>
<span data-ttu-id="a11d3-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a11d3-171">-WhatIf</span></span>
<span data-ttu-id="a11d3-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a11d3-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-173">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a11d3-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a11d3-174">CommonParameters</span></span>
<span data-ttu-id="a11d3-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a11d3-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a11d3-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a11d3-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a11d3-177">입력</span><span class="sxs-lookup"><span data-stu-id="a11d3-177">INPUTS</span></span>

###  
<span data-ttu-id="a11d3-178">않아야</span><span class="sxs-lookup"><span data-stu-id="a11d3-178">None</span></span>

## <span data-ttu-id="a11d3-179">출력</span><span class="sxs-lookup"><span data-stu-id="a11d3-179">OUTPUTS</span></span>

### <span data-ttu-id="a11d3-180">DatabaseDataMaskingRuleModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="a11d3-180">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingRuleModel</span></span>

## <span data-ttu-id="a11d3-181">상속자</span><span class="sxs-lookup"><span data-stu-id="a11d3-181">NOTES</span></span>

## <span data-ttu-id="a11d3-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a11d3-182">RELATED LINKS</span></span>

[<span data-ttu-id="a11d3-183">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a11d3-183">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a11d3-184">새로운 AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a11d3-184">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a11d3-185">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a11d3-185">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a11d3-186">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a11d3-186">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


