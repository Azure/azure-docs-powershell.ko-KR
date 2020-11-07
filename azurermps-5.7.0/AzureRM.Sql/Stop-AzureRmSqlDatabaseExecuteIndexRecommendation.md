---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: d4cb344f63b871f55668c4de7205ada80ff04f35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703207"
---
# <span data-ttu-id="2457d-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2457d-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="2457d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2457d-102">SYNOPSIS</span></span>
<span data-ttu-id="2457d-103">추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2457d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2457d-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2457d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2457d-105">DESCRIPTION</span></span>
<span data-ttu-id="2457d-106">**AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet은 추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="2457d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2457d-107">EXAMPLES</span></span>

### <span data-ttu-id="2457d-108">예제 1: 인덱스 권장 실행 중지</span><span class="sxs-lookup"><span data-stu-id="2457d-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="2457d-109">이 명령은 인덱스 권장 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="2457d-110">변수</span><span class="sxs-lookup"><span data-stu-id="2457d-110">PARAMETERS</span></span>

### <span data-ttu-id="2457d-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="2457d-111">-DatabaseName</span></span>
<span data-ttu-id="2457d-112">이 cmdlet이 워크플로를 중지 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2457d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2457d-113">-DefaultProfile</span></span>
<span data-ttu-id="2457d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2457d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2457d-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="2457d-115">-IndexRecommendationName</span></span>
<span data-ttu-id="2457d-116">이 cmdlet이 중지 하는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2457d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2457d-117">-ResourceGroupName</span></span>
<span data-ttu-id="2457d-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="2457d-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2457d-119">-ServerName</span></span>
<span data-ttu-id="2457d-120">이 cmdlet이 워크플로를 중지 하는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2457d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2457d-121">CommonParameters</span></span>
<span data-ttu-id="2457d-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2457d-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2457d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2457d-124">입력</span><span class="sxs-lookup"><span data-stu-id="2457d-124">INPUTS</span></span>

### <span data-ttu-id="2457d-125">않아야</span><span class="sxs-lookup"><span data-stu-id="2457d-125">None</span></span>
<span data-ttu-id="2457d-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2457d-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2457d-127">출력</span><span class="sxs-lookup"><span data-stu-id="2457d-127">OUTPUTS</span></span>

## <span data-ttu-id="2457d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="2457d-128">NOTES</span></span>

## <span data-ttu-id="2457d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2457d-129">RELATED LINKS</span></span>

[<span data-ttu-id="2457d-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="2457d-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="2457d-131">시작-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="2457d-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="2457d-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="2457d-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


