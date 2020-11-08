---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4e39a2d9e314a29eaf273e4ef20e71d96293f1f7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046961"
---
# <span data-ttu-id="f648c-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="f648c-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="f648c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f648c-102">SYNOPSIS</span></span>
<span data-ttu-id="f648c-103">특정 위치에 있는 모든 패브릭 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-103">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="f648c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f648c-104">SYNTAX</span></span>

### <span data-ttu-id="f648c-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f648c-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f648c-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="f648c-106">Get</span></span>
```
Get-AzsInfrastructureShare [-Name] <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="f648c-107">리소스</span><span class="sxs-lookup"><span data-stu-id="f648c-107">ResourceId</span></span>
```
Get-AzsInfrastructureShare -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="f648c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f648c-108">DESCRIPTION</span></span>
<span data-ttu-id="f648c-109">특정 위치에 있는 모든 패브릭 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-109">Returns a list of all fabric file shares at a certain location.</span></span>

## <span data-ttu-id="f648c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f648c-110">EXAMPLES</span></span>

### <span data-ttu-id="f648c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f648c-111">EXAMPLE 1</span></span>
```
Get-AzsInfrastructureShare
```

<span data-ttu-id="f648c-112">모든 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="f648c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f648c-113">EXAMPLE 2</span></span>
```
Get-AzsInfrastructureShare -Name Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare.Name
```

<span data-ttu-id="f648c-114">이름을 기반으로 하는 파일 공유를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="f648c-115">변수</span><span class="sxs-lookup"><span data-stu-id="f648c-115">PARAMETERS</span></span>

### <span data-ttu-id="f648c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="f648c-116">-Name</span></span>
<span data-ttu-id="f648c-117">패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-117">Fabric file share name.</span></span>

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

### <span data-ttu-id="f648c-118">-위치</span><span class="sxs-lookup"><span data-stu-id="f648c-118">-Location</span></span>
<span data-ttu-id="f648c-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-119">Location of the resource.</span></span>

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

### <span data-ttu-id="f648c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f648c-120">-ResourceGroupName</span></span>
<span data-ttu-id="f648c-121">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-121">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f648c-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f648c-122">-ResourceId</span></span>
<span data-ttu-id="f648c-123">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-123">The resource id.</span></span>

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

### <span data-ttu-id="f648c-124">-필터</span><span class="sxs-lookup"><span data-stu-id="f648c-124">-Filter</span></span>
<span data-ttu-id="f648c-125">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-125">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f648c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f648c-126">CommonParameters</span></span>
<span data-ttu-id="f648c-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f648c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f648c-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f648c-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f648c-129">입력</span><span class="sxs-lookup"><span data-stu-id="f648c-129">INPUTS</span></span>

## <span data-ttu-id="f648c-130">출력</span><span class="sxs-lookup"><span data-stu-id="f648c-130">OUTPUTS</span></span>

### <span data-ttu-id="f648c-131">Microsoft AzureStack. 관리. a. 관리자. 공유 모델</span><span class="sxs-lookup"><span data-stu-id="f648c-131">Microsoft.AzureStack.Management.Fabric.Admin.Models.FileShare</span></span>

## <span data-ttu-id="f648c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="f648c-132">NOTES</span></span>

## <span data-ttu-id="f648c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f648c-133">RELATED LINKS</span></span>
