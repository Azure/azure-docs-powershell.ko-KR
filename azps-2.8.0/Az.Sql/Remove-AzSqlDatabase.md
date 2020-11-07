---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabase.md
ms.openlocfilehash: 200e53ef1f23c4b829380a2c8b7ca663443e5f7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873591"
---
# <span data-ttu-id="4150f-101">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-101">Remove-AzSqlDatabase</span></span>

## <span data-ttu-id="4150f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4150f-102">SYNOPSIS</span></span>
<span data-ttu-id="4150f-103">Azure SQL 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-103">Removes an Azure SQL database.</span></span>

## <span data-ttu-id="4150f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4150f-104">SYNTAX</span></span>

```
Remove-AzSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4150f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4150f-105">DESCRIPTION</span></span>
<span data-ttu-id="4150f-106">**AzSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-106">The **Remove-AzSqlDatabase** cmdlet removes an Azure SQL database.</span></span>
<span data-ttu-id="4150f-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="4150f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4150f-108">EXAMPLES</span></span>

### <span data-ttu-id="4150f-109">예제 1: Azure SQL server에서 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="4150f-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4150f-110">이 명령은 Database01 이라는 데이터베이스를 서버 Server01에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="4150f-111">변수</span><span class="sxs-lookup"><span data-stu-id="4150f-111">PARAMETERS</span></span>

### <span data-ttu-id="4150f-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4150f-112">-DatabaseName</span></span>
<span data-ttu-id="4150f-113">이 cmdlet이 제거 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-113">Specifies the name of the database that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4150f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4150f-114">-DefaultProfile</span></span>
<span data-ttu-id="4150f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4150f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4150f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4150f-116">-Force</span></span>
<span data-ttu-id="4150f-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4150f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4150f-118">-ResourceGroupName</span></span>
<span data-ttu-id="4150f-119">데이터베이스가 할당 된 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="4150f-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4150f-120">-ServerName</span></span>
<span data-ttu-id="4150f-121">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="4150f-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4150f-122">-Confirm</span></span>
<span data-ttu-id="4150f-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4150f-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4150f-124">-WhatIf</span></span>
<span data-ttu-id="4150f-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4150f-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4150f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4150f-127">CommonParameters</span></span>
<span data-ttu-id="4150f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4150f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4150f-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4150f-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4150f-130">입력</span><span class="sxs-lookup"><span data-stu-id="4150f-130">INPUTS</span></span>

### <span data-ttu-id="4150f-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4150f-131">System.String</span></span>

## <span data-ttu-id="4150f-132">출력</span><span class="sxs-lookup"><span data-stu-id="4150f-132">OUTPUTS</span></span>

### <span data-ttu-id="4150f-133">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="4150f-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="4150f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="4150f-134">NOTES</span></span>

## <span data-ttu-id="4150f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4150f-135">RELATED LINKS</span></span>

[<span data-ttu-id="4150f-136">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-136">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="4150f-137">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-137">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="4150f-138">이력서-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-138">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="4150f-139">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-139">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="4150f-140">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="4150f-140">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="4150f-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="4150f-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


