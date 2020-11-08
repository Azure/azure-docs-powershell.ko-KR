---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046991"
---
# <span data-ttu-id="b9c6d-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="b9c6d-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="b9c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c6d-103">모든 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-103">List all quotas.</span></span>

## <span data-ttu-id="b9c6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b9c6d-104">SYNTAX</span></span>

### <span data-ttu-id="b9c6d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b9c6d-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9c6d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b9c6d-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="b9c6d-107">리소스</span><span class="sxs-lookup"><span data-stu-id="b9c6d-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b9c6d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b9c6d-108">DESCRIPTION</span></span>
<span data-ttu-id="b9c6d-109">모든 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-109">List all quotas.</span></span>
<span data-ttu-id="b9c6d-110">이름 또는 필터를 전달 하 여 목록을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="b9c6d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b9c6d-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c6d-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b9c6d-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="b9c6d-113">모든 네트워크 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="b9c6d-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="b9c6d-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="b9c6d-115">지정 된 네트워크 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="b9c6d-116">변수</span><span class="sxs-lookup"><span data-stu-id="b9c6d-116">PARAMETERS</span></span>

### <span data-ttu-id="b9c6d-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b9c6d-117">-Name</span></span>
<span data-ttu-id="b9c6d-118">네트워크 할당량 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="b9c6d-119">-위치</span><span class="sxs-lookup"><span data-stu-id="b9c6d-119">-Location</span></span>
<span data-ttu-id="b9c6d-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-120">Location of the resource.</span></span>

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

### <span data-ttu-id="b9c6d-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9c6d-121">-ResourceId</span></span>
<span data-ttu-id="b9c6d-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-122">The resource id.</span></span>

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

### <span data-ttu-id="b9c6d-123">-필터</span><span class="sxs-lookup"><span data-stu-id="b9c6d-123">-Filter</span></span>
<span data-ttu-id="b9c6d-124">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="b9c6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c6d-125">CommonParameters</span></span>
<span data-ttu-id="b9c6d-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b9c6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c6d-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9c6d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c6d-128">입력</span><span class="sxs-lookup"><span data-stu-id="b9c6d-128">INPUTS</span></span>

## <span data-ttu-id="b9c6d-129">출력</span><span class="sxs-lookup"><span data-stu-id="b9c6d-129">OUTPUTS</span></span>

### <span data-ttu-id="b9c6d-130">Microsoft AzureStack. 관리자. i a 관리. 할당량</span><span class="sxs-lookup"><span data-stu-id="b9c6d-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="b9c6d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b9c6d-131">NOTES</span></span>

## <span data-ttu-id="b9c6d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b9c6d-132">RELATED LINKS</span></span>
