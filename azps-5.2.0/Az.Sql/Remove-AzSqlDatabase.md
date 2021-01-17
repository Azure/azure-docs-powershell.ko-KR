---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: a0a232ae48b47759be4a4dde9a8d80e56fc88106
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323749"
---
# <span data-ttu-id="5be29-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="5be29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5be29-102">SYNOPSIS</span></span>
<span data-ttu-id="5be29-103">Azure SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="5be29-104">구문</span><span class="sxs-lookup"><span data-stu-id="5be29-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5be29-105">설명</span><span class="sxs-lookup"><span data-stu-id="5be29-105">DESCRIPTION</span></span>
<span data-ttu-id="5be29-106">**Remove-AzSqlDatabase** cmdlet은 Azure SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="5be29-107">이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="5be29-108">예제</span><span class="sxs-lookup"><span data-stu-id="5be29-108">EXAMPLES</span></span>

### <span data-ttu-id="5be29-109">예제 1: Azure SQL 서버에서 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="5be29-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="5be29-110">이 명령은 server Server01에서 Database01이라는 데이터베이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="5be29-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5be29-111">PARAMETERS</span></span>

### <span data-ttu-id="5be29-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="5be29-112">-DatabaseName</span></span>
<span data-ttu-id="5be29-113">이 cmdlet이 제거하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5be29-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5be29-114">-DefaultProfile</span></span>
<span data-ttu-id="5be29-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5be29-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5be29-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5be29-116">-Force</span></span>
<span data-ttu-id="5be29-117">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5be29-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5be29-118">-ResourceGroupName</span></span>
<span data-ttu-id="5be29-119">데이터베이스가 할당된 Azure 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="5be29-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="5be29-120">-ServerName</span></span>
<span data-ttu-id="5be29-121">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="5be29-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5be29-122">-Confirm</span></span>
<span data-ttu-id="5be29-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5be29-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5be29-124">-WhatIf</span></span>
<span data-ttu-id="5be29-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5be29-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5be29-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5be29-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5be29-127">CommonParameters</span></span>
<span data-ttu-id="5be29-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5be29-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5be29-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5be29-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5be29-130">입력</span><span class="sxs-lookup"><span data-stu-id="5be29-130">INPUTS</span></span>

### <span data-ttu-id="5be29-131">System.String</span><span class="sxs-lookup"><span data-stu-id="5be29-131">System.String</span></span>

## <span data-ttu-id="5be29-132">출력</span><span class="sxs-lookup"><span data-stu-id="5be29-132">OUTPUTS</span></span>

### <span data-ttu-id="5be29-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="5be29-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="5be29-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5be29-134">NOTES</span></span>

## <span data-ttu-id="5be29-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5be29-135">RELATED LINKS</span></span>

[<span data-ttu-id="5be29-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="5be29-137">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="5be29-138">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="5be29-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="5be29-140">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="5be29-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="5be29-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="5be29-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


