---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047571"
---
# <span data-ttu-id="8f529-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8f529-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="8f529-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f529-102">SYNOPSIS</span></span>
<span data-ttu-id="8f529-103">서버 또는 데이터베이스에 대해 권장 되는 인덱스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="8f529-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f529-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f529-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8f529-105">DESCRIPTION</span></span>
<span data-ttu-id="8f529-106">**AzSqlDatabaseIndexRecommendation** Cmdlet은 Azure SQL 데이터베이스 서버 또는 데이터베이스에 대해 권장 되는 인덱스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="8f529-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8f529-107">EXAMPLES</span></span>

### <span data-ttu-id="8f529-108">예제 1: 서버의 모든 데이터베이스에 대 한 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="8f529-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="8f529-109">이 명령은 서버 server01의 모든 데이터베이스에 대 한 인덱스 권장 사항을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="8f529-110">예제 2: 특정 데이터베이스에 대 한 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="8f529-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8f529-111">이 명령은 특정 데이터베이스에 대 한 인덱스 권장 사항을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="8f529-112">예제 3: 이름으로 단일 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="8f529-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="8f529-113">이 명령은 이름으로 단일 인덱스 권장 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="8f529-114">변수</span><span class="sxs-lookup"><span data-stu-id="8f529-114">PARAMETERS</span></span>

### <span data-ttu-id="8f529-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f529-115">-DatabaseName</span></span>
<span data-ttu-id="8f529-116">이 cmdlet에서 인덱스 권장 구성을 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="8f529-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f529-117">-DefaultProfile</span></span>
<span data-ttu-id="8f529-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8f529-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f529-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="8f529-119">-IndexRecommendationName</span></span>
<span data-ttu-id="8f529-120">이 cmdlet이 가져오는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="8f529-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f529-121">-ResourceGroupName</span></span>
<span data-ttu-id="8f529-122">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="8f529-123">이 cmdlet은이 서버에서 호스팅하는 데이터베이스에 대 한 인덱스 권장 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="8f529-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8f529-124">-ServerName</span></span>
<span data-ttu-id="8f529-125">이 cmdlet에서 인덱스 권장 구성을 가져오는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="8f529-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="8f529-126">-TableName</span></span>
<span data-ttu-id="8f529-127">Azure SQL 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="8f529-128">-확인</span><span class="sxs-lookup"><span data-stu-id="8f529-128">-Confirm</span></span>
<span data-ttu-id="8f529-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f529-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f529-130">-WhatIf</span></span>
<span data-ttu-id="8f529-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f529-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f529-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f529-133">CommonParameters</span></span>
<span data-ttu-id="8f529-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f529-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f529-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8f529-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f529-136">입력</span><span class="sxs-lookup"><span data-stu-id="8f529-136">INPUTS</span></span>

### <span data-ttu-id="8f529-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f529-137">System.String</span></span>

## <span data-ttu-id="8f529-138">출력</span><span class="sxs-lookup"><span data-stu-id="8f529-138">OUTPUTS</span></span>

### <span data-ttu-id="8f529-139">Microsoft. Azure. i a m. 권장 사항</span><span class="sxs-lookup"><span data-stu-id="8f529-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="8f529-140">상속자</span><span class="sxs-lookup"><span data-stu-id="8f529-140">NOTES</span></span>

## <span data-ttu-id="8f529-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f529-141">RELATED LINKS</span></span>

[<span data-ttu-id="8f529-142">시작-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8f529-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="8f529-143">중지-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="8f529-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
