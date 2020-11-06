---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: A333A60D-CA76-4E4E-9C8B-72AAEF464F0A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsSavedSearch.md
ms.openlocfilehash: ebea93e7d59e0740aa21e909f35779857aacba01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527352"
---
# <span data-ttu-id="83aa6-101">Set-AzureRmOperationalInsightsSavedSearch</span><span class="sxs-lookup"><span data-stu-id="83aa6-101">Set-AzureRmOperationalInsightsSavedSearch</span></span>

## <span data-ttu-id="83aa6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83aa6-102">SYNOPSIS</span></span>
<span data-ttu-id="83aa6-103">이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-103">Updates a saved search that already exists.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="83aa6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="83aa6-104">SYNTAX</span></span>

```
Set-AzureRmOperationalInsightsSavedSearch [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-SavedSearchId] <String> [-DisplayName] <String> [-Category] <String> [-Query] <String> [[-Tags] <Hashtable>]
 [[-Version] <Int64>] [[-ETag] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83aa6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="83aa6-105">DESCRIPTION</span></span>
<span data-ttu-id="83aa6-106">**Set-AzureRmOperationalInsightsSavedSearch** cmdlet은 이미 존재 하는 저장 된 검색을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-106">The **Set-AzureRmOperationalInsightsSavedSearch** cmdlet updates a saved search that already exists.</span></span>

## <span data-ttu-id="83aa6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="83aa6-107">EXAMPLES</span></span>

### <span data-ttu-id="83aa6-108">예제 1: 업데이트 된 속성을 사용 하 여 저장 된 검색 설정</span><span class="sxs-lookup"><span data-stu-id="83aa6-108">Example 1: Sets a saved search with updated properties</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsSavedSearch -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace" -SavedSearchId "ContosoSavedSearchId" -DisplayName "ContosoSavedSearchDisplayName" -Category "ContosoSavedSearchCategory" -Query "Type=Event" -Version $Version -ETag "ContosoSavedSearchEtag"
```

<span data-ttu-id="83aa6-109">이 명령은 업데이트 된 속성을 사용 하 여 저장 한 검색을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-109">This command sets a saved search with updated properties.</span></span>

## <span data-ttu-id="83aa6-110">변수</span><span class="sxs-lookup"><span data-stu-id="83aa6-110">PARAMETERS</span></span>

### <span data-ttu-id="83aa6-111">-범주</span><span class="sxs-lookup"><span data-stu-id="83aa6-111">-Category</span></span>
<span data-ttu-id="83aa6-112">범주 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-112">Specifies the category name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-113">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="83aa6-113">-DisplayName</span></span>
<span data-ttu-id="83aa6-114">표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-114">Specifies the display name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-115">-ETag</span><span class="sxs-lookup"><span data-stu-id="83aa6-115">-ETag</span></span>
<span data-ttu-id="83aa6-116">ETag 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-116">Specifies the ETag name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-117">-쿼리</span><span class="sxs-lookup"><span data-stu-id="83aa6-117">-Query</span></span>
<span data-ttu-id="83aa6-118">쿼리 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-118">Specifies the query name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83aa6-119">-ResourceGroupName</span></span>
<span data-ttu-id="83aa6-120">리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-120">Specifies the resource group name.</span></span>

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

### <span data-ttu-id="83aa6-121">-SavedSearchId</span><span class="sxs-lookup"><span data-stu-id="83aa6-121">-SavedSearchId</span></span>
<span data-ttu-id="83aa6-122">저장 된 검색 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-122">Specifies the saved search ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-123">태그</span><span class="sxs-lookup"><span data-stu-id="83aa6-123">-Tags</span></span>
```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-124">-버전</span><span class="sxs-lookup"><span data-stu-id="83aa6-124">-Version</span></span>
```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="83aa6-125">-WorkspaceName</span></span>
<span data-ttu-id="83aa6-126">작업 영역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-126">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83aa6-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83aa6-127">-DefaultProfile</span></span>
<span data-ttu-id="83aa6-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83aa6-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83aa6-129">CommonParameters</span></span>
<span data-ttu-id="83aa6-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="83aa6-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83aa6-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="83aa6-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83aa6-132">입력</span><span class="sxs-lookup"><span data-stu-id="83aa6-132">INPUTS</span></span>

## <span data-ttu-id="83aa6-133">출력</span><span class="sxs-lookup"><span data-stu-id="83aa6-133">OUTPUTS</span></span>

## <span data-ttu-id="83aa6-134">상속자</span><span class="sxs-lookup"><span data-stu-id="83aa6-134">NOTES</span></span>

## <span data-ttu-id="83aa6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83aa6-135">RELATED LINKS</span></span>

[<span data-ttu-id="83aa6-136">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="83aa6-136">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


