---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 4882ada2348a8b878cfaab04a85ac50ae58d9daf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008448"
---
# <span data-ttu-id="36e66-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="36e66-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="36e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36e66-102">SYNOPSIS</span></span>
<span data-ttu-id="36e66-103">권장 인덱스 작업을 실행하는 워크플로를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="36e66-104">구문</span><span class="sxs-lookup"><span data-stu-id="36e66-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36e66-105">설명</span><span class="sxs-lookup"><span data-stu-id="36e66-105">DESCRIPTION</span></span>
<span data-ttu-id="36e66-106">**Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet은 권장 인덱스 작업을 실행하는 워크플로를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="36e66-107">예제</span><span class="sxs-lookup"><span data-stu-id="36e66-107">EXAMPLES</span></span>

### <span data-ttu-id="36e66-108">예제 1: 인덱스 권장 사항 실행 중지</span><span class="sxs-lookup"><span data-stu-id="36e66-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="36e66-109">이 명령은 인덱스 권장 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="36e66-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="36e66-110">PARAMETERS</span></span>

### <span data-ttu-id="36e66-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="36e66-111">-DatabaseName</span></span>
<span data-ttu-id="36e66-112">이 cmdlet이 워크플로를 중지하는 데이터베이스 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="36e66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e66-113">-DefaultProfile</span></span>
<span data-ttu-id="36e66-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="36e66-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36e66-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="36e66-115">-IndexRecommendationName</span></span>
<span data-ttu-id="36e66-116">이 cmdlet이 중지하는 인덱스 권장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="36e66-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36e66-117">-ResourceGroupName</span></span>
<span data-ttu-id="36e66-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="36e66-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="36e66-119">-ServerName</span></span>
<span data-ttu-id="36e66-120">이 cmdlet이 워크플로를 중지하는 데이터베이스를 호스트하는 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="36e66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e66-121">CommonParameters</span></span>
<span data-ttu-id="36e66-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="36e66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e66-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e66-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e66-124">입력</span><span class="sxs-lookup"><span data-stu-id="36e66-124">INPUTS</span></span>

### <span data-ttu-id="36e66-125">System.String</span><span class="sxs-lookup"><span data-stu-id="36e66-125">System.String</span></span>

## <span data-ttu-id="36e66-126">출력</span><span class="sxs-lookup"><span data-stu-id="36e66-126">OUTPUTS</span></span>

### <span data-ttu-id="36e66-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="36e66-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="36e66-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="36e66-128">NOTES</span></span>

## <span data-ttu-id="36e66-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36e66-129">RELATED LINKS</span></span>

[<span data-ttu-id="36e66-130">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="36e66-130">Get-AzSqlDatabaseIndexRecommendation</span></span>](./Get-AzSqlDatabaseIndexRecommendation.md)

[<span data-ttu-id="36e66-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="36e66-131">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="36e66-132">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="36e66-132">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


