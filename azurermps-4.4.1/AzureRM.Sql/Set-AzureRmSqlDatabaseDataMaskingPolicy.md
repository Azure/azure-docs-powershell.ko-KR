---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 72ee5f7bd636747b4321e1c87b78fdb37ed84dc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702675"
---
# <span data-ttu-id="ae1a0-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae1a0-101">Set-AzureRmSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="ae1a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ae1a0-103">데이터베이스에 대 한 데이터 마스킹을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-103">Sets data masking for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae1a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae1a0-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedLogins <String>] [-PrivilegedUsers <String>]
 [-DataMaskingState <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae1a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ae1a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ae1a0-106">**AzureRmSqlDatabaseDataMaskingPolicy** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-106">The **Set-AzureRmSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="ae1a0-107">이 cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* 및 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-107">To use this cmdlet, use the *ResourceGroupName* , *ServerName* , and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="ae1a0-108">*DataMaskingState* 매개 변수를 설정 하 여 데이터 마스킹 작업을 사용할지 여부를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>

<span data-ttu-id="ae1a0-109">*PrivilegedLogins* 매개 변수를 설정 하 여 마스크 되지 않은 데이터를 볼 수 있는 사용자를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-109">You can also set the *PrivilegedLogins* parameter to specify which users are allowed to see the unmasked data.</span></span>
<span data-ttu-id="ae1a0-110">Cmdlet이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 데이터베이스 식별자 외에도 현재 데이터 마스킹 정책을 설명 하는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-110">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="ae1a0-111">데이터베이스 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-111">Database identifiers include, but are not limited to, **ResourceGroupName** , **ServerName** , and **DatabaseName**.</span></span>

<span data-ttu-id="ae1a0-112">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-112">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="ae1a0-113">예제의</span><span class="sxs-lookup"><span data-stu-id="ae1a0-113">EXAMPLES</span></span>

### <span data-ttu-id="ae1a0-114">예제 1: 데이터베이스에 대 한 데이터 마스킹 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ae1a0-114">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="ae1a0-115">이 명령은 server01 라는 서버의 database01 이라는 데이터베이스에 대 한 데이터 마스킹 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-115">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="ae1a0-116">변수</span><span class="sxs-lookup"><span data-stu-id="ae1a0-116">PARAMETERS</span></span>

### <span data-ttu-id="ae1a0-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ae1a0-117">-DatabaseName</span></span>
<span data-ttu-id="ae1a0-118">정책이 설정 된 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-118">Specifies the name of the database where the policy is set.</span></span>

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

### <span data-ttu-id="ae1a0-119">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="ae1a0-119">-DataMaskingState</span></span>
<span data-ttu-id="ae1a0-120">데이터 마스킹 작업을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-120">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="ae1a0-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae1a0-122">수</span><span class="sxs-lookup"><span data-stu-id="ae1a0-122">Enabled</span></span>
- <span data-ttu-id="ae1a0-123">비활성화</span><span class="sxs-lookup"><span data-stu-id="ae1a0-123">Disabled</span></span>

<span data-ttu-id="ae1a0-124">기본값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-124">The default value is Enabled.</span></span>

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

### <span data-ttu-id="ae1a0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae1a0-125">-PassThru</span></span>
<span data-ttu-id="ae1a0-126">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ae1a0-127">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ae1a0-128">-PrivilegedLogins</span><span class="sxs-lookup"><span data-stu-id="ae1a0-128">-PrivilegedLogins</span></span>
<span data-ttu-id="ae1a0-129">마스킹에서 제외 되는 SQL 사용자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-129">Specifies which SQL users are excluded from masking.</span></span>

<span data-ttu-id="ae1a0-130">이 매개 변수는 더 이상 사용 되지 않으며 이후 릴리스에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-130">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="ae1a0-131">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="ae1a0-131">-PrivilegedUsers</span></span>
<span data-ttu-id="ae1a0-132">세미콜론으로 구분 된 권한 있는 사용자 Id 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-132">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="ae1a0-133">이러한 사용자는 마스크 데이터를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-133">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="ae1a0-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae1a0-134">-ResourceGroupName</span></span>
<span data-ttu-id="ae1a0-135">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-135">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="ae1a0-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ae1a0-136">-ServerName</span></span>
<span data-ttu-id="ae1a0-137">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-137">Specifies the name of the server hosting the database.</span></span>

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

### <span data-ttu-id="ae1a0-138">-확인</span><span class="sxs-lookup"><span data-stu-id="ae1a0-138">-Confirm</span></span>
<span data-ttu-id="ae1a0-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae1a0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae1a0-140">-WhatIf</span></span>
<span data-ttu-id="ae1a0-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae1a0-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae1a0-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae1a0-143">-DefaultProfile</span></span>
<span data-ttu-id="ae1a0-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae1a0-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae1a0-145">CommonParameters</span></span>
<span data-ttu-id="ae1a0-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae1a0-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae1a0-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae1a0-148">입력</span><span class="sxs-lookup"><span data-stu-id="ae1a0-148">INPUTS</span></span>

## <span data-ttu-id="ae1a0-149">출력</span><span class="sxs-lookup"><span data-stu-id="ae1a0-149">OUTPUTS</span></span>

### <span data-ttu-id="ae1a0-150">DatabaseDataMaskingPolicyModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="ae1a0-150">Microsoft.Azure.Commands.Sql.Security.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="ae1a0-151">상속자</span><span class="sxs-lookup"><span data-stu-id="ae1a0-151">NOTES</span></span>

## <span data-ttu-id="ae1a0-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae1a0-152">RELATED LINKS</span></span>

[<span data-ttu-id="ae1a0-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="ae1a0-153">Get-AzureRmSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzureRmSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="ae1a0-154">Get-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae1a0-154">Get-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae1a0-155">새로운 AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae1a0-155">New-AzureRmSqlDatabaseDataMaskingRule</span></span>](./New-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae1a0-156">제거-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae1a0-156">Remove-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae1a0-157">Set-AzureRmSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="ae1a0-157">Set-AzureRmSqlDatabaseDataMaskingRule</span></span>](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="ae1a0-158">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="ae1a0-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


