---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/start-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: c61f1bd988410b696eddd12162958333022dd892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529335"
---
# <span data-ttu-id="4634c-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4634c-101">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="4634c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4634c-102">SYNOPSIS</span></span>
<span data-ttu-id="4634c-103">추천 인덱스 작업을 실행 하는 워크플로를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-103">Starts the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4634c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4634c-104">SYNTAX</span></span>

```
Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4634c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4634c-105">DESCRIPTION</span></span>
<span data-ttu-id="4634c-106">**AzureRmSqlDatabaseExecuteIndexRecommendation** Cmdlet은 Azure SQL 데이터베이스에 대해 권장 되는 인덱스 작업을 실행 하는 워크플로를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-106">The **Start-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="4634c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4634c-107">EXAMPLES</span></span>

### <span data-ttu-id="4634c-108">예제 1: 인덱스 권장 실행</span><span class="sxs-lookup"><span data-stu-id="4634c-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="4634c-109">이 명령은 index 권고안을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="4634c-110">변수</span><span class="sxs-lookup"><span data-stu-id="4634c-110">PARAMETERS</span></span>

### <span data-ttu-id="4634c-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4634c-111">-DatabaseName</span></span>
<span data-ttu-id="4634c-112">이 cmdlet이 워크플로를 시작 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="4634c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4634c-113">-DefaultProfile</span></span>
<span data-ttu-id="4634c-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4634c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4634c-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="4634c-115">-IndexRecommendationName</span></span>
<span data-ttu-id="4634c-116">이 cmdlet이 실행 하는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="4634c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4634c-117">-ResourceGroupName</span></span>
<span data-ttu-id="4634c-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="4634c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4634c-119">-ServerName</span></span>
<span data-ttu-id="4634c-120">이 cmdlet이 워크플로를 시작 하는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="4634c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4634c-121">CommonParameters</span></span>
<span data-ttu-id="4634c-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4634c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4634c-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4634c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4634c-124">입력</span><span class="sxs-lookup"><span data-stu-id="4634c-124">INPUTS</span></span>

### <span data-ttu-id="4634c-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4634c-125">System.String</span></span>

## <span data-ttu-id="4634c-126">출력</span><span class="sxs-lookup"><span data-stu-id="4634c-126">OUTPUTS</span></span>

### <span data-ttu-id="4634c-127">Microsoft. Azure. i a m. 권장 사항</span><span class="sxs-lookup"><span data-stu-id="4634c-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="4634c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4634c-128">NOTES</span></span>

## <span data-ttu-id="4634c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4634c-129">RELATED LINKS</span></span>

[<span data-ttu-id="4634c-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="4634c-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="4634c-131">중지-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4634c-131">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="4634c-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="4634c-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


