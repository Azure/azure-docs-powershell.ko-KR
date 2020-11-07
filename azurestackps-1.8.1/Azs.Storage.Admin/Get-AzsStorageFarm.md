---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd280133b3a0bc536c57f839fcc0faab81669c03
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875091"
---
# <span data-ttu-id="46508-101">Get-AzsStorageFarm</span><span class="sxs-lookup"><span data-stu-id="46508-101">Get-AzsStorageFarm</span></span>

## <span data-ttu-id="46508-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46508-102">SYNOPSIS</span></span>
<span data-ttu-id="46508-103">모든 저장소 팜의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46508-103">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="46508-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46508-104">SYNTAX</span></span>

### <span data-ttu-id="46508-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="46508-105">List (Default)</span></span>
```
Get-AzsStorageFarm [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="46508-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="46508-106">Get</span></span>
```
Get-AzsStorageFarm [-Name] <String> [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="46508-107">리소스</span><span class="sxs-lookup"><span data-stu-id="46508-107">ResourceId</span></span>
```
Get-AzsStorageFarm -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="46508-108">설명은</span><span class="sxs-lookup"><span data-stu-id="46508-108">DESCRIPTION</span></span>
<span data-ttu-id="46508-109">모든 저장소 팜의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46508-109">Returns a list of all storage farms.</span></span>

## <span data-ttu-id="46508-110">예제의</span><span class="sxs-lookup"><span data-stu-id="46508-110">EXAMPLES</span></span>

### <span data-ttu-id="46508-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="46508-111">EXAMPLE 1</span></span>
```
Get-AzsStorageFarm
```

<span data-ttu-id="46508-112">모든 저장소 팜의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46508-112">Get the list of all storage farms.</span></span>

## <span data-ttu-id="46508-113">변수</span><span class="sxs-lookup"><span data-stu-id="46508-113">PARAMETERS</span></span>

### <span data-ttu-id="46508-114">-이름</span><span class="sxs-lookup"><span data-stu-id="46508-114">-Name</span></span>
<span data-ttu-id="46508-115">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="46508-115">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46508-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46508-116">-ResourceGroupName</span></span>
<span data-ttu-id="46508-117">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46508-117">Resource group name.</span></span>

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

### <span data-ttu-id="46508-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="46508-118">-ResourceId</span></span>
<span data-ttu-id="46508-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="46508-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46508-120">-생략</span><span class="sxs-lookup"><span data-stu-id="46508-120">-Skip</span></span>
<span data-ttu-id="46508-121">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="46508-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="46508-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="46508-122">-Top</span></span>
<span data-ttu-id="46508-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46508-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="46508-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46508-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="46508-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46508-125">CommonParameters</span></span>
<span data-ttu-id="46508-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46508-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46508-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46508-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46508-128">입력</span><span class="sxs-lookup"><span data-stu-id="46508-128">INPUTS</span></span>

## <span data-ttu-id="46508-129">출력</span><span class="sxs-lookup"><span data-stu-id="46508-129">OUTPUTS</span></span>

### <span data-ttu-id="46508-130">Microsoft AzureStack. 관리. 팜</span><span class="sxs-lookup"><span data-stu-id="46508-130">Microsoft.AzureStack.Management.Storage.Admin.Models.Farm</span></span>

## <span data-ttu-id="46508-131">상속자</span><span class="sxs-lookup"><span data-stu-id="46508-131">NOTES</span></span>

## <span data-ttu-id="46508-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46508-132">RELATED LINKS</span></span>
