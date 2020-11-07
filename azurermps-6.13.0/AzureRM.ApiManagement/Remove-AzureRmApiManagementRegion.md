---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 9ccd7379a07b83b3ed45eff5f8095b950868810c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703508"
---
# <span data-ttu-id="a98fe-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a98fe-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="a98fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98fe-102">SYNOPSIS</span></span>
<span data-ttu-id="a98fe-103">PsApiManagement 인스턴스에서 기존 배포 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a98fe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a98fe-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a98fe-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a98fe-105">DESCRIPTION</span></span>
<span data-ttu-id="a98fe-106">**AzureRmApiManagementRegion** Cmdlet은 ApiManagement의 인스턴스를 제공 하 고, **Additionalregions** 컬렉션에서 **PsApiManagementRegion** 형식의 인스턴스를 제거 합니다. **ApiManagement. PsApiManagement** 의 인스턴스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="a98fe-107">이 cmdlet은 배포를 단독으로 수정 하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="a98fe-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 **update-AzureRmApiManagement** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="a98fe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a98fe-109">EXAMPLES</span></span>

### <span data-ttu-id="a98fe-110">예제 1: PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="a98fe-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="a98fe-111">이 명령은 **PsApiManagement** 인스턴스에서 동부 라는 지역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="a98fe-112">예제 2: 일련의 명령을 사용 하 여 PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="a98fe-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="a98fe-113">첫 번째 명령은 ContosoApi 이라는 리소스 그룹에서 **PsApiManagement** 의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="a98fe-114">마지막 명령은 해당 인스턴스에서 동부 라는 지역을 제거 하 고 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="a98fe-115">변수</span><span class="sxs-lookup"><span data-stu-id="a98fe-115">PARAMETERS</span></span>

### <span data-ttu-id="a98fe-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a98fe-116">-ApiManagement</span></span>
<span data-ttu-id="a98fe-117">이 cmdlet가 추가 배포 영역을 제거 하는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="a98fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98fe-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="a98fe-119">-위치</span><span class="sxs-lookup"><span data-stu-id="a98fe-119">-Location</span></span>
<span data-ttu-id="a98fe-120">이 cmdlet이 제거 하는 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="a98fe-121">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="a98fe-122">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="a98fe-122">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="a98fe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98fe-123">CommonParameters</span></span>
<span data-ttu-id="a98fe-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98fe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98fe-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a98fe-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98fe-126">입력</span><span class="sxs-lookup"><span data-stu-id="a98fe-126">INPUTS</span></span>

### <span data-ttu-id="a98fe-127">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="a98fe-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="a98fe-128">매개 변수: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a98fe-128">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="a98fe-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a98fe-129">System.String</span></span>

## <span data-ttu-id="a98fe-130">출력</span><span class="sxs-lookup"><span data-stu-id="a98fe-130">OUTPUTS</span></span>

### <span data-ttu-id="a98fe-131">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="a98fe-131">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a98fe-132">상속자</span><span class="sxs-lookup"><span data-stu-id="a98fe-132">NOTES</span></span>

## <span data-ttu-id="a98fe-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a98fe-133">RELATED LINKS</span></span>

[<span data-ttu-id="a98fe-134">추가-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a98fe-134">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="a98fe-135">업데이트-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a98fe-135">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


