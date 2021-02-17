---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 4D2E0956-FBFA-43CC-ABE3-A6CBB9409263
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/stop-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Stop-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 7f13b1a1a5daad4e7c97de962943bb859f6a09df
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402187"
---
# <span data-ttu-id="39101-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="39101-101">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="39101-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39101-102">SYNOPSIS</span></span>
<span data-ttu-id="39101-103">권장되는 인덱스 작업을 실행하는 워크플로를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-103">Stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="39101-104">구문</span><span class="sxs-lookup"><span data-stu-id="39101-104">SYNTAX</span></span>

```
Stop-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="39101-105">설명</span><span class="sxs-lookup"><span data-stu-id="39101-105">DESCRIPTION</span></span>
<span data-ttu-id="39101-106">**Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet은 권장되는 인덱스 작업을 실행하는 워크플로를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-106">The **Stop-AzSqlDatabaseExecuteIndexRecommendation** cmdlet stops the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="39101-107">예제</span><span class="sxs-lookup"><span data-stu-id="39101-107">EXAMPLES</span></span>

### <span data-ttu-id="39101-108">예제 1: 인덱스 권장 사항 실행 중지</span><span class="sxs-lookup"><span data-stu-id="39101-108">Example 1: Stop running an index recommendation</span></span>
```
PS C:\>Stop-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="39101-109">이 명령은 인덱스 권장 실행을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-109">This command stops running an index recommendation.</span></span>

## <span data-ttu-id="39101-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="39101-110">PARAMETERS</span></span>

### <span data-ttu-id="39101-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="39101-111">-DatabaseName</span></span>
<span data-ttu-id="39101-112">이 cmdlet이 워크플로를 중지하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-112">Specifies the name of the database for which this cmdlet stops the workflow.</span></span>

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

### <span data-ttu-id="39101-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39101-113">-DefaultProfile</span></span>
<span data-ttu-id="39101-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="39101-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="39101-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="39101-115">-IndexRecommendationName</span></span>
<span data-ttu-id="39101-116">이 cmdlet이 중지하는 인덱스 권장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-116">Specifies the name of the index recommendation that this cmdlet stops.</span></span>

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

### <span data-ttu-id="39101-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39101-117">-ResourceGroupName</span></span>
<span data-ttu-id="39101-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="39101-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="39101-119">-ServerName</span></span>
<span data-ttu-id="39101-120">이 cmdlet이 워크플로를 중지하는 데이터베이스를 호스트하는 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-120">Specifies the server that hosts the database for which this cmdlet stops a workflow.</span></span>

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

### <span data-ttu-id="39101-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39101-121">CommonParameters</span></span>
<span data-ttu-id="39101-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="39101-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39101-123">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="39101-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39101-124">입력</span><span class="sxs-lookup"><span data-stu-id="39101-124">INPUTS</span></span>

### <span data-ttu-id="39101-125">System.String</span><span class="sxs-lookup"><span data-stu-id="39101-125">System.String</span></span>

## <span data-ttu-id="39101-126">출력</span><span class="sxs-lookup"><span data-stu-id="39101-126">OUTPUTS</span></span>

### <span data-ttu-id="39101-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="39101-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="39101-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="39101-128">NOTES</span></span>

## <span data-ttu-id="39101-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39101-129">RELATED LINKS</span></span>


[<span data-ttu-id="39101-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="39101-130">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="39101-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="39101-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


