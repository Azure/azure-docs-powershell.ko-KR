---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3def97a3e02e77efd6ec21768b30c855f1ceb34e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874837"
---
# <span data-ttu-id="6535b-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="6535b-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="6535b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6535b-102">SYNOPSIS</span></span>
<span data-ttu-id="6535b-103">모든 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-103">List all quotas.</span></span>

## <span data-ttu-id="6535b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6535b-104">SYNTAX</span></span>

### <span data-ttu-id="6535b-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6535b-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="6535b-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6535b-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="6535b-107">리소스</span><span class="sxs-lookup"><span data-stu-id="6535b-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6535b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6535b-108">DESCRIPTION</span></span>
<span data-ttu-id="6535b-109">모든 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-109">List all quotas.</span></span>
<span data-ttu-id="6535b-110">이름 또는 필터를 전달 하 여 목록을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="6535b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6535b-111">EXAMPLES</span></span>

### <span data-ttu-id="6535b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="6535b-112">EXAMPLE 1</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="6535b-113">모든 네트워크 할당량을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="6535b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="6535b-114">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="6535b-115">지정 된 네트워크 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="6535b-116">변수</span><span class="sxs-lookup"><span data-stu-id="6535b-116">PARAMETERS</span></span>

### <span data-ttu-id="6535b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="6535b-117">-Name</span></span>
<span data-ttu-id="6535b-118">네트워크 할당량 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-118">Network quota resource name.</span></span>

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

### <span data-ttu-id="6535b-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6535b-119">-Location</span></span>
<span data-ttu-id="6535b-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-120">Location of the resource.</span></span>

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

### <span data-ttu-id="6535b-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6535b-121">-ResourceId</span></span>
<span data-ttu-id="6535b-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-122">The resource id.</span></span>

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

### <span data-ttu-id="6535b-123">-필터</span><span class="sxs-lookup"><span data-stu-id="6535b-123">-Filter</span></span>
<span data-ttu-id="6535b-124">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-124">OData filter parameter.</span></span>

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

### <span data-ttu-id="6535b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6535b-125">CommonParameters</span></span>
<span data-ttu-id="6535b-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6535b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6535b-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6535b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6535b-128">입력</span><span class="sxs-lookup"><span data-stu-id="6535b-128">INPUTS</span></span>

## <span data-ttu-id="6535b-129">출력</span><span class="sxs-lookup"><span data-stu-id="6535b-129">OUTPUTS</span></span>

### <span data-ttu-id="6535b-130">Microsoft AzureStack. 관리자. i a 관리. 할당량</span><span class="sxs-lookup"><span data-stu-id="6535b-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="6535b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="6535b-131">NOTES</span></span>

## <span data-ttu-id="6535b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6535b-132">RELATED LINKS</span></span>
