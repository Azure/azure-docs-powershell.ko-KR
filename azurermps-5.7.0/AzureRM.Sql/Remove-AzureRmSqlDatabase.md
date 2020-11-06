---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531592"
---
# <span data-ttu-id="fcda8-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="fcda8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcda8-102">SYNOPSIS</span></span>
<span data-ttu-id="fcda8-103">Azure SQL 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcda8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcda8-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcda8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fcda8-105">DESCRIPTION</span></span>
<span data-ttu-id="fcda8-106">**AzureRmSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="fcda8-107">이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="fcda8-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fcda8-108">EXAMPLES</span></span>

### <span data-ttu-id="fcda8-109">예제 1: Azure SQL server에서 데이터베이스 제거</span><span class="sxs-lookup"><span data-stu-id="fcda8-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="fcda8-110">이 명령은 Database01 이라는 데이터베이스를 서버 Server01에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="fcda8-111">변수</span><span class="sxs-lookup"><span data-stu-id="fcda8-111">PARAMETERS</span></span>

### <span data-ttu-id="fcda8-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fcda8-112">-DatabaseName</span></span>
<span data-ttu-id="fcda8-113">이 cmdlet이 제거 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcda8-114">-DefaultProfile</span></span>
<span data-ttu-id="fcda8-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fcda8-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="fcda8-116">-Force</span></span>
<span data-ttu-id="fcda8-117">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcda8-118">-ResourceGroupName</span></span>
<span data-ttu-id="fcda8-119">데이터베이스가 할당 된 Azure 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fcda8-120">-ServerName</span></span>
<span data-ttu-id="fcda8-121">데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-121">Specifies the name of the server that hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-122">-확인</span><span class="sxs-lookup"><span data-stu-id="fcda8-122">-Confirm</span></span>
<span data-ttu-id="fcda8-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcda8-124">-WhatIf</span></span>
<span data-ttu-id="fcda8-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcda8-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcda8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcda8-127">CommonParameters</span></span>
<span data-ttu-id="fcda8-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcda8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcda8-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcda8-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcda8-130">입력</span><span class="sxs-lookup"><span data-stu-id="fcda8-130">INPUTS</span></span>

### <span data-ttu-id="fcda8-131">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="fcda8-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fcda8-132">출력</span><span class="sxs-lookup"><span data-stu-id="fcda8-132">OUTPUTS</span></span>

### <span data-ttu-id="fcda8-133">AzureSqlDatabaseModel을 (를) 보세요.</span><span class="sxs-lookup"><span data-stu-id="fcda8-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="fcda8-134">상속자</span><span class="sxs-lookup"><span data-stu-id="fcda8-134">NOTES</span></span>

## <span data-ttu-id="fcda8-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcda8-135">RELATED LINKS</span></span>

[<span data-ttu-id="fcda8-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="fcda8-137">새로운 AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="fcda8-138">이력서-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="fcda8-139">Set-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="fcda8-140">일시 중단-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="fcda8-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="fcda8-141">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="fcda8-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


