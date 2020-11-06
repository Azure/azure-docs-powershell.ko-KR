---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537804"
---
# <span data-ttu-id="f626a-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="f626a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f626a-102">SYNOPSIS</span></span>
<span data-ttu-id="f626a-103">SQL Data Warehouse 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f626a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f626a-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f626a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f626a-105">DESCRIPTION</span></span>
<span data-ttu-id="f626a-106">**이력서 AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f626a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f626a-107">EXAMPLES</span></span>

### <span data-ttu-id="f626a-108">예제 1: Azure SQL Data Warehouse 데이터베이스 다시 시작</span><span class="sxs-lookup"><span data-stu-id="f626a-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="f626a-109">이 명령은 일시 중단 된 Azure SQL 데이터 웨어하우스 데이터베이스를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="f626a-110">변수</span><span class="sxs-lookup"><span data-stu-id="f626a-110">PARAMETERS</span></span>

### <span data-ttu-id="f626a-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f626a-111">-DatabaseName</span></span>
<span data-ttu-id="f626a-112">이 cmdlet이 다시 시작 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="f626a-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f626a-113">-ResourceGroupName</span></span>
<span data-ttu-id="f626a-114">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="f626a-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f626a-115">-ServerName</span></span>
<span data-ttu-id="f626a-116">이 cmdlet이 다시 시작 하는 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="f626a-117">-확인</span><span class="sxs-lookup"><span data-stu-id="f626a-117">-Confirm</span></span>
<span data-ttu-id="f626a-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f626a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f626a-119">-WhatIf</span></span>
<span data-ttu-id="f626a-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f626a-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f626a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f626a-122">-DefaultProfile</span></span>
<span data-ttu-id="f626a-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f626a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f626a-124">CommonParameters</span></span>
<span data-ttu-id="f626a-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f626a-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f626a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f626a-127">입력</span><span class="sxs-lookup"><span data-stu-id="f626a-127">INPUTS</span></span>

### <span data-ttu-id="f626a-128">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="f626a-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f626a-129">출력</span><span class="sxs-lookup"><span data-stu-id="f626a-129">OUTPUTS</span></span>

### <span data-ttu-id="f626a-130">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="f626a-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="f626a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="f626a-131">NOTES</span></span>
* <span data-ttu-id="f626a-132">**이력서 AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터 웨어하우스 데이터베이스 에서만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="f626a-133">이 작업은 Azure SQL Database Basic, Standard 및 Premium edition에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f626a-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="f626a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f626a-134">RELATED LINKS</span></span>

[<span data-ttu-id="f626a-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="f626a-136">새로운 AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="f626a-137">제거-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="f626a-138">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="f626a-139">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="f626a-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="f626a-140">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="f626a-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


