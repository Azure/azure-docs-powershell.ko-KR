---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B5C909D7-6087-463A-83BF-99DD196B9862
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseactivity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseActivity.md
ms.openlocfilehash: 91c23a32fd25c184e46249424b439375caed6ac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699051"
---
# <span data-ttu-id="d46aa-101">Get-AzSqlDatabaseActivity</span><span class="sxs-lookup"><span data-stu-id="d46aa-101">Get-AzSqlDatabaseActivity</span></span>

## <span data-ttu-id="d46aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d46aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d46aa-103">데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-103">Gets the status of database operations.</span></span>

## <span data-ttu-id="d46aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d46aa-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseActivity [-ServerName] <String> [-ElasticPoolName <String>] -DatabaseName <String>
 [-OperationId <Guid>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d46aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d46aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d46aa-106">**AzSqlDatabaseActivity** Cmdlet은 Azure SQL 데이터베이스에서 데이터베이스 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-106">The **Get-AzSqlDatabaseActivity** cmdlet gets the status of database operations in Azure SQL Database.</span></span>

## <span data-ttu-id="d46aa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d46aa-107">EXAMPLES</span></span>

### <span data-ttu-id="d46aa-108">예제 1: 모든 SQL 데이터베이스 인스턴스의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="d46aa-108">Example 1: Get status for all SQL Database instances</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01"
```

<span data-ttu-id="d46aa-109">이 명령은 ElasticPool01 이라는 탄력적 풀에 있는 모든 SQL 데이터베이스 인스턴스의 작업 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-109">This command returns the operation status of all SQL Database instances in an elastic pool named ElasticPool01.</span></span>

### <span data-ttu-id="d46aa-110">예제 2: 모든 SQL 데이터베이스 작업의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="d46aa-110">Example 2: Get status for all SQL Database operations</span></span>
```
PS C:\>Get-AzSqlDatabaseActivity -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d46aa-111">이 명령은 데이터베이스에서 모든 SQL 데이터베이스 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-111">This command returns the status of all SQL Database operations in a database.</span></span>

## <span data-ttu-id="d46aa-112">변수</span><span class="sxs-lookup"><span data-stu-id="d46aa-112">PARAMETERS</span></span>

### <span data-ttu-id="d46aa-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d46aa-113">-DatabaseName</span></span>
<span data-ttu-id="d46aa-114">이 cmdlet이 상태를 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-114">Specifies the name of the database for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="d46aa-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46aa-115">-DefaultProfile</span></span>
<span data-ttu-id="d46aa-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d46aa-117">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d46aa-117">-ElasticPoolName</span></span>
<span data-ttu-id="d46aa-118">이 cmdlet이 상태를 가져오는 탄력적 데이터베이스 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-118">Specifies the name of the elastic database pool for which this cmdlet gets status.</span></span>

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

### <span data-ttu-id="d46aa-119">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d46aa-119">-OperationId</span></span>
<span data-ttu-id="d46aa-120">이 cmdlet이 가져오는 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-120">Specifies the ID of the operation that this cmdlet gets.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="d46aa-122">데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-122">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d46aa-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d46aa-123">-ServerName</span></span>
<span data-ttu-id="d46aa-124">데이터베이스를 호스트 하는 Microsoft SQL Server의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-124">Specifies the name of the Microsoft SQL Server that hosts the database.</span></span>

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

### <span data-ttu-id="d46aa-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d46aa-125">-Confirm</span></span>
<span data-ttu-id="d46aa-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46aa-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46aa-127">-WhatIf</span></span>
<span data-ttu-id="d46aa-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46aa-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46aa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46aa-130">CommonParameters</span></span>
<span data-ttu-id="d46aa-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d46aa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46aa-132">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d46aa-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46aa-133">입력</span><span class="sxs-lookup"><span data-stu-id="d46aa-133">INPUTS</span></span>

### <span data-ttu-id="d46aa-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d46aa-134">System.String</span></span>

### <span data-ttu-id="d46aa-135">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d46aa-135">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d46aa-136">출력</span><span class="sxs-lookup"><span data-stu-id="d46aa-136">OUTPUTS</span></span>

### <span data-ttu-id="d46aa-137">AzureSqlDatabaseActivityModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="d46aa-137">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseActivityModel</span></span>

## <span data-ttu-id="d46aa-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d46aa-138">NOTES</span></span>

## <span data-ttu-id="d46aa-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d46aa-139">RELATED LINKS</span></span>
