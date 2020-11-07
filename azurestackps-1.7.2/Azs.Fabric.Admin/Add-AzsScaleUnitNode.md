---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09391f521a2b75663b25731c6cc20ef78a658d5f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874583"
---
# <span data-ttu-id="8acb3-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8acb3-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8acb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8acb3-102">SYNOPSIS</span></span>
<span data-ttu-id="8acb3-103">배율 단위를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-103">Scale out a scale unit.</span></span>

## <span data-ttu-id="8acb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8acb3-104">SYNTAX</span></span>

```
Add-AzsScaleUnitNode [-NodeList] <ScaleOutScaleUnitParameters[]> [[-ResourceGroupName] <String>]
 [-ScaleUnit] <String> [[-Location] <String>] [-AwaitStorageConvergence] [-AsJob] [<CommonParameters>]
```

## <span data-ttu-id="8acb3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8acb3-105">DESCRIPTION</span></span>
<span data-ttu-id="8acb3-106">확장 단위 클러스터에 새 배율 단위 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-106">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="8acb3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8acb3-107">EXAMPLES</span></span>

### <span data-ttu-id="8acb3-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="8acb3-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName
```

<span data-ttu-id="8acb3-109">눈금 단위에 노드 목록을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-109">Adds a list of nodes to the scale unit.</span></span>

## <span data-ttu-id="8acb3-110">변수</span><span class="sxs-lookup"><span data-stu-id="8acb3-110">PARAMETERS</span></span>

### <span data-ttu-id="8acb3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8acb3-111">-AsJob</span></span>
<span data-ttu-id="8acb3-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-112">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-113">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="8acb3-113">-AwaitStorageConvergence</span></span>
<span data-ttu-id="8acb3-114">성공으로 반환 하기 전에 저장소 복제가 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-114">Wait for storage replication to complete before returning success.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-115">-위치</span><span class="sxs-lookup"><span data-stu-id="8acb3-115">-Location</span></span>
<span data-ttu-id="8acb3-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-117">-NodeList</span><span class="sxs-lookup"><span data-stu-id="8acb3-117">-NodeList</span></span>
<span data-ttu-id="8acb3-118">배율 단위 노드 집합을 추가 하는 데 사용할 수 있는 입력 데이터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-118">A list of input data that allows for adding a set of scale unit nodes.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8acb3-119">-ResourceGroupName</span></span>
<span data-ttu-id="8acb3-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-120">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-121">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8acb3-121">-ScaleUnit</span></span>
<span data-ttu-id="8acb3-122">눈금 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-122">Name of the scale units.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8acb3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8acb3-123">CommonParameters</span></span>
<span data-ttu-id="8acb3-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8acb3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8acb3-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8acb3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8acb3-126">입력</span><span class="sxs-lookup"><span data-stu-id="8acb3-126">INPUTS</span></span>

## <span data-ttu-id="8acb3-127">출력</span><span class="sxs-lookup"><span data-stu-id="8acb3-127">OUTPUTS</span></span>

## <span data-ttu-id="8acb3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8acb3-128">NOTES</span></span>

## <span data-ttu-id="8acb3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8acb3-129">RELATED LINKS</span></span>

