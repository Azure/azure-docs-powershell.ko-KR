---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: 29dd6d1938228d3e76c0393ca27f49a3a9fe2564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525735"
---
# <span data-ttu-id="0a4e1-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0a4e1-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="0a4e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a4e1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a4e1-103">PsApiManagement 인스턴스에서 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a4e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a4e1-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0a4e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a4e1-105">DESCRIPTION</span></span>
<span data-ttu-id="0a4e1-106">**AzureRmApiManagementRegion** Cmdlet은 ApiManagement. e **ApiManagement. PsApiManagement** 의 제공 된 인스턴스에 대 한 **additionalregions** 개체의 컬렉션에 있는 **PsApiManagementRegion** 형식의 기존 인스턴스를 업데이트 합니다.).</span><span class="sxs-lookup"><span data-stu-id="0a4e1-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0a4e1-107">이 cmdlet은 모든 항목을 배포 하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0a4e1-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 Update-AzureRmApiManagementDeployment cmdlet에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="0a4e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a4e1-109">EXAMPLES</span></span>

## <span data-ttu-id="0a4e1-110">변수</span><span class="sxs-lookup"><span data-stu-id="0a4e1-110">PARAMETERS</span></span>

### <span data-ttu-id="0a4e1-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4e1-111">-ApiManagement</span></span>
<span data-ttu-id="0a4e1-112">**PsApiManagement** 인스턴스를 지정 하 여의 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="0a4e1-113">용량</span><span class="sxs-lookup"><span data-stu-id="0a4e1-113">-Capacity</span></span>
<span data-ttu-id="0a4e1-114">배포 영역의 새 SKU 용량 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-114">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e1-115">-위치</span><span class="sxs-lookup"><span data-stu-id="0a4e1-115">-Location</span></span>
<span data-ttu-id="0a4e1-116">업데이트할 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-116">Specifies the location of the deployment region to update.</span></span>

<span data-ttu-id="0a4e1-117">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-117">Valid values are:</span></span>

- <span data-ttu-id="0a4e1-118">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-118">North Central US</span></span>
- <span data-ttu-id="0a4e1-119">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="0a4e1-119">South Central US</span></span>
- <span data-ttu-id="0a4e1-120">중부 US</span><span class="sxs-lookup"><span data-stu-id="0a4e1-120">Central US</span></span>
- <span data-ttu-id="0a4e1-121">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="0a4e1-121">West Europe</span></span>
- <span data-ttu-id="0a4e1-122">동유럽</span><span class="sxs-lookup"><span data-stu-id="0a4e1-122">North Europe</span></span>
- <span data-ttu-id="0a4e1-123">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-123">West US</span></span>
- <span data-ttu-id="0a4e1-124">미국 동부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-124">East US</span></span>
- <span data-ttu-id="0a4e1-125">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="0a4e1-125">East US 2</span></span>
- <span data-ttu-id="0a4e1-126">일본 동부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-126">Japan East</span></span>
- <span data-ttu-id="0a4e1-127">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="0a4e1-127">Japan West</span></span>
- <span data-ttu-id="0a4e1-128">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-128">Brazil South</span></span>
- <span data-ttu-id="0a4e1-129">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="0a4e1-129">Southeast Asia</span></span>
- <span data-ttu-id="0a4e1-130">동아시아</span><span class="sxs-lookup"><span data-stu-id="0a4e1-130">East Asia</span></span>
- <span data-ttu-id="0a4e1-131">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="0a4e1-131">Australia East</span></span>
- <span data-ttu-id="0a4e1-132">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="0a4e1-132">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e1-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="0a4e1-133">-Sku</span></span>
<span data-ttu-id="0a4e1-134">배포 영역의 새 계층 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-134">Specifies the new tier value for the deployment region.</span></span>

<span data-ttu-id="0a4e1-135">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-135">Valid values are:</span></span>

- <span data-ttu-id="0a4e1-136">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="0a4e1-136">Developer</span></span>
- <span data-ttu-id="0a4e1-137">표준이</span><span class="sxs-lookup"><span data-stu-id="0a4e1-137">Standard</span></span>
- <span data-ttu-id="0a4e1-138">Premium</span><span class="sxs-lookup"><span data-stu-id="0a4e1-138">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e1-139">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="0a4e1-139">-VirtualNetwork</span></span>
<span data-ttu-id="0a4e1-140">배포 영역에 대 한 가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-140">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="0a4e1-141">$Null를 전달 하면 해당 지역에 대 한 가상 네트워크 구성이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-141">Passing $null will remove virtual network configuration for the region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a4e1-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a4e1-142">-DefaultProfile</span></span>
<span data-ttu-id="0a4e1-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a4e1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a4e1-144">CommonParameters</span></span>
<span data-ttu-id="0a4e1-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a4e1-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a4e1-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a4e1-147">입력</span><span class="sxs-lookup"><span data-stu-id="0a4e1-147">INPUTS</span></span>

### <span data-ttu-id="0a4e1-148">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="0a4e1-148">PsApiManagement</span></span>
<span data-ttu-id="0a4e1-149">' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-149">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="0a4e1-150">출력</span><span class="sxs-lookup"><span data-stu-id="0a4e1-150">OUTPUTS</span></span>

### <span data-ttu-id="0a4e1-151">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="0a4e1-151">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0a4e1-152">상속자</span><span class="sxs-lookup"><span data-stu-id="0a4e1-152">NOTES</span></span>

## <span data-ttu-id="0a4e1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a4e1-153">RELATED LINKS</span></span>

[<span data-ttu-id="0a4e1-154">추가-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0a4e1-154">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="0a4e1-155">제거-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0a4e1-155">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="0a4e1-156">업데이트-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="0a4e1-156">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
