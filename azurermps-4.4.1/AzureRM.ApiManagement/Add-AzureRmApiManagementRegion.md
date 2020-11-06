---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementRegion.md
ms.openlocfilehash: 7edf16a6970f831235f76c64ef5cb5181a49bf98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535552"
---
# <span data-ttu-id="6a846-101">Add-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6a846-101">Add-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="6a846-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a846-102">SYNOPSIS</span></span>
<span data-ttu-id="6a846-103">PsApiManagement 인스턴스에 새 배포 영역을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a846-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a846-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a846-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a846-105">DESCRIPTION</span></span>
<span data-ttu-id="6a846-106">**AzureRmApiManagementRegion** Cmdlet은 **PsApiManagementRegion** 형식의 새 인스턴스를 **ApiManagement. PsApiManagement** 유형의 제공 된 **additionalregions** 컬렉션에 추가 합니다..</span><span class="sxs-lookup"><span data-stu-id="6a846-106">The **Add-AzureRmApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="6a846-107">이 cmdlet은 자기 자신을 배포 하는 것이 아니라 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="6a846-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagement** 인스턴스를 Update-AzureRmApiManagementDeployment에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Update-AzureRmApiManagementDeployment.</span></span>

## <span data-ttu-id="6a846-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6a846-109">EXAMPLES</span></span>

### <span data-ttu-id="6a846-110">예제 1: PsApiManagement 인스턴스에 새 배포 영역 추가</span><span class="sxs-lookup"><span data-stu-id="6a846-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="6a846-111">이 명령은 2 개의 premium SKU 단위와 동부 US 라는 지역 번호를 **PsApiManagement** 인스턴스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="6a846-112">예제 2: PsApiManagement 인스턴스에 새 배포 영역 추가 후 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="6a846-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi" | Add-AzureRmApiManagementRegion -Location "East US" -Sku "Premium" -Capacity 2 | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="6a846-113">이 명령은 **PsApiManagement** 개체를 가져오고 동부 US 이라는 지역에 대해 두 개의 premium SKU 단위를 추가한 다음 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="6a846-114">변수</span><span class="sxs-lookup"><span data-stu-id="6a846-114">PARAMETERS</span></span>

### <span data-ttu-id="6a846-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a846-115">-ApiManagement</span></span>
<span data-ttu-id="6a846-116">이 cmdlet이 추가 배포 영역을 추가 하는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-117">용량</span><span class="sxs-lookup"><span data-stu-id="6a846-117">-Capacity</span></span>
<span data-ttu-id="6a846-118">배포 영역의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-118">Specifies the SKU capacity of the deployment region.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-119">-위치</span><span class="sxs-lookup"><span data-stu-id="6a846-119">-Location</span></span>
<span data-ttu-id="6a846-120">새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-120">Specifies the location of the new deployment region.</span></span>

<span data-ttu-id="6a846-121">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-121">Valid values are:</span></span> 

- <span data-ttu-id="6a846-122">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="6a846-122">North Central US</span></span>
- <span data-ttu-id="6a846-123">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="6a846-123">South Central US</span></span>
- <span data-ttu-id="6a846-124">중부 US</span><span class="sxs-lookup"><span data-stu-id="6a846-124">Central US</span></span>
- <span data-ttu-id="6a846-125">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="6a846-125">West Europe</span></span>
- <span data-ttu-id="6a846-126">동유럽</span><span class="sxs-lookup"><span data-stu-id="6a846-126">North Europe</span></span>
- <span data-ttu-id="6a846-127">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="6a846-127">West US</span></span>
- <span data-ttu-id="6a846-128">미국 동부</span><span class="sxs-lookup"><span data-stu-id="6a846-128">East US</span></span>
- <span data-ttu-id="6a846-129">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="6a846-129">East US 2</span></span>
- <span data-ttu-id="6a846-130">일본 동부</span><span class="sxs-lookup"><span data-stu-id="6a846-130">Japan East</span></span>
- <span data-ttu-id="6a846-131">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="6a846-131">Japan West</span></span>
- <span data-ttu-id="6a846-132">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="6a846-132">Brazil South</span></span>
- <span data-ttu-id="6a846-133">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="6a846-133">Southeast Asia</span></span>
- <span data-ttu-id="6a846-134">동아시아</span><span class="sxs-lookup"><span data-stu-id="6a846-134">East Asia</span></span>
- <span data-ttu-id="6a846-135">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="6a846-135">Australia East</span></span>
- <span data-ttu-id="6a846-136">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="6a846-136">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-137">-Sku</span><span class="sxs-lookup"><span data-stu-id="6a846-137">-Sku</span></span>
<span data-ttu-id="6a846-138">배포 영역의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-138">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="6a846-139">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-139">Valid values are:</span></span> 

- <span data-ttu-id="6a846-140">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="6a846-140">Developer</span></span>
- <span data-ttu-id="6a846-141">표준이</span><span class="sxs-lookup"><span data-stu-id="6a846-141">Standard</span></span>
- <span data-ttu-id="6a846-142">Premium</span><span class="sxs-lookup"><span data-stu-id="6a846-142">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-143">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6a846-143">-VirtualNetwork</span></span>
<span data-ttu-id="6a846-144">가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-144">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a846-145">-DefaultProfile</span></span>
<span data-ttu-id="6a846-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a846-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a846-147">CommonParameters</span></span>
<span data-ttu-id="6a846-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a846-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a846-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a846-150">입력</span><span class="sxs-lookup"><span data-stu-id="6a846-150">INPUTS</span></span>

### <span data-ttu-id="6a846-151">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="6a846-151">PsApiManagement</span></span>
<span data-ttu-id="6a846-152">' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-152">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="6a846-153">출력</span><span class="sxs-lookup"><span data-stu-id="6a846-153">OUTPUTS</span></span>

### <span data-ttu-id="6a846-154">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="6a846-154">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="6a846-155">상속자</span><span class="sxs-lookup"><span data-stu-id="6a846-155">NOTES</span></span>
* <span data-ttu-id="6a846-156">Cmdlet은 파이프라인에 업데이트 된 **PsApiManagement** 인스턴스를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="6a846-156">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="6a846-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a846-157">RELATED LINKS</span></span>

[<span data-ttu-id="6a846-158">제거-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6a846-158">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="6a846-159">업데이트-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="6a846-159">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)

[<span data-ttu-id="6a846-160">업데이트-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="6a846-160">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)


