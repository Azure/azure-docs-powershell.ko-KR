---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: FFC02A5D-A12F-494D-8542-76A5B89E32DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: 8fb1b8125a6fd0c42bedc00733f3a128846673e4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176988"
---
# <span data-ttu-id="f8c9f-101">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f8c9f-101">Get-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="f8c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c9f-103">데이터베이스에 대한 데이터 마스킹 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-103">Gets the data masking policy for a database.</span></span>

## <span data-ttu-id="f8c9f-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8c9f-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseDataMaskingPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f8c9f-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8c9f-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c9f-106">**Get-AzSqlDatabaseDataMaskingPolicy** cmdlet은 Azure SQL 데이터베이스의 데이터 마스킹 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-106">The **Get-AzSqlDatabaseDataMaskingPolicy** cmdlet gets the data masking policy of an Azure SQL database.</span></span>
<span data-ttu-id="f8c9f-107">이 cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 데이터베이스를 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="f8c9f-108">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="f8c9f-109">예제</span><span class="sxs-lookup"><span data-stu-id="f8c9f-109">EXAMPLES</span></span>

### <span data-ttu-id="f8c9f-110">예제 1: Azure SQL 데이터베이스에 대한 데이터 마스킹 정책 사용</span><span class="sxs-lookup"><span data-stu-id="f8c9f-110">Example 1: Get the data masking policy for an Azure SQL database</span></span>
```
PS C:\>Get-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
DatabaseName      : Database01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
DataMaskingState  : Enabled
PrivilegedUsers  :
```

<span data-ttu-id="f8c9f-111">이 명령은 server Server01의 리소스 그룹 ResourceGroup01에 있는 Database01에서 데이터 마스킹 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-111">This command gets the data masking policy from database Database01 in resource group ResourceGroup01 on server Server01.</span></span>

## <span data-ttu-id="f8c9f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8c9f-112">PARAMETERS</span></span>

### <span data-ttu-id="f8c9f-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8c9f-113">-DatabaseName</span></span>
<span data-ttu-id="f8c9f-114">데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-114">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="f8c9f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c9f-115">-DefaultProfile</span></span>
<span data-ttu-id="f8c9f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f8c9f-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f8c9f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c9f-117">-ResourceGroupName</span></span>
<span data-ttu-id="f8c9f-118">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f8c9f-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f8c9f-119">-ServerName</span></span>
<span data-ttu-id="f8c9f-120">데이터베이스가 있는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-120">Specifies the name of the server where the database is located.</span></span>

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

### <span data-ttu-id="f8c9f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8c9f-121">-Confirm</span></span>
<span data-ttu-id="f8c9f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c9f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c9f-123">-WhatIf</span></span>
<span data-ttu-id="f8c9f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f8c9f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8c9f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c9f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c9f-126">CommonParameters</span></span>
<span data-ttu-id="f8c9f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c9f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f8c9f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c9f-129">입력</span><span class="sxs-lookup"><span data-stu-id="f8c9f-129">INPUTS</span></span>

### <span data-ttu-id="f8c9f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f8c9f-130">System.String</span></span>

## <span data-ttu-id="f8c9f-131">출력</span><span class="sxs-lookup"><span data-stu-id="f8c9f-131">OUTPUTS</span></span>

### <span data-ttu-id="f8c9f-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="f8c9f-132">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="f8c9f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8c9f-133">NOTES</span></span>

## <span data-ttu-id="f8c9f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8c9f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f8c9f-135">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f8c9f-135">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f8c9f-136">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f8c9f-136">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f8c9f-137">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f8c9f-137">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="f8c9f-138">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="f8c9f-138">Set-AzSqlDatabaseDataMaskingPolicy</span></span>](./Set-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="f8c9f-139">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="f8c9f-139">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)


