---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 7fa565eb16ced9e9146b219d7850354e499ef06e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697911"
---
# <span data-ttu-id="f7db8-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f7db8-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="f7db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7db8-102">SYNOPSIS</span></span>
<span data-ttu-id="f7db8-103">PsApiManagement 인스턴스에서 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="f7db8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f7db8-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7db8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f7db8-105">DESCRIPTION</span></span>
<span data-ttu-id="f7db8-106">**AzApiManagementRegion** Cmdlet은 ApiManagement. e **ApiManagement. PsApiManagement** 의 제공 된 인스턴스에 대 한 **additionalregions** 개체의 컬렉션에 있는 **PsApiManagementRegion** 형식의 기존 인스턴스를 업데이트 합니다.).</span><span class="sxs-lookup"><span data-stu-id="f7db8-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="f7db8-107">이 cmdlet은 모든 항목을 배포 하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="f7db8-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 Set-AzApiManagement cmdlet에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="f7db8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f7db8-109">EXAMPLES</span></span>

### <span data-ttu-id="f7db8-110">예제 1: PsApiManagement 인스턴스에서 추가 영역의 용량 증가</span><span class="sxs-lookup"><span data-stu-id="f7db8-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="f7db8-111">이 명령은 중앙 미국 및 미국 중부의 국가를 포함 하는 API Management Premium SKU 서비스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="f7db8-112">그런 다음 **AzApiManagement** 를 사용 하 여 북쪽 중앙 미국 지역의 용량을 2로 늘립니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="f7db8-113">다음 cmdlet **집합-AzApiManagement** 는 구성 변경 사항을 Api Management 서비스에 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

## <span data-ttu-id="f7db8-114">변수</span><span class="sxs-lookup"><span data-stu-id="f7db8-114">PARAMETERS</span></span>

### <span data-ttu-id="f7db8-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7db8-115">-ApiManagement</span></span>
<span data-ttu-id="f7db8-116">**PsApiManagement** 인스턴스를 지정 하 여의 기존 배포 영역을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-116">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="f7db8-117">용량</span><span class="sxs-lookup"><span data-stu-id="f7db8-117">-Capacity</span></span>
<span data-ttu-id="f7db8-118">배포 영역의 새 SKU 용량 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-118">Specifies the new SKU capacity value for the deployment region.</span></span>

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

### <span data-ttu-id="f7db8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7db8-119">-DefaultProfile</span></span>
<span data-ttu-id="f7db8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-121">-위치</span><span class="sxs-lookup"><span data-stu-id="f7db8-121">-Location</span></span>
<span data-ttu-id="f7db8-122">업데이트할 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-122">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="f7db8-123">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-123">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="f7db8-124">유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="f7db8-124">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="f7db8-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="f7db8-125">-Sku</span></span>
<span data-ttu-id="f7db8-126">배포 영역의 새 계층 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-126">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="f7db8-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-127">Valid values are:</span></span>
- <span data-ttu-id="f7db8-128">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="f7db8-128">Developer</span></span>
- <span data-ttu-id="f7db8-129">표준이</span><span class="sxs-lookup"><span data-stu-id="f7db8-129">Standard</span></span>
- <span data-ttu-id="f7db8-130">Premium</span><span class="sxs-lookup"><span data-stu-id="f7db8-130">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7db8-131">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="f7db8-131">-VirtualNetwork</span></span>
<span data-ttu-id="f7db8-132">배포 영역에 대 한 가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-132">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="f7db8-133">$Null를 전달 하면 해당 지역에 대 한 가상 네트워크 구성이 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-133">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="f7db8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7db8-134">CommonParameters</span></span>
<span data-ttu-id="f7db8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7db8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7db8-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f7db8-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7db8-137">입력</span><span class="sxs-lookup"><span data-stu-id="f7db8-137">INPUTS</span></span>

### <span data-ttu-id="f7db8-138">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="f7db8-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="f7db8-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f7db8-139">System.String</span></span>

### <span data-ttu-id="f7db8-140">ApiManagement. PsApiManagementSku/.</span><span class="sxs-lookup"><span data-stu-id="f7db8-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="f7db8-141">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="f7db8-141">System.Int32</span></span>

### <span data-ttu-id="f7db8-142">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="f7db8-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="f7db8-143">출력</span><span class="sxs-lookup"><span data-stu-id="f7db8-143">OUTPUTS</span></span>

### <span data-ttu-id="f7db8-144">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="f7db8-144">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f7db8-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f7db8-145">NOTES</span></span>

## <span data-ttu-id="f7db8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7db8-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7db8-147">추가-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f7db8-147">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="f7db8-148">제거-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="f7db8-148">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="f7db8-149">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="f7db8-149">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
