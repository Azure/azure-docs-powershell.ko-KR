---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213895"
---
# <span data-ttu-id="60079-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="60079-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="60079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60079-102">SYNOPSIS</span></span>
<span data-ttu-id="60079-103">데이터베이스에 대 한 데이터 마스킹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="60079-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60079-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60079-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60079-105">DESCRIPTION</span></span>
<span data-ttu-id="60079-106">**AzSqlDatabaseDataMaskingPolicy** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="60079-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="60079-108">*DataMaskingState* 매개 변수를 설정 하 여 데이터 마스킹 작업을 사용할지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60079-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="60079-109">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 데이터 마스킹 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="60079-110">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60079-110">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>
<span data-ttu-id="60079-111">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60079-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="60079-112">예제의</span><span class="sxs-lookup"><span data-stu-id="60079-112">EXAMPLES</span></span>

### <span data-ttu-id="60079-113">예제 1: 데이터베이스에 대 한 데이터 마스킹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="60079-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="60079-114">이 명령은 server01 라는 서버의 database01 이라는 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="60079-115">변수</span><span class="sxs-lookup"><span data-stu-id="60079-115">PARAMETERS</span></span>

### <span data-ttu-id="60079-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="60079-116">-DatabaseName</span></span>
<span data-ttu-id="60079-117">정책이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="60079-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="60079-118">-DataMaskingState</span></span>
<span data-ttu-id="60079-119">데이터 마스킹 작업을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="60079-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="60079-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="60079-121">수</span><span class="sxs-lookup"><span data-stu-id="60079-121">Enabled</span></span>
- <span data-ttu-id="60079-122">사용 안 함 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-122">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="60079-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60079-123">-DefaultProfile</span></span>
<span data-ttu-id="60079-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60079-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="60079-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60079-125">-PassThru</span></span>
<span data-ttu-id="60079-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="60079-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60079-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="60079-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="60079-128">-PrivilegedUsers</span></span>
<span data-ttu-id="60079-129">세미콜론으로 구분 된 권한 있는 사용자 Id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="60079-130">이러한 사용자는 마스크 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="60079-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="60079-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60079-131">-ResourceGroupName</span></span>
<span data-ttu-id="60079-132">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="60079-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="60079-133">-ServerName</span></span>
<span data-ttu-id="60079-134">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="60079-135">-확인</span><span class="sxs-lookup"><span data-stu-id="60079-135">-Confirm</span></span>
<span data-ttu-id="60079-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60079-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60079-137">-WhatIf</span></span>
<span data-ttu-id="60079-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="60079-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60079-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60079-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60079-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60079-140">CommonParameters</span></span>
<span data-ttu-id="60079-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60079-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60079-142">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="60079-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60079-143">입력</span><span class="sxs-lookup"><span data-stu-id="60079-143">INPUTS</span></span>

### <span data-ttu-id="60079-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="60079-144">System.String</span></span>

## <span data-ttu-id="60079-145">출력</span><span class="sxs-lookup"><span data-stu-id="60079-145">OUTPUTS</span></span>

### <span data-ttu-id="60079-146">DataMasking. DatabaseDataMaskingPolicyModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="60079-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="60079-147">상속자</span><span class="sxs-lookup"><span data-stu-id="60079-147">NOTES</span></span>

## <span data-ttu-id="60079-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60079-148">RELATED LINKS</span></span>

[<span data-ttu-id="60079-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="60079-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="60079-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="60079-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="60079-151">새로운 AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="60079-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="60079-152">제거-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="60079-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="60079-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="60079-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="60079-154">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="60079-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


