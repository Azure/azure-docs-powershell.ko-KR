---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: e0af0c6d741e45c2e00e958342fad940acc2c3e0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698798"
---
# <span data-ttu-id="e7e62-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7e62-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="e7e62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7e62-102">SYNOPSIS</span></span>
<span data-ttu-id="e7e62-103">데이터베이스에 대 한 데이터 마스킹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="e7e62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7e62-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e7e62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e7e62-105">DESCRIPTION</span></span>
<span data-ttu-id="e7e62-106">**AzSqlDatabaseDataMaskingPolicy** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="e7e62-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="e7e62-108">*DataMaskingState* 매개 변수를 설정 하 여 데이터 마스킹 작업을 사용할지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="e7e62-109">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 데이터 마스킹 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="e7e62-110">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="e7e62-111">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="e7e62-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e7e62-112">EXAMPLES</span></span>

### <span data-ttu-id="e7e62-113">예제 1: 데이터베이스에 대 한 데이터 마스킹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="e7e62-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="e7e62-114">이 명령은 server01 라는 서버의 database01 이라는 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="e7e62-115">변수</span><span class="sxs-lookup"><span data-stu-id="e7e62-115">PARAMETERS</span></span>

### <span data-ttu-id="e7e62-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e7e62-116">-DatabaseName</span></span>
<span data-ttu-id="e7e62-117">정책이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="e7e62-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="e7e62-118">-DataMaskingState</span></span>
<span data-ttu-id="e7e62-119">데이터 마스킹 작업을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="e7e62-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e7e62-121">수</span><span class="sxs-lookup"><span data-stu-id="e7e62-121">Enabled</span></span>
- <span data-ttu-id="e7e62-122">사용 안 함 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e7e62-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7e62-123">-DefaultProfile</span></span>
<span data-ttu-id="e7e62-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e7e62-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e7e62-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7e62-125">-PassThru</span></span>
<span data-ttu-id="e7e62-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e7e62-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e7e62-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="e7e62-128">-PrivilegedUsers</span></span>
<span data-ttu-id="e7e62-129">세미콜론으로 구분 된 권한 있는 사용자 Id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="e7e62-130">이러한 사용자는 마스크 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="e7e62-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7e62-131">-ResourceGroupName</span></span>
<span data-ttu-id="e7e62-132">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="e7e62-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="e7e62-133">-ServerName</span></span>
<span data-ttu-id="e7e62-134">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="e7e62-135">-확인</span><span class="sxs-lookup"><span data-stu-id="e7e62-135">-Confirm</span></span>
<span data-ttu-id="e7e62-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7e62-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7e62-137">-WhatIf</span></span>
<span data-ttu-id="e7e62-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7e62-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7e62-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7e62-140">CommonParameters</span></span>
<span data-ttu-id="e7e62-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7e62-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7e62-142">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7e62-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7e62-143">입력</span><span class="sxs-lookup"><span data-stu-id="e7e62-143">INPUTS</span></span>

### <span data-ttu-id="e7e62-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e7e62-144">System.String</span></span>

## <span data-ttu-id="e7e62-145">출력</span><span class="sxs-lookup"><span data-stu-id="e7e62-145">OUTPUTS</span></span>

### <span data-ttu-id="e7e62-146">DataMasking. DatabaseDataMaskingPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="e7e62-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="e7e62-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e7e62-147">NOTES</span></span>

## <span data-ttu-id="e7e62-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7e62-148">RELATED LINKS</span></span>

[<span data-ttu-id="e7e62-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="e7e62-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="e7e62-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7e62-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7e62-151">새로운 AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7e62-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7e62-152">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7e62-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7e62-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="e7e62-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="e7e62-154">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="e7e62-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


