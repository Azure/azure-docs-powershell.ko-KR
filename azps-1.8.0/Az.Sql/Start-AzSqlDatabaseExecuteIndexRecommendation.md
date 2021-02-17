---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 0EA0B131-A3D0-43CA-8517-9E724A11B04F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/start-azsqldatabaseexecuteindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Start-AzSqlDatabaseExecuteIndexRecommendation.md
ms.openlocfilehash: 1ab1e223ec173cf5727011956f52979026159594
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399518"
---
# <span data-ttu-id="03312-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="03312-101">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>

## <span data-ttu-id="03312-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03312-102">SYNOPSIS</span></span>
<span data-ttu-id="03312-103">권장되는 인덱스 작업을 실행하는 워크플로를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-103">Starts the workflow that runs a recommended index operation.</span></span>

## <span data-ttu-id="03312-104">구문</span><span class="sxs-lookup"><span data-stu-id="03312-104">SYNTAX</span></span>

```
Start-AzSqlDatabaseExecuteIndexRecommendation -ServerName <String> -DatabaseName <String>
 -IndexRecommendationName <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03312-105">설명</span><span class="sxs-lookup"><span data-stu-id="03312-105">DESCRIPTION</span></span>
<span data-ttu-id="03312-106">**Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet은 Azure SQL Database에 대한 권장 인덱스 작업을 실행하는 워크플로를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-106">The **Start-AzSqlDatabaseExecuteIndexRecommendation** cmdlet starts the workflow that runs a recommended index operation for an Azure SQL Database.</span></span>

## <span data-ttu-id="03312-107">예제</span><span class="sxs-lookup"><span data-stu-id="03312-107">EXAMPLES</span></span>

### <span data-ttu-id="03312-108">예제 1: 인덱스 권장 사항 실행</span><span class="sxs-lookup"><span data-stu-id="03312-108">Example 1: Run an index recommendation</span></span>
```
PS C:\>Start-AzSqlDatabaseExecuteIndexRecommendation -ResourceGroup "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="03312-109">이 명령은 인덱스 권장을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-109">This command runs an index recommendation.</span></span>

## <span data-ttu-id="03312-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03312-110">PARAMETERS</span></span>

### <span data-ttu-id="03312-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="03312-111">-DatabaseName</span></span>
<span data-ttu-id="03312-112">이 cmdlet이 워크플로를 시작하는 데이터베이스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-112">Specifies the name of the database for which this cmdlet starts the workflow.</span></span>

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

### <span data-ttu-id="03312-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03312-113">-DefaultProfile</span></span>
<span data-ttu-id="03312-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="03312-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03312-115">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="03312-115">-IndexRecommendationName</span></span>
<span data-ttu-id="03312-116">이 cmdlet이 실행되는 인덱스 권장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-116">Specifies the name of the index recommendation that this cmdlet runs.</span></span>

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

### <span data-ttu-id="03312-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03312-117">-ResourceGroupName</span></span>
<span data-ttu-id="03312-118">서버가 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="03312-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="03312-119">-ServerName</span></span>
<span data-ttu-id="03312-120">이 cmdlet이 워크플로를 시작하는 데이터베이스를 호스트하는 서버를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-120">Specifies the server that hosts the database for which this cmdlet starts a workflow.</span></span>

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

### <span data-ttu-id="03312-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03312-121">CommonParameters</span></span>
<span data-ttu-id="03312-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03312-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03312-123">자세한 내용은 [다음](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03312-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03312-124">입력</span><span class="sxs-lookup"><span data-stu-id="03312-124">INPUTS</span></span>

### <span data-ttu-id="03312-125">System.String</span><span class="sxs-lookup"><span data-stu-id="03312-125">System.String</span></span>

## <span data-ttu-id="03312-126">출력</span><span class="sxs-lookup"><span data-stu-id="03312-126">OUTPUTS</span></span>

### <span data-ttu-id="03312-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="03312-127">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="03312-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03312-128">NOTES</span></span>

## <span data-ttu-id="03312-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03312-129">RELATED LINKS</span></span>


[<span data-ttu-id="03312-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="03312-130">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="03312-131">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="03312-131">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


