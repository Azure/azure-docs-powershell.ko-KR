---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: b3b09e9027a578809fe68a90630331ad6ee35943
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536931"
---
# <span data-ttu-id="07f4a-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="07f4a-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="07f4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07f4a-102">SYNOPSIS</span></span>
<span data-ttu-id="07f4a-103">서버 또는 데이터베이스에 대해 권장 되는 인덱스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07f4a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07f4a-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f4a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07f4a-105">DESCRIPTION</span></span>
<span data-ttu-id="07f4a-106">**AzureRmSqlDatabaseIndexRecommendations** Cmdlet은 Azure SQL 데이터베이스 서버 또는 데이터베이스에 대해 권장 되는 인덱스 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="07f4a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07f4a-107">EXAMPLES</span></span>

### <span data-ttu-id="07f4a-108">예제 1: 서버의 모든 데이터베이스에 대 한 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f4a-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="07f4a-109">이 명령은 서버 server01의 모든 데이터베이스에 대 한 인덱스 권장 사항을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="07f4a-110">예제 2: 특정 데이터베이스에 대 한 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f4a-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="07f4a-111">이 명령은 특정 데이터베이스에 대 한 인덱스 권장 사항을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="07f4a-112">예제 3: 이름으로 단일 인덱스 권장 사항 가져오기</span><span class="sxs-lookup"><span data-stu-id="07f4a-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="07f4a-113">이 명령은 이름으로 단일 인덱스 권장 구성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="07f4a-114">변수</span><span class="sxs-lookup"><span data-stu-id="07f4a-114">PARAMETERS</span></span>

### <span data-ttu-id="07f4a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="07f4a-115">-DatabaseName</span></span>
<span data-ttu-id="07f4a-116">이 cmdlet에서 인덱스 권장 구성을 가져오는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="07f4a-117">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="07f4a-117">-IndexRecommendationName</span></span>
<span data-ttu-id="07f4a-118">이 cmdlet이 가져오는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-118">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="07f4a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f4a-119">-ResourceGroupName</span></span>
<span data-ttu-id="07f4a-120">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-120">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="07f4a-121">이 cmdlet은이 서버에서 호스팅하는 데이터베이스에 대 한 인덱스 권장 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-121">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="07f4a-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="07f4a-122">-ServerName</span></span>
<span data-ttu-id="07f4a-123">이 cmdlet에서 인덱스 권장 구성을 가져오는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-123">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="07f4a-124">-TableName</span><span class="sxs-lookup"><span data-stu-id="07f4a-124">-TableName</span></span>
<span data-ttu-id="07f4a-125">Azure SQL 테이블의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-125">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="07f4a-126">-확인</span><span class="sxs-lookup"><span data-stu-id="07f4a-126">-Confirm</span></span>
<span data-ttu-id="07f4a-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f4a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f4a-128">-WhatIf</span></span>
<span data-ttu-id="07f4a-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f4a-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f4a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f4a-131">-DefaultProfile</span></span>
<span data-ttu-id="07f4a-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07f4a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f4a-133">CommonParameters</span></span>
<span data-ttu-id="07f4a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07f4a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f4a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07f4a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f4a-136">입력</span><span class="sxs-lookup"><span data-stu-id="07f4a-136">INPUTS</span></span>

## <span data-ttu-id="07f4a-137">출력</span><span class="sxs-lookup"><span data-stu-id="07f4a-137">OUTPUTS</span></span>

## <span data-ttu-id="07f4a-138">상속자</span><span class="sxs-lookup"><span data-stu-id="07f4a-138">NOTES</span></span>

## <span data-ttu-id="07f4a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07f4a-139">RELATED LINKS</span></span>

[<span data-ttu-id="07f4a-140">시작-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="07f4a-140">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="07f4a-141">중지-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="07f4a-141">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
