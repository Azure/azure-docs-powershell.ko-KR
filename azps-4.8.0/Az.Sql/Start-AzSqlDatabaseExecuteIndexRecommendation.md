---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: e69cffe6955a5bf19636dd519c0906be64ce4413
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213847"
---
# <span data-ttu-id="bdcb1-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="bdcb1-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="bdcb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdcb1-102">SYNOPSIS</span></span>
<span data-ttu-id="bdcb1-103">추천 인덱스 작업을 실행 하는 워크플로를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="bdcb1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bdcb1-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdcb1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bdcb1-105">DESCRIPTION</span></span>
<span data-ttu-id="bdcb1-106">**AzSqlDatabaseExecuteIndexRecommendation** Cmdlet은 Azure SQL 데이터베이스에 대해 권장 되는 인덱스 작업을 실행 하는 워크플로를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="bdcb1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bdcb1-107">EXAMPLES</span></span>

### <span data-ttu-id="bdcb1-108">예제 1: 인덱스 권장 실행</span><span class="sxs-lookup"><span data-stu-id="bdcb1-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="bdcb1-109">이 명령은 index 권고안을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="bdcb1-110">변수</span><span class="sxs-lookup"><span data-stu-id="bdcb1-110">PARAMETERS</span></span>

### <span data-ttu-id="bdcb1-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="bdcb1-111">-DatabaseName</span></span>
<span data-ttu-id="bdcb1-112">이 cmdlet이 워크플로를 시작 하는 데이터베이스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="bdcb1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdcb1-113">-DefaultProfile</span></span>
<span data-ttu-id="bdcb1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bdcb1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bdcb1-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="bdcb1-115">-IndexRecommendationName</span></span>
<span data-ttu-id="bdcb1-116">이 cmdlet이 실행 하는 인덱스 권장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="bdcb1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdcb1-117">-ResourceGroupName</span></span>
<span data-ttu-id="bdcb1-118">서버가 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="bdcb1-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="bdcb1-119">-ServerName</span></span>
<span data-ttu-id="bdcb1-120">이 cmdlet이 워크플로를 시작 하는 데이터베이스를 호스팅하는 서버를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="bdcb1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdcb1-121">CommonParameters</span></span>
<span data-ttu-id="bdcb1-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdcb1-123">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bdcb1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdcb1-124">입력</span><span class="sxs-lookup"><span data-stu-id="bdcb1-124">INPUTS</span></span>

### <span data-ttu-id="bdcb1-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bdcb1-125">System.String</span></span>

## <span data-ttu-id="bdcb1-126">출력</span><span class="sxs-lookup"><span data-stu-id="bdcb1-126">OUTPUTS</span></span>

### <span data-ttu-id="bdcb1-127">Microsoft. Azure. i a m. 권장 사항</span><span class="sxs-lookup"><span data-stu-id="bdcb1-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="bdcb1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bdcb1-128">NOTES</span></span>

## <span data-ttu-id="bdcb1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bdcb1-129">RELATED LINKS</span></span>

[<span data-ttu-id="bdcb1-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="bdcb1-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="bdcb1-131">중지-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="bdcb1-131">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="bdcb1-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="bdcb1-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


