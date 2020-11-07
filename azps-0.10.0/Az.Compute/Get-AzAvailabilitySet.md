---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 45D55DC9-0027-4EB9-B2F7-9ABF6685E6B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azavailabilityset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzAvailabilitySet.md
ms.openlocfilehash: ef42e8910b9ff6a71277c998825aa53cd3ad085e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877099"
---
# <span data-ttu-id="ce2cf-101">Get-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce2cf-101">Get-AzAvailabilitySet</span></span>

## <span data-ttu-id="ce2cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce2cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ce2cf-103">리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-103">Gets Azure availability sets in a resource group.</span></span>

## <span data-ttu-id="ce2cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce2cf-104">SYNTAX</span></span>

```
Get-AzAvailabilitySet [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce2cf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce2cf-105">DESCRIPTION</span></span>
<span data-ttu-id="ce2cf-106">**Get-AzAvailabilitySet** cmdlet은 리소스 그룹의 Azure 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-106">The **Get-AzAvailabilitySet** cmdlet gets Azure availability sets in a resource group.</span></span>
<span data-ttu-id="ce2cf-107">가져올 특정 가용성 집합의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-107">You can specify the name of a specific availability set to get.</span></span>

## <span data-ttu-id="ce2cf-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ce2cf-108">EXAMPLES</span></span>

### <span data-ttu-id="ce2cf-109">예제 1: 특정 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="ce2cf-109">Example 1: Get a specific availability set</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
```

<span data-ttu-id="ce2cf-110">이 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet03 이라는 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-110">This command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="ce2cf-111">예제 2: 모든 가용성 집합 가져오기</span><span class="sxs-lookup"><span data-stu-id="ce2cf-111">Example 2: Get all availability sets</span></span>
```
PS C:\> Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11"
```

<span data-ttu-id="ce2cf-112">이 명령은 ResourceGroup11 이라는 리소스 그룹에 있는 모든 가용성 집합을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-112">This command gets all the availability sets in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="ce2cf-113">변수</span><span class="sxs-lookup"><span data-stu-id="ce2cf-113">PARAMETERS</span></span>

### <span data-ttu-id="ce2cf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce2cf-114">-DefaultProfile</span></span>
<span data-ttu-id="ce2cf-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce2cf-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ce2cf-116">-Name</span></span>
<span data-ttu-id="ce2cf-117">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-117">Specifies the name of an availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="ce2cf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce2cf-118">-ResourceGroupName</span></span>
<span data-ttu-id="ce2cf-119">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-119">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ce2cf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce2cf-120">CommonParameters</span></span>
<span data-ttu-id="ce2cf-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce2cf-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce2cf-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce2cf-123">입력</span><span class="sxs-lookup"><span data-stu-id="ce2cf-123">INPUTS</span></span>

### <span data-ttu-id="ce2cf-124">않아야</span><span class="sxs-lookup"><span data-stu-id="ce2cf-124">None</span></span>
<span data-ttu-id="ce2cf-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce2cf-126">출력</span><span class="sxs-lookup"><span data-stu-id="ce2cf-126">OUTPUTS</span></span>

### <span data-ttu-id="ce2cf-127">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce2cf-127">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="ce2cf-128">상속자</span><span class="sxs-lookup"><span data-stu-id="ce2cf-128">NOTES</span></span>

## <span data-ttu-id="ce2cf-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce2cf-129">RELATED LINKS</span></span>

[<span data-ttu-id="ce2cf-130">새로운 AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce2cf-130">New-AzAvailabilitySet</span></span>](./New-AzAvailabilitySet.md)

[<span data-ttu-id="ce2cf-131">제거-AzAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="ce2cf-131">Remove-AzAvailabilitySet</span></span>](./Remove-AzAvailabilitySet.md)


