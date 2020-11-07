---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BF6AA8D4-D624-4BE1-A393-1A43909450C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermavailabilityset
schema: 2.0.0
ms.openlocfilehash: f08de8d1ea5f157270617c69a2092764d0ad4657
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880766"
---
# <span data-ttu-id="2e513-101">New-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2e513-101">New-AzureRmAvailabilitySet</span></span>

## <span data-ttu-id="2e513-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e513-102">SYNOPSIS</span></span>
<span data-ttu-id="2e513-103">Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-103">Creates an Azure availability set.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2e513-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e513-104">SYNTAX</span></span>

```
New-AzureRmAvailabilitySet [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-PlatformUpdateDomainCount] <Int32>] [[-PlatformFaultDomainCount] <Int32>] [[-Sku] <String>] [-Managed]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e513-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e513-105">DESCRIPTION</span></span>
<span data-ttu-id="2e513-106">**AzureRmAvailabilitySet** Cmdlet은 Azure 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-106">The **New-AzureRmAvailabilitySet** cmdlet creates an Azure availability set.</span></span>

## <span data-ttu-id="2e513-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2e513-107">EXAMPLES</span></span>

### <span data-ttu-id="2e513-108">예제 1: 가용성 집합 만들기</span><span class="sxs-lookup"><span data-stu-id="2e513-108">Example 1: Create an availability set</span></span>
```
PS C:\> New-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03" -Location "West US"
```

<span data-ttu-id="2e513-109">이 명령은 ResourceGroup11 이라는 리소스 그룹에 AvailablitySet03 이라는 가용성 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-109">This command creates an availability set named AvailablitySet03 in the resource group named ResourceGroup11.</span></span>

## <span data-ttu-id="2e513-110">변수</span><span class="sxs-lookup"><span data-stu-id="2e513-110">PARAMETERS</span></span>

### <span data-ttu-id="2e513-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e513-111">-AsJob</span></span>
<span data-ttu-id="2e513-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e513-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e513-113">-DefaultProfile</span></span>
<span data-ttu-id="2e513-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e513-115">-위치</span><span class="sxs-lookup"><span data-stu-id="2e513-115">-Location</span></span>
<span data-ttu-id="2e513-116">가용성 집합의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-116">Specifies the location for the availability set.</span></span>

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

### <span data-ttu-id="2e513-117">관리</span><span class="sxs-lookup"><span data-stu-id="2e513-117">-Managed</span></span>
<span data-ttu-id="2e513-118">관리 되는 가용성 집합</span><span class="sxs-lookup"><span data-stu-id="2e513-118">Managed Availability Set</span></span>
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

### <span data-ttu-id="2e513-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2e513-119">-Name</span></span>
<span data-ttu-id="2e513-120">가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-120">Specifies a name for the availability set.</span></span>

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

### <span data-ttu-id="2e513-121">-PlatformFaultDomainCount</span><span class="sxs-lookup"><span data-stu-id="2e513-121">-PlatformFaultDomainCount</span></span>
<span data-ttu-id="2e513-122">플랫폼 오류 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-122">Specifies the platform fault domain count.</span></span>

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

### <span data-ttu-id="2e513-123">-PlatformUpdateDomainCount</span><span class="sxs-lookup"><span data-stu-id="2e513-123">-PlatformUpdateDomainCount</span></span>
<span data-ttu-id="2e513-124">플랫폼 업데이트 도메인 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-124">Specifies the platform update domain count.</span></span>

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

### <span data-ttu-id="2e513-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e513-125">-ResourceGroupName</span></span>
<span data-ttu-id="2e513-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2e513-127">-Sku</span><span class="sxs-lookup"><span data-stu-id="2e513-127">-Sku</span></span>
<span data-ttu-id="2e513-128">Sku 이름</span><span class="sxs-lookup"><span data-stu-id="2e513-128">The Name of Sku</span></span>
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

### <span data-ttu-id="2e513-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e513-129">CommonParameters</span></span>
<span data-ttu-id="2e513-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e513-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e513-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e513-132">입력</span><span class="sxs-lookup"><span data-stu-id="2e513-132">INPUTS</span></span>

### <span data-ttu-id="2e513-133">않아야</span><span class="sxs-lookup"><span data-stu-id="2e513-133">None</span></span>
<span data-ttu-id="2e513-134">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2e513-135">출력</span><span class="sxs-lookup"><span data-stu-id="2e513-135">OUTPUTS</span></span>

### <span data-ttu-id="2e513-136">PSAvailabilitySet를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e513-136">Microsoft.Azure.Commands.Compute.Models.PSAvailabilitySet</span></span>

## <span data-ttu-id="2e513-137">상속자</span><span class="sxs-lookup"><span data-stu-id="2e513-137">NOTES</span></span>

## <span data-ttu-id="2e513-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e513-138">RELATED LINKS</span></span>

[<span data-ttu-id="2e513-139">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2e513-139">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="2e513-140">제거-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="2e513-140">Remove-AzureRmAvailabilitySet</span></span>](./Remove-AzureRmAvailabilitySet.md)


