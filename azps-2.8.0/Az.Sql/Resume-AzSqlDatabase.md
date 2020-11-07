---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: c5f30388e1e3cb804aa0ef8d45e0afe34a1d2cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873555"
---
# <span data-ttu-id="cda85-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="cda85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cda85-102">SYNOPSIS</span></span>
<span data-ttu-id="cda85-103">SQL Data Warehouse 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cda85-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cda85-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cda85-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cda85-105">DESCRIPTION</span></span>
<span data-ttu-id="cda85-106">**이력서 AzSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cda85-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cda85-107">EXAMPLES</span></span>

### <span data-ttu-id="cda85-108">예제 1: Azure SQL Data Warehouse 데이터베이스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="cda85-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="cda85-109">이 명령은 일시 중단 된 Azure SQL 데이터 웨어하우스 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="cda85-110">변수</span><span class="sxs-lookup"><span data-stu-id="cda85-110">PARAMETERS</span></span>

### <span data-ttu-id="cda85-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cda85-111">-AsJob</span></span>
<span data-ttu-id="cda85-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cda85-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cda85-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="cda85-113">-DatabaseName</span></span>
<span data-ttu-id="cda85-114">이 cmdlet이 다시 시작 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="cda85-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cda85-115">-DefaultProfile</span></span>
<span data-ttu-id="cda85-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cda85-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cda85-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cda85-117">-ResourceGroupName</span></span>
<span data-ttu-id="cda85-118">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="cda85-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="cda85-119">-ServerName</span></span>
<span data-ttu-id="cda85-120">이 cmdlet이 다시 시작 하는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="cda85-121">-확인</span><span class="sxs-lookup"><span data-stu-id="cda85-121">-Confirm</span></span>
<span data-ttu-id="cda85-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cda85-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cda85-123">-WhatIf</span></span>
<span data-ttu-id="cda85-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cda85-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cda85-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cda85-126">CommonParameters</span></span>
<span data-ttu-id="cda85-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cda85-128">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cda85-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cda85-129">입력</span><span class="sxs-lookup"><span data-stu-id="cda85-129">INPUTS</span></span>

### <span data-ttu-id="cda85-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cda85-130">System.String</span></span>

## <span data-ttu-id="cda85-131">출력</span><span class="sxs-lookup"><span data-stu-id="cda85-131">OUTPUTS</span></span>

### <span data-ttu-id="cda85-132">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="cda85-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="cda85-133">상속자</span><span class="sxs-lookup"><span data-stu-id="cda85-133">NOTES</span></span>
* <span data-ttu-id="cda85-134">**이력서 AzSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="cda85-135">이 작업은 Azure SQL Database Basic, Standard 및 Premium edition에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cda85-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="cda85-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cda85-136">RELATED LINKS</span></span>

[<span data-ttu-id="cda85-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="cda85-138">새로운 AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="cda85-139">제거-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="cda85-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="cda85-141">일시 중단-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="cda85-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="cda85-142">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="cda85-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


