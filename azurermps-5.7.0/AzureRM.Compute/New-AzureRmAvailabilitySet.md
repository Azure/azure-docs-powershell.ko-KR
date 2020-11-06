---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmAvailabilitySet.md
ms.openlocfilehash: b5e9828c0cf9f73f88a44b7a4471a22bbfbe49af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529916"
---
# <span data-ttu-id="1c00f-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c00f-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="1c00f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c00f-102">SYNOPSIS</span></span>
<span data-ttu-id="1c00f-103">Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1c00f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1c00f-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [<CommonParameters>]
```

## <span data-ttu-id="1c00f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1c00f-105">DESCRIPTION</span></span>
<span data-ttu-id="1c00f-106">**AzureRmAvailabilitySet** Cmdlet은 Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="1c00f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1c00f-107">EXAMPLES</span></span>

### <span data-ttu-id="1c00f-108">예제 1: 가용성 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="1c00f-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="1c00f-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에 AvailablitySet03 이라는 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="1c00f-110">변수</span><span class="sxs-lookup"><span data-stu-id="1c00f-110">PARAMETERS</span></span>

### <span data-ttu-id="1c00f-111">-위치</span><span class="sxs-lookup"><span data-stu-id="1c00f-111">-Location</span></span>
<span data-ttu-id="1c00f-112">가용성 집합의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-112">Specifies the location for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-113">관리</span><span class="sxs-lookup"><span data-stu-id="1c00f-113">-Managed</span></span>
<span data-ttu-id="1c00f-114">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="1c00f-114">Managed Availability Set</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="1c00f-115">-Name</span></span>
<span data-ttu-id="1c00f-116">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-116">Specifies a name for the availability set.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, AvailabilitySetName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-117">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="1c00f-117">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="1c00f-118">플랫폼 오류 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-118">Specifies the platform fault domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-119">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="1c00f-119">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="1c00f-120">플랫폼 업데이트 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-120">Specifies the platform update domain count.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c00f-121">-ResourceGroupName</span></span>
<span data-ttu-id="1c00f-122">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-122">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="1c00f-123">-Sku</span><span class="sxs-lookup"><span data-stu-id="1c00f-123">-Sku</span></span>
<span data-ttu-id="1c00f-124">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="1c00f-124">The Name of Sku</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c00f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c00f-125">CommonParameters</span></span>
<span data-ttu-id="1c00f-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c00f-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c00f-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c00f-128">입력</span><span class="sxs-lookup"><span data-stu-id="1c00f-128">INPUTS</span></span>

### <span data-ttu-id="1c00f-129">않아야</span><span class="sxs-lookup"><span data-stu-id="1c00f-129">None</span></span>
<span data-ttu-id="1c00f-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c00f-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1c00f-131">출력</span><span class="sxs-lookup"><span data-stu-id="1c00f-131">OUTPUTS</span></span>

## <span data-ttu-id="1c00f-132">상속자</span><span class="sxs-lookup"><span data-stu-id="1c00f-132">NOTES</span></span>

## <span data-ttu-id="1c00f-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c00f-133">RELATED LINKS</span></span>

[<span data-ttu-id="1c00f-134">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c00f-134">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="1c00f-135">제거-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="1c00f-135">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


