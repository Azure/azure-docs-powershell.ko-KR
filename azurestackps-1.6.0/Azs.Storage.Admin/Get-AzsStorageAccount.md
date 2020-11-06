---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: be2198103338a3df56f924e28b497095e21bf1de
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523579"
---
# <span data-ttu-id="49ce4-101">Get-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="49ce4-101">Get-AzsStorageAccount</span></span>

## <span data-ttu-id="49ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="49ce4-103">요청 된 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-103">Returns the requested storage account.</span></span>

## <span data-ttu-id="49ce4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="49ce4-104">SYNTAX</span></span>

### <span data-ttu-id="49ce4-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="49ce4-105">List (Default)</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-ResourceGroupName <String>] [-Summary] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="49ce4-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="49ce4-106">Get</span></span>
```
Get-AzsStorageAccount -FarmName <String> [-Name <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="49ce4-107">리소스</span><span class="sxs-lookup"><span data-stu-id="49ce4-107">ResourceId</span></span>
```
Get-AzsStorageAccount [-ResourceId <String>] [<CommonParameters>]
```

## <span data-ttu-id="49ce4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="49ce4-108">DESCRIPTION</span></span>
<span data-ttu-id="49ce4-109">요청 된 저장소 계정을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-109">Returns the requested storage account.</span></span>

## <span data-ttu-id="49ce4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="49ce4-110">EXAMPLES</span></span>

### <span data-ttu-id="49ce4-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="49ce4-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Summary
```

<span data-ttu-id="49ce4-112">저장소 계정 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-112">Get a list of storage accounts.</span></span>

### <span data-ttu-id="49ce4-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="49ce4-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsStorageAccount -FarmName 431e8245-9e38-43e9-bf73-5f9cb2fbbdb6 -Name f8f7ff7335cb4ba284fb855547e48f34
```

<span data-ttu-id="49ce4-114">지정 된 저장소 계정에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-114">Get details of the specified storage account.</span></span>

## <span data-ttu-id="49ce4-115">변수</span><span class="sxs-lookup"><span data-stu-id="49ce4-115">PARAMETERS</span></span>

### <span data-ttu-id="49ce4-116">-FarmName</span><span class="sxs-lookup"><span data-stu-id="49ce4-116">-FarmName</span></span>
<span data-ttu-id="49ce4-117">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-117">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-118">-이름</span><span class="sxs-lookup"><span data-stu-id="49ce4-118">-Name</span></span>
<span data-ttu-id="49ce4-119">테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-119">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49ce4-120">-ResourceGroupName</span></span>
<span data-ttu-id="49ce4-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-121">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49ce4-122">-ResourceId</span></span>
<span data-ttu-id="49ce4-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-123">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-124">-생략</span><span class="sxs-lookup"><span data-stu-id="49ce4-124">-Skip</span></span>
<span data-ttu-id="49ce4-125">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-125">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-126">-요약</span><span class="sxs-lookup"><span data-stu-id="49ce4-126">-Summary</span></span>
<span data-ttu-id="49ce4-127">Wheter 요약에 대 한 스위치 또는 자세한 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-127">Switch for wheter summary or detailed information is returned.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="49ce4-128">-Top</span></span>
<span data-ttu-id="49ce4-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="49ce4-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-130">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49ce4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49ce4-131">CommonParameters</span></span>
<span data-ttu-id="49ce4-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="49ce4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49ce4-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49ce4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49ce4-134">입력</span><span class="sxs-lookup"><span data-stu-id="49ce4-134">INPUTS</span></span>

## <span data-ttu-id="49ce4-135">출력</span><span class="sxs-lookup"><span data-stu-id="49ce4-135">OUTPUTS</span></span>

### <span data-ttu-id="49ce4-136">Microsoft AzureStack. 관리자. StorageAccount</span><span class="sxs-lookup"><span data-stu-id="49ce4-136">Microsoft.AzureStack.Management.Storage.Admin.Models.StorageAccount</span></span>

## <span data-ttu-id="49ce4-137">상속자</span><span class="sxs-lookup"><span data-stu-id="49ce4-137">NOTES</span></span>

## <span data-ttu-id="49ce4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49ce4-138">RELATED LINKS</span></span>
