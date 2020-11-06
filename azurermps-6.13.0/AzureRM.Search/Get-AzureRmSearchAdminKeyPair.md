---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchAdminKeyPair.md
ms.openlocfilehash: 92b2e7304c0f837e47f7464e84769478902c973a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531949"
---
# <span data-ttu-id="f0d1f-101">Get-AzureRmSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="f0d1f-101">Get-AzureRmSearchAdminKeyPair</span></span>

## <span data-ttu-id="f0d1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0d1f-102">SYNOPSIS</span></span>
<span data-ttu-id="f0d1f-103">Azure Search 서비스의 관리 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-103">Gets admin key pair of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f0d1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0d1f-104">SYNTAX</span></span>

### <span data-ttu-id="f0d1f-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0d1f-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0d1f-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d1f-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0d1f-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0d1f-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0d1f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f0d1f-108">DESCRIPTION</span></span>
<span data-ttu-id="f0d1f-109">**AzureRmSearchAdminKeyPair** Cmdlet은 Azure Search 서비스의 관리자 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-109">The **Get-AzureRmSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="f0d1f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f0d1f-110">EXAMPLES</span></span>

### <span data-ttu-id="f0d1f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0d1f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="f0d1f-112">이 예제에서는 Azure Search 서비스의 관리 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="f0d1f-113">변수</span><span class="sxs-lookup"><span data-stu-id="f0d1f-113">PARAMETERS</span></span>

### <span data-ttu-id="f0d1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0d1f-114">-DefaultProfile</span></span>
<span data-ttu-id="f0d1f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0d1f-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f0d1f-116">-ParentObject</span></span>
<span data-ttu-id="f0d1f-117">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-117">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d1f-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="f0d1f-118">-ParentResourceId</span></span>
<span data-ttu-id="f0d1f-119">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-119">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0d1f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0d1f-120">-ResourceGroupName</span></span>
<span data-ttu-id="f0d1f-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-121">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d1f-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f0d1f-122">-ServiceName</span></span>
<span data-ttu-id="f0d1f-123">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0d1f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0d1f-124">CommonParameters</span></span>
<span data-ttu-id="f0d1f-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0d1f-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0d1f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0d1f-127">입력</span><span class="sxs-lookup"><span data-stu-id="f0d1f-127">INPUTS</span></span>

### <span data-ttu-id="f0d1f-128">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="f0d1f-129">매개 변수: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f0d1f-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="f0d1f-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0d1f-130">System.String</span></span>

## <span data-ttu-id="f0d1f-131">출력</span><span class="sxs-lookup"><span data-stu-id="f0d1f-131">OUTPUTS</span></span>

### <span data-ttu-id="f0d1f-132">. PSSearchAdminKey를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0d1f-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="f0d1f-133">상속자</span><span class="sxs-lookup"><span data-stu-id="f0d1f-133">NOTES</span></span>

## <span data-ttu-id="f0d1f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0d1f-134">RELATED LINKS</span></span>

[<span data-ttu-id="f0d1f-135">새로운 AzureRmSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="f0d1f-135">New-AzureRmSearchAdminKey</span></span>](./New-AzureRmSearchAdminKey.md)
