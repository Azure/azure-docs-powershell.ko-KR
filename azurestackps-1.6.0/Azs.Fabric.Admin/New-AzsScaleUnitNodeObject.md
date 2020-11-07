---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 70d8ded2b2954746a97d6144f33c043c27341da4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701708"
---
# <span data-ttu-id="5f451-101">New-AzsScaleUnitNodeObject</span><span class="sxs-lookup"><span data-stu-id="5f451-101">New-AzsScaleUnitNodeObject</span></span>

## <span data-ttu-id="5f451-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f451-102">SYNOPSIS</span></span>
<span data-ttu-id="5f451-103">배율 단위 노드를 추가 하는 데 사용할 수 있는 입력 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-103">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="5f451-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5f451-104">SYNTAX</span></span>

```
New-AzsScaleUnitNodeObject [[-BMCIPv4Address] <String>] [[-ComputerName] <String>] [<CommonParameters>]
```

## <span data-ttu-id="5f451-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5f451-105">DESCRIPTION</span></span>
<span data-ttu-id="5f451-106">배율 단위 노드를 추가 하는 데 사용할 수 있는 입력 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-106">Input data that allows for adding a scale unit node.</span></span>

## <span data-ttu-id="5f451-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5f451-107">EXAMPLES</span></span>

### <span data-ttu-id="5f451-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5f451-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsScaleUnitNodeObject -BMCIPv4Address 192.168.1.1 -ComputeName 'NodeName'
```

<span data-ttu-id="5f451-109">새 노드 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-109">Create a new node object.</span></span>

## <span data-ttu-id="5f451-110">변수</span><span class="sxs-lookup"><span data-stu-id="5f451-110">PARAMETERS</span></span>

### <span data-ttu-id="5f451-111">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="5f451-111">-BMCIPv4Address</span></span>
<span data-ttu-id="5f451-112">물리적 컴퓨터의 Bmc 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-112">Bmc address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f451-113">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="5f451-113">-ComputerName</span></span>
<span data-ttu-id="5f451-114">물리적 컴퓨터의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-114">Computer name of the physical machine.</span></span>

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

### <span data-ttu-id="5f451-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f451-115">CommonParameters</span></span>
<span data-ttu-id="5f451-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f451-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f451-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f451-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f451-118">입력</span><span class="sxs-lookup"><span data-stu-id="5f451-118">INPUTS</span></span>

## <span data-ttu-id="5f451-119">출력</span><span class="sxs-lookup"><span data-stu-id="5f451-119">OUTPUTS</span></span>

## <span data-ttu-id="5f451-120">상속자</span><span class="sxs-lookup"><span data-stu-id="5f451-120">NOTES</span></span>

## <span data-ttu-id="5f451-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f451-121">RELATED LINKS</span></span>

