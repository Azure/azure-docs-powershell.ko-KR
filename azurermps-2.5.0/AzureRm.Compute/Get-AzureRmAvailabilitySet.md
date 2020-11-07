---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: ef00a9e425f67fbfc1ce47746503b574d483598f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880770"
---
# <span data-ttu-id="d8d67-101">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d67-101">Get-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="d8d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8d67-102">SYNOPSIS</span></span>
<span data-ttu-id="d8d67-103">리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-103">Gets Azure availability sets in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8d67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8d67-104">SYNTAX</span></span>

```
Get-AzureRmAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8d67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d8d67-105">DESCRIPTION</span></span>
<span data-ttu-id="d8d67-106">**Get-AzureRmAvailabilitySet** cmdlet은 리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-106">The **Get-AzureRmAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="d8d67-107">가져올 특정 가용성 집합의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="d8d67-108">예제의</span><span class="sxs-lookup"><span data-stu-id="d8d67-108">EXAMPLES</span></span>

### <span data-ttu-id="d8d67-109">예제 1: 특정 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8d67-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="d8d67-110">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="d8d67-111">예제 2: 모든 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="d8d67-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="d8d67-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 모든 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="d8d67-113">변수</span><span class="sxs-lookup"><span data-stu-id="d8d67-113">PARAMETERS</span></span>

### <span data-ttu-id="d8d67-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8d67-114">-DefaultProfile</span></span>
<span data-ttu-id="d8d67-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8d67-116">-이름</span><span class="sxs-lookup"><span data-stu-id="d8d67-116">-Name</span></span>
<span data-ttu-id="d8d67-117">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d67-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8d67-118">-ResourceGroupName</span></span>
<span data-ttu-id="d8d67-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-119">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8d67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8d67-120">CommonParameters</span></span>
<span data-ttu-id="d8d67-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8d67-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8d67-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8d67-123">입력</span><span class="sxs-lookup"><span data-stu-id="d8d67-123">INPUTS</span></span>

### <span data-ttu-id="d8d67-124">않아야</span><span class="sxs-lookup"><span data-stu-id="d8d67-124">None</span></span>
<span data-ttu-id="d8d67-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d8d67-126">출력</span><span class="sxs-lookup"><span data-stu-id="d8d67-126">OUTPUTS</span></span>

### <span data-ttu-id="d8d67-127">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8d67-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="d8d67-128">상속자</span><span class="sxs-lookup"><span data-stu-id="d8d67-128">NOTES</span></span>

## <span data-ttu-id="d8d67-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8d67-129">RELATED LINKS</span></span>

[<span data-ttu-id="d8d67-130">새로운 AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d67-130">New-AzureRmAvailabilitySet</span></span>](./New-AzureRmAvailabilitySet.md)

[<span data-ttu-id="d8d67-131">제거-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="d8d67-131">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


