---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374963"
---
# <span data-ttu-id="c7206-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c7206-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="c7206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7206-102">SYNOPSIS</span></span>
<span data-ttu-id="c7206-103">서버 또는 데이터베이스에 대한 권장되는 인덱스 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="c7206-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7206-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7206-105">설명</span><span class="sxs-lookup"><span data-stu-id="c7206-105">DESCRIPTION</span></span>
<span data-ttu-id="c7206-106">**Get-AzSqlDatabaseIndexRecommendation** cmdlet은 Azure SQL 데이터베이스 서버 또는 데이터베이스에 대해 권장되는 인덱스 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="c7206-107">예제</span><span class="sxs-lookup"><span data-stu-id="c7206-107">EXAMPLES</span></span>

### <span data-ttu-id="c7206-108">예제 1: 서버의 모든 데이터베이스에 대한 인덱스 권장 사항 얻기</span><span class="sxs-lookup"><span data-stu-id="c7206-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c7206-109">이 명령은 server server01의 모든 데이터베이스에 대한 인덱스 권장 사항을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="c7206-110">예제 2: 특정 데이터베이스에 대한 인덱스 권장 사항 얻기</span><span class="sxs-lookup"><span data-stu-id="c7206-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="c7206-111">이 명령은 특정 데이터베이스에 대한 인덱스 권장 사항을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="c7206-112">예제 3: 이름에 의해 단일 인덱스 권장 사항 얻기</span><span class="sxs-lookup"><span data-stu-id="c7206-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="c7206-113">이 명령은 이름으로 단일 인덱스 권장을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="c7206-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7206-114">PARAMETERS</span></span>

### <span data-ttu-id="c7206-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c7206-115">-DatabaseName</span></span>
<span data-ttu-id="c7206-116">이 cmdlet이 인덱스 권장 사항을 얻을 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="c7206-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7206-117">-DefaultProfile</span></span>
<span data-ttu-id="c7206-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c7206-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7206-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="c7206-119">-IndexRecommendationName</span></span>
<span data-ttu-id="c7206-120">이 cmdlet에서 얻을 인덱스 권장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7206-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7206-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7206-122">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="c7206-123">이 cmdlet은 이 서버에서 호스트하는 데이터베이스에 대한 인덱스 권장 사항을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="c7206-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c7206-124">-ServerName</span></span>
<span data-ttu-id="c7206-125">이 cmdlet이 인덱스 권장 사항을 얻을 데이터베이스를 호스트하는 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="c7206-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="c7206-126">-TableName</span></span>
<span data-ttu-id="c7206-127">Azure SQL 테이블의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="c7206-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7206-128">-Confirm</span></span>
<span data-ttu-id="c7206-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7206-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7206-130">-WhatIf</span></span>
<span data-ttu-id="c7206-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7206-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7206-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7206-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7206-133">CommonParameters</span></span>
<span data-ttu-id="c7206-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7206-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7206-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7206-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7206-136">입력</span><span class="sxs-lookup"><span data-stu-id="c7206-136">INPUTS</span></span>

### <span data-ttu-id="c7206-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c7206-137">System.String</span></span>

## <span data-ttu-id="c7206-138">출력</span><span class="sxs-lookup"><span data-stu-id="c7206-138">OUTPUTS</span></span>

### <span data-ttu-id="c7206-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c7206-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="c7206-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7206-140">NOTES</span></span>

## <span data-ttu-id="c7206-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7206-141">RELATED LINKS</span></span>

[<span data-ttu-id="c7206-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c7206-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="c7206-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="c7206-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
