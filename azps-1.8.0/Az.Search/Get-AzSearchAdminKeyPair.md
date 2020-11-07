---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: cd944184f4691b3f88934afc3a7bd9132eb23fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699281"
---
# <span data-ttu-id="006cb-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="006cb-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="006cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="006cb-102">SYNOPSIS</span></span>
<span data-ttu-id="006cb-103">Azure Search 서비스의 관리 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="006cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="006cb-104">SYNTAX</span></span>

### <span data-ttu-id="006cb-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="006cb-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="006cb-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="006cb-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="006cb-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="006cb-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="006cb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="006cb-108">DESCRIPTION</span></span>
<span data-ttu-id="006cb-109">**AzSearchAdminKeyPair** Cmdlet은 Azure Search 서비스의 관리자 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="006cb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="006cb-110">EXAMPLES</span></span>

### <span data-ttu-id="006cb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="006cb-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="006cb-112">이 예제에서는 Azure Search 서비스의 관리 키 쌍을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="006cb-113">변수</span><span class="sxs-lookup"><span data-stu-id="006cb-113">PARAMETERS</span></span>

### <span data-ttu-id="006cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006cb-114">-DefaultProfile</span></span>
<span data-ttu-id="006cb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="006cb-116">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="006cb-116">-ParentObject</span></span>
<span data-ttu-id="006cb-117">검색 서비스 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="006cb-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="006cb-118">-ParentResourceId</span></span>
<span data-ttu-id="006cb-119">검색 서비스 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="006cb-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006cb-120">-ResourceGroupName</span></span>
<span data-ttu-id="006cb-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-121">Resource Group name.</span></span>

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

### <span data-ttu-id="006cb-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="006cb-122">-ServiceName</span></span>
<span data-ttu-id="006cb-123">검색 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-123">Search Service name.</span></span>

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

### <span data-ttu-id="006cb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006cb-124">CommonParameters</span></span>
<span data-ttu-id="006cb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006cb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006cb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006cb-127">입력</span><span class="sxs-lookup"><span data-stu-id="006cb-127">INPUTS</span></span>

### <span data-ttu-id="006cb-128">Microsoft. Azure. PSSearchService를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="006cb-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="006cb-129">System.String</span></span>

## <span data-ttu-id="006cb-130">출력</span><span class="sxs-lookup"><span data-stu-id="006cb-130">OUTPUTS</span></span>

### <span data-ttu-id="006cb-131">. PSSearchAdminKey를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="006cb-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="006cb-132">상속자</span><span class="sxs-lookup"><span data-stu-id="006cb-132">NOTES</span></span>

## <span data-ttu-id="006cb-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="006cb-133">RELATED LINKS</span></span>

[<span data-ttu-id="006cb-134">새로운 AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="006cb-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)