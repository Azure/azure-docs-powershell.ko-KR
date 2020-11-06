---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementRegion.md
ms.openlocfilehash: ed26538e54cef189837bd36bf9e6f561df3541f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526356"
---
# <span data-ttu-id="2d9c1-101">Update-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2d9c1-101">Update-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="2d9c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d9c1-102">SYNOPSIS</span></span>
<span data-ttu-id="2d9c1-103">PsApiManagement 인스턴스에서 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-103">Updates existing deployment region in PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d9c1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2d9c1-104">SYNTAX</span></span>

```
Update-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d9c1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2d9c1-105">DESCRIPTION</span></span>
<span data-ttu-id="2d9c1-106">**AzureRmApiManagementRegion** Cmdlet은 ApiManagement. e **ApiManagement. PsApiManagement** 의 제공 된 인스턴스에 대 한 **additionalregions** 개체의 컬렉션에 있는 **PsApiManagementRegion** 형식의 기존 인스턴스를 업데이트 합니다.).</span><span class="sxs-lookup"><span data-stu-id="2d9c1-106">The **Update-AzureRmApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="2d9c1-107">이 cmdlet은 모든 항목을 배포 하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="2d9c1-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 Update-AzureRmApiManagementDeployment cmdlet에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Update-AzureRmApiManagementDeployment cmdlet.</span></span>

## <span data-ttu-id="2d9c1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2d9c1-109">EXAMPLES</span></span>

## <span data-ttu-id="2d9c1-110">변수</span><span class="sxs-lookup"><span data-stu-id="2d9c1-110">PARAMETERS</span></span>

### <span data-ttu-id="2d9c1-111">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="2d9c1-111">-ApiManagement</span></span>
<span data-ttu-id="2d9c1-112">**PsApiManagement** 인스턴스를 지정 하 여의 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-112">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="2d9c1-113">용량</span><span class="sxs-lookup"><span data-stu-id="2d9c1-113">-Capacity</span></span>
<span data-ttu-id="2d9c1-114">배포 영역의 새 SKU 용량 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-114">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="2d9c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d9c1-115">-DefaultProfile</span></span>
<span data-ttu-id="2d9c1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d9c1-117">-위치</span><span class="sxs-lookup"><span data-stu-id="2d9c1-117">-Location</span></span>
<span data-ttu-id="2d9c1-118">업데이트할 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-118">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="2d9c1-119">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="2d9c1-120">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="2d9c1-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="2d9c1-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="2d9c1-121">-Sku</span></span>
<span data-ttu-id="2d9c1-122">배포 영역의 새 계층 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-122">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="2d9c1-123">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-123">Valid values are:</span></span>
- <span data-ttu-id="2d9c1-124">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="2d9c1-124">Developer</span></span>
- <span data-ttu-id="2d9c1-125">표준이</span><span class="sxs-lookup"><span data-stu-id="2d9c1-125">Standard</span></span>
- <span data-ttu-id="2d9c1-126">Premium</span><span class="sxs-lookup"><span data-stu-id="2d9c1-126">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d9c1-127">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="2d9c1-127">-VirtualNetwork</span></span>
<span data-ttu-id="2d9c1-128">배포 영역에 대 한 가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-128">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="2d9c1-129">$Null를 전달 하면 해당 지역에 대 한 가상 네트워크 구성이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-129">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="2d9c1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d9c1-130">CommonParameters</span></span>
<span data-ttu-id="2d9c1-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d9c1-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d9c1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d9c1-133">입력</span><span class="sxs-lookup"><span data-stu-id="2d9c1-133">INPUTS</span></span>

### <span data-ttu-id="2d9c1-134">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-134">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="2d9c1-135">매개 변수: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2d9c1-135">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="2d9c1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2d9c1-136">System.String</span></span>

### <span data-ttu-id="2d9c1-137">ApiManagement. PsApiManagementSku/.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="2d9c1-138">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-138">System.Int32</span></span>

### <span data-ttu-id="2d9c1-139">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-139">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="2d9c1-140">출력</span><span class="sxs-lookup"><span data-stu-id="2d9c1-140">OUTPUTS</span></span>

### <span data-ttu-id="2d9c1-141">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="2d9c1-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="2d9c1-142">상속자</span><span class="sxs-lookup"><span data-stu-id="2d9c1-142">NOTES</span></span>

## <span data-ttu-id="2d9c1-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2d9c1-143">RELATED LINKS</span></span>

[<span data-ttu-id="2d9c1-144">추가-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2d9c1-144">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="2d9c1-145">제거-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="2d9c1-145">Remove-AzureRmApiManagementRegion</span></span>](./Remove-AzureRmApiManagementRegion.md)

[<span data-ttu-id="2d9c1-146">업데이트-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="2d9c1-146">Update-AzureRmApiManagementDeployment</span></span>](./Update-AzureRmApiManagementDeployment.md)
