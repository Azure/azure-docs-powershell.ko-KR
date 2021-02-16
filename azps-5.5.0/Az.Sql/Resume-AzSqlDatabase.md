---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201409"
---
# <span data-ttu-id="1b9a6-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="1b9a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b9a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9a6-103">데이터 웨어하우스 SQL 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="1b9a6-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b9a6-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b9a6-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b9a6-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9a6-106">**Resume-AzSqlDatabase** cmdlet은 Azure SQL Data Warehouse 데이터베이스를 다시 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="1b9a6-107">예제</span><span class="sxs-lookup"><span data-stu-id="1b9a6-107">EXAMPLES</span></span>

### <span data-ttu-id="1b9a6-108">예제 1: Azure SQL Data Warehouse 데이터베이스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="1b9a6-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="1b9a6-109">이 명령은 일시 중단된 Azure SQL Data Warehouse 데이터베이스를 다시 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="1b9a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b9a6-110">PARAMETERS</span></span>

### <span data-ttu-id="1b9a6-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b9a6-111">-AsJob</span></span>
<span data-ttu-id="1b9a6-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1b9a6-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1b9a6-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b9a6-113">-DatabaseName</span></span>
<span data-ttu-id="1b9a6-114">이 cmdlet이 다시 시작되는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="1b9a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9a6-115">-DefaultProfile</span></span>
<span data-ttu-id="1b9a6-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1b9a6-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b9a6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b9a6-117">-ResourceGroupName</span></span>
<span data-ttu-id="1b9a6-118">데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="1b9a6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1b9a6-119">-ServerName</span></span>
<span data-ttu-id="1b9a6-120">이 cmdlet이 다시 시작하는 데이터베이스를 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="1b9a6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b9a6-121">-Confirm</span></span>
<span data-ttu-id="1b9a6-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b9a6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9a6-123">-WhatIf</span></span>
<span data-ttu-id="1b9a6-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1b9a6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b9a6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b9a6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9a6-126">CommonParameters</span></span>
<span data-ttu-id="1b9a6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9a6-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9a6-129">입력</span><span class="sxs-lookup"><span data-stu-id="1b9a6-129">INPUTS</span></span>

### <span data-ttu-id="1b9a6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1b9a6-130">System.String</span></span>

## <span data-ttu-id="1b9a6-131">출력</span><span class="sxs-lookup"><span data-stu-id="1b9a6-131">OUTPUTS</span></span>

### <span data-ttu-id="1b9a6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="1b9a6-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="1b9a6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b9a6-133">NOTES</span></span>
* <span data-ttu-id="1b9a6-134">**Resume-AzSqlDatabase** cmdlet은 Azure SQL Data Warehouse 데이터베이스에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="1b9a6-135">이 작업은 Azure SQL Database Basic, Standard 및 Premium 버전에서 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b9a6-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="1b9a6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b9a6-136">RELATED LINKS</span></span>

[<span data-ttu-id="1b9a6-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="1b9a6-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="1b9a6-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="1b9a6-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="1b9a6-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="1b9a6-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="1b9a6-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="1b9a6-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


