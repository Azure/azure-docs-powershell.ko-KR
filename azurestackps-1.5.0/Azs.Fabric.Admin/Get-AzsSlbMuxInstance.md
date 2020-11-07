---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 42d6233a99979687b7031ab58a620319fa675a28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701694"
---
# <span data-ttu-id="75ac5-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="75ac5-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="75ac5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75ac5-102">SYNOPSIS</span></span>
<span data-ttu-id="75ac5-103">위치에 있는 모든 소프트웨어 부하 분산 장치 인스턴스의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-103">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="75ac5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75ac5-104">SYNTAX</span></span>

### <span data-ttu-id="75ac5-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="75ac5-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="75ac5-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="75ac5-106">Get</span></span>
```
Get-AzsSlbMuxInstance [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="75ac5-107">리소스</span><span class="sxs-lookup"><span data-stu-id="75ac5-107">ResourceId</span></span>
```
Get-AzsSlbMuxInstance -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="75ac5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="75ac5-108">DESCRIPTION</span></span>
<span data-ttu-id="75ac5-109">위치에 있는 모든 소프트웨어 부하 분산 장치 인스턴스의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-109">Returns a list of all software load balancer instances at a location.</span></span>

## <span data-ttu-id="75ac5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="75ac5-110">EXAMPLES</span></span>

### <span data-ttu-id="75ac5-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="75ac5-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSlbMuxInstance
```

<span data-ttu-id="75ac5-112">위치에 있는 모든 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="75ac5-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="75ac5-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsSlbMuxInstance -Name "AzS-SLB01"
```

<span data-ttu-id="75ac5-114">이름에 주어진 위치에 특정 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="75ac5-115">변수</span><span class="sxs-lookup"><span data-stu-id="75ac5-115">PARAMETERS</span></span>

### <span data-ttu-id="75ac5-116">-필터</span><span class="sxs-lookup"><span data-stu-id="75ac5-116">-Filter</span></span>
<span data-ttu-id="75ac5-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="75ac5-118">-위치</span><span class="sxs-lookup"><span data-stu-id="75ac5-118">-Location</span></span>
<span data-ttu-id="75ac5-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-119">Location of the resource.</span></span>

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

### <span data-ttu-id="75ac5-120">-이름</span><span class="sxs-lookup"><span data-stu-id="75ac5-120">-Name</span></span>
<span data-ttu-id="75ac5-121">SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-121">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="75ac5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75ac5-122">-ResourceGroupName</span></span>
<span data-ttu-id="75ac5-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="75ac5-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="75ac5-124">-ResourceId</span></span>
<span data-ttu-id="75ac5-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-125">The resource id.</span></span>

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

### <span data-ttu-id="75ac5-126">-생략</span><span class="sxs-lookup"><span data-stu-id="75ac5-126">-Skip</span></span>
<span data-ttu-id="75ac5-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="75ac5-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="75ac5-128">-Top</span></span>
<span data-ttu-id="75ac5-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="75ac5-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="75ac5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ac5-131">CommonParameters</span></span>
<span data-ttu-id="75ac5-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75ac5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ac5-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ac5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ac5-134">입력</span><span class="sxs-lookup"><span data-stu-id="75ac5-134">INPUTS</span></span>

## <span data-ttu-id="75ac5-135">출력</span><span class="sxs-lookup"><span data-stu-id="75ac5-135">OUTPUTS</span></span>

### <span data-ttu-id="75ac5-136">SlbMuxInstance. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="75ac5-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.SlbMuxInstance</span></span>

## <span data-ttu-id="75ac5-137">상속자</span><span class="sxs-lookup"><span data-stu-id="75ac5-137">NOTES</span></span>

## <span data-ttu-id="75ac5-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75ac5-138">RELATED LINKS</span></span>

