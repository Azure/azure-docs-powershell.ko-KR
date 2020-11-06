---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/stop-azurermsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 2922edf4f7b7cfd0d814a5559bb1e6e7bb9ef3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529325"
---
# <span data-ttu-id="986c2-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="986c2-101">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="986c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="986c2-102">SYNOPSIS</span></span>
<span data-ttu-id="986c2-103">추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-103">Stops the workflow that runs a recommended index operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="986c2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="986c2-104">SYNTAX</span></span>

```
Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="986c2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="986c2-105">DESCRIPTION</span></span>
<span data-ttu-id="986c2-106">**AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet은 추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-106">The **Stop-AzureRmSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="986c2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="986c2-107">EXAMPLES</span></span>

### <span data-ttu-id="986c2-108">예제 1: 인덱스 권장 실행 중지</span><span class="sxs-lookup"><span data-stu-id="986c2-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzureRmSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="986c2-109">이 명령은 인덱스 권장 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="986c2-110">변수</span><span class="sxs-lookup"><span data-stu-id="986c2-110">PARAMETERS</span></span>

### <span data-ttu-id="986c2-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="986c2-111">-DatabaseName</span></span>
<span data-ttu-id="986c2-112">이 cmdlet이 워크플로를 중지 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="986c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986c2-113">-DefaultProfile</span></span>
<span data-ttu-id="986c2-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="986c2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="986c2-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="986c2-115">-IndexRecommendationName</span></span>
<span data-ttu-id="986c2-116">이 cmdlet이 중지 하는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="986c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="986c2-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="986c2-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="986c2-119">-ServerName</span></span>
<span data-ttu-id="986c2-120">이 cmdlet이 워크플로를 중지 하는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="986c2-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986c2-121">CommonParameters</span></span>
<span data-ttu-id="986c2-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="986c2-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986c2-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986c2-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986c2-124">입력</span><span class="sxs-lookup"><span data-stu-id="986c2-124">INPUTS</span></span>

### <span data-ttu-id="986c2-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="986c2-125">System.String</span></span>

## <span data-ttu-id="986c2-126">출력</span><span class="sxs-lookup"><span data-stu-id="986c2-126">OUTPUTS</span></span>

### <span data-ttu-id="986c2-127">Microsoft. Azure. i a m. 권장 사항</span><span class="sxs-lookup"><span data-stu-id="986c2-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="986c2-128">상속자</span><span class="sxs-lookup"><span data-stu-id="986c2-128">NOTES</span></span>

## <span data-ttu-id="986c2-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="986c2-129">RELATED LINKS</span></span>

[<span data-ttu-id="986c2-130">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="986c2-130">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>](./Get-AzureRmSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="986c2-131">시작-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="986c2-131">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="986c2-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="986c2-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


