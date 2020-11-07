---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 9b21c290b2d5e5b6056297bba7d4196dd68d68d2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873980"
---
# <span data-ttu-id="7a2f6-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7a2f6-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="7a2f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="7a2f6-103">추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="7a2f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a2f6-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a2f6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="7a2f6-106">**AzSqlDatabaseExecuteIndexRecommendation** cmdlet은 추천 인덱스 작업을 실행 하는 워크플로를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="7a2f6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7a2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="7a2f6-108">예제 1: 인덱스 권장 실행 중지</span><span class="sxs-lookup"><span data-stu-id="7a2f6-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="7a2f6-109">이 명령은 인덱스 권장 실행을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="7a2f6-110">변수</span><span class="sxs-lookup"><span data-stu-id="7a2f6-110">PARAMETERS</span></span>

### <span data-ttu-id="7a2f6-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="7a2f6-111">-DatabaseName</span></span>
<span data-ttu-id="7a2f6-112">이 cmdlet이 워크플로를 중지 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="7a2f6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a2f6-113">-DefaultProfile</span></span>
<span data-ttu-id="7a2f6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a2f6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a2f6-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="7a2f6-115">-IndexRecommendationName</span></span>
<span data-ttu-id="7a2f6-116">이 cmdlet이 중지 하는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="7a2f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a2f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="7a2f6-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="7a2f6-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="7a2f6-119">-ServerName</span></span>
<span data-ttu-id="7a2f6-120">이 cmdlet이 워크플로를 중지 하는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="7a2f6-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a2f6-121">CommonParameters</span></span>
<span data-ttu-id="7a2f6-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a2f6-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7a2f6-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a2f6-124">입력</span><span class="sxs-lookup"><span data-stu-id="7a2f6-124">INPUTS</span></span>

### <span data-ttu-id="7a2f6-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a2f6-125">System.String</span></span>

## <span data-ttu-id="7a2f6-126">출력</span><span class="sxs-lookup"><span data-stu-id="7a2f6-126">OUTPUTS</span></span>

### <span data-ttu-id="7a2f6-127">Microsoft. Azure. i a m. 권장 사항</span><span class="sxs-lookup"><span data-stu-id="7a2f6-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="7a2f6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7a2f6-128">NOTES</span></span>

## <span data-ttu-id="7a2f6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a2f6-129">RELATED LINKS</span></span>

[<span data-ttu-id="7a2f6-130">Get-AzSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="7a2f6-130">Get-AzSqlDatabaseIndexRecommendations</span></span>](./Get-AzSqlDatabaseIndexRecommendations.md)

[<span data-ttu-id="7a2f6-131">시작-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="7a2f6-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="7a2f6-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="7a2f6-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


