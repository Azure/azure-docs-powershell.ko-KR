---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5c686faa457d83ab0ddffb932b20ab5fcd168ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523972"
---
# <span data-ttu-id="b7026-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="b7026-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="b7026-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7026-102">SYNOPSIS</span></span>
<span data-ttu-id="b7026-103">위치에 있는 모든 MAC 주소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-103">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="b7026-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7026-104">SYNTAX</span></span>

### <span data-ttu-id="b7026-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7026-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="b7026-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b7026-106">Get</span></span>
```
Get-AzsMacAddressPool [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="b7026-107">리소스</span><span class="sxs-lookup"><span data-stu-id="b7026-107">ResourceId</span></span>
```
Get-AzsMacAddressPool -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="b7026-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b7026-108">DESCRIPTION</span></span>
<span data-ttu-id="b7026-109">위치에 있는 모든 MAC 주소 풀의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-109">Returns a list of all MAC address pools at a location.</span></span>

## <span data-ttu-id="b7026-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b7026-110">EXAMPLES</span></span>

### <span data-ttu-id="b7026-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7026-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsMacAddressPool
```

<span data-ttu-id="b7026-112">위치에서 모든 MAC 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-112">Get all MAC address pools at a location.</span></span>

### <span data-ttu-id="b7026-113">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="b7026-113">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"
```

<span data-ttu-id="b7026-114">이름에 따라 위치에 특정 MAC 주소 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="b7026-115">변수</span><span class="sxs-lookup"><span data-stu-id="b7026-115">PARAMETERS</span></span>

### <span data-ttu-id="b7026-116">-필터</span><span class="sxs-lookup"><span data-stu-id="b7026-116">-Filter</span></span>
<span data-ttu-id="b7026-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="b7026-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b7026-118">-Location</span></span>
<span data-ttu-id="b7026-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-119">Location of the resource.</span></span>

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

### <span data-ttu-id="b7026-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b7026-120">-Name</span></span>
<span data-ttu-id="b7026-121">MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-121">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="b7026-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7026-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7026-123">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="b7026-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7026-124">-ResourceId</span></span>
<span data-ttu-id="b7026-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-125">The resource id.</span></span>

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

### <span data-ttu-id="b7026-126">-생략</span><span class="sxs-lookup"><span data-stu-id="b7026-126">-Skip</span></span>
<span data-ttu-id="b7026-127">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-127">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="b7026-128">-위쪽</span><span class="sxs-lookup"><span data-stu-id="b7026-128">-Top</span></span>
<span data-ttu-id="b7026-129">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-129">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="b7026-130">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-130">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="b7026-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7026-131">CommonParameters</span></span>
<span data-ttu-id="b7026-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7026-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7026-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7026-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7026-134">입력</span><span class="sxs-lookup"><span data-stu-id="b7026-134">INPUTS</span></span>

## <span data-ttu-id="b7026-135">출력</span><span class="sxs-lookup"><span data-stu-id="b7026-135">OUTPUTS</span></span>

### <span data-ttu-id="b7026-136">MacAddressPool. 관리. m a. 관리자</span><span class="sxs-lookup"><span data-stu-id="b7026-136">Microsoft.AzureStack.Management.Fabric.Admin.Models.MacAddressPool</span></span>

## <span data-ttu-id="b7026-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b7026-137">NOTES</span></span>

## <span data-ttu-id="b7026-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7026-138">RELATED LINKS</span></span>

