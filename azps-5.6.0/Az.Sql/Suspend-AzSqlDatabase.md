---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 43284eb2f3d0cc39e5fcf5869ad26ebf0e52bd5a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992329"
---
# <span data-ttu-id="50a2a-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="50a2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50a2a-102">SYNOPSIS</span></span>
<span data-ttu-id="50a2a-103">데이터 SQL 데이터베이스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="50a2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="50a2a-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50a2a-105">설명</span><span class="sxs-lookup"><span data-stu-id="50a2a-105">DESCRIPTION</span></span>
<span data-ttu-id="50a2a-106">**suspend-AzSqlDatabase** cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스를 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="50a2a-107">예제</span><span class="sxs-lookup"><span data-stu-id="50a2a-107">EXAMPLES</span></span>

### <span data-ttu-id="50a2a-108">예제 1: Azure SQL 데이터 웨어하우스 데이터베이스 일시 중단</span><span class="sxs-lookup"><span data-stu-id="50a2a-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="50a2a-109">이 명령은 데이터 웨어하우스 데이터베이스의 활성 Azure SQL 일시 중단합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="50a2a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="50a2a-110">PARAMETERS</span></span>

### <span data-ttu-id="50a2a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="50a2a-111">-AsJob</span></span>
<span data-ttu-id="50a2a-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="50a2a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="50a2a-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="50a2a-113">-DatabaseName</span></span>
<span data-ttu-id="50a2a-114">이 cmdlet이 일시 중단하는 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="50a2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50a2a-115">-DefaultProfile</span></span>
<span data-ttu-id="50a2a-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="50a2a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50a2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50a2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="50a2a-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="50a2a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="50a2a-119">-ServerName</span></span>
<span data-ttu-id="50a2a-120">데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="50a2a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="50a2a-121">-Confirm</span></span>
<span data-ttu-id="50a2a-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50a2a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50a2a-123">-WhatIf</span></span>
<span data-ttu-id="50a2a-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50a2a-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50a2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50a2a-126">CommonParameters</span></span>
<span data-ttu-id="50a2a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50a2a-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50a2a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50a2a-129">입력</span><span class="sxs-lookup"><span data-stu-id="50a2a-129">INPUTS</span></span>

### <span data-ttu-id="50a2a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="50a2a-130">System.String</span></span>

## <span data-ttu-id="50a2a-131">출력</span><span class="sxs-lookup"><span data-stu-id="50a2a-131">OUTPUTS</span></span>

### <span data-ttu-id="50a2a-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="50a2a-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="50a2a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50a2a-133">NOTES</span></span>
* <span data-ttu-id="50a2a-134">**Suspend-AzSqlDatabase** cmdlet은 Azure SQL Data Warehouse 데이터베이스에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="50a2a-135">이 작업은 Azure 데이터베이스 기본, 표준 및 프리미엄 SQL 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50a2a-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="50a2a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50a2a-136">RELATED LINKS</span></span>

[<span data-ttu-id="50a2a-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="50a2a-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="50a2a-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="50a2a-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="50a2a-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="50a2a-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="50a2a-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="50a2a-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


