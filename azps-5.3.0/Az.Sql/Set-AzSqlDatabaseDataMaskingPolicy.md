---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489480"
---
# <span data-ttu-id="a583d-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a583d-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="a583d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a583d-102">SYNOPSIS</span></span>
<span data-ttu-id="a583d-103">데이터베이스에 대한 데이터 마스킹을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="a583d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a583d-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a583d-105">설명</span><span class="sxs-lookup"><span data-stu-id="a583d-105">DESCRIPTION</span></span>
<span data-ttu-id="a583d-106">**Set-AzSqlDatabaseDataMaskingPolicy** cmdlet은 Azure SQL 데이터베이스에 대한 데이터 마스킹 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="a583d-107">이 cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="a583d-108">*DataMaskingState* 매개 변수를 설정하여 데이터 마스킹 작업을 사용하도록 설정하거나 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="a583d-109">cmdlet이 성공하고 *PassThru* 매개 변수를 사용하는 경우 데이터베이스 식별자 외에도 현재 데이터 마스킹 정책을 설명하는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="a583d-110">데이터베이스 식별자는 **ResourceGroupName, ServerName** 및 DatabaseName을 포함하지만 **제한되지 않습니다.** </span><span class="sxs-lookup"><span data-stu-id="a583d-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="a583d-111">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="a583d-112">예제</span><span class="sxs-lookup"><span data-stu-id="a583d-112">EXAMPLES</span></span>

### <span data-ttu-id="a583d-113">예제 1: 데이터베이스에 대한 데이터 마스킹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="a583d-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="a583d-114">이 명령은 server01이라는 서버에서 database01이라는 데이터베이스에 대한 데이터 마스킹 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="a583d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a583d-115">PARAMETERS</span></span>

### <span data-ttu-id="a583d-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a583d-116">-DatabaseName</span></span>
<span data-ttu-id="a583d-117">정책이 설정된 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-117">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="a583d-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="a583d-118">-DataMaskingState</span></span>
<span data-ttu-id="a583d-119">데이터 마스킹 작업을 사용하도록 설정하거나 사용하지 않도록 설정할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="a583d-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a583d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a583d-121">사용</span><span class="sxs-lookup"><span data-stu-id="a583d-121">Enabled</span></span>
- <span data-ttu-id="a583d-122">사용 안 하게 설정: 기본값은 사용입니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-122">Disabled The default value is Enabled.</span></span>

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

### <span data-ttu-id="a583d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a583d-123">-DefaultProfile</span></span>
<span data-ttu-id="a583d-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a583d-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a583d-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a583d-125">-PassThru</span></span>
<span data-ttu-id="a583d-126">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a583d-127">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a583d-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="a583d-128">-PrivilegedUsers</span></span>
<span data-ttu-id="a583d-129">권한 있는 사용자 ID의 세미코론으로 구분된 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="a583d-130">이러한 사용자는 마스킹 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="a583d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a583d-131">-ResourceGroupName</span></span>
<span data-ttu-id="a583d-132">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="a583d-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a583d-133">-ServerName</span></span>
<span data-ttu-id="a583d-134">데이터베이스를 호스팅하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-134">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="a583d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a583d-135">-Confirm</span></span>
<span data-ttu-id="a583d-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a583d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a583d-137">-WhatIf</span></span>
<span data-ttu-id="a583d-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a583d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a583d-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a583d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a583d-140">CommonParameters</span></span>
<span data-ttu-id="a583d-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a583d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a583d-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a583d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a583d-143">입력</span><span class="sxs-lookup"><span data-stu-id="a583d-143">INPUTS</span></span>

### <span data-ttu-id="a583d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="a583d-144">System.String</span></span>

## <span data-ttu-id="a583d-145">출력</span><span class="sxs-lookup"><span data-stu-id="a583d-145">OUTPUTS</span></span>

### <span data-ttu-id="a583d-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="a583d-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="a583d-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a583d-147">NOTES</span></span>

## <span data-ttu-id="a583d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a583d-148">RELATED LINKS</span></span>

[<span data-ttu-id="a583d-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="a583d-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="a583d-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a583d-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a583d-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a583d-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a583d-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a583d-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a583d-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="a583d-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="a583d-154">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a583d-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


