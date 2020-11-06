---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8bacb26b4e30521ddd840d2a8081365ed9c4c6ad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525759"
---
# <span data-ttu-id="84e3b-101">Remove-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="84e3b-101">Remove-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="84e3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84e3b-102">SYNOPSIS</span></span>
<span data-ttu-id="84e3b-103">PsApiManagement 인스턴스에서 기존 배포 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84e3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84e3b-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="84e3b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84e3b-105">DESCRIPTION</span></span>
<span data-ttu-id="84e3b-106">**AzureRmApiManagementRegion** Cmdlet은 ApiManagement의 인스턴스를 제공 하 고, **Additionalregions** 컬렉션에서 **PsApiManagementRegion** 형식의 인스턴스를 제거 합니다. **ApiManagement. PsApiManagement** 의 인스턴스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-106">The **Remove-AzureRmApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="84e3b-107">이 cmdlet은 배포를 단독으로 수정 하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="84e3b-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 **update-AzureRmApiManagement** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzureRmApiManagement**.</span></span>

## <span data-ttu-id="84e3b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="84e3b-109">EXAMPLES</span></span>

### <span data-ttu-id="84e3b-110">예제 1: PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="84e3b-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzureRmApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="84e3b-111">이 명령은 **PsApiManagement** 인스턴스에서 동부 라는 지역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="84e3b-112">예제 2: 일련의 명령을 사용 하 여 PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="84e3b-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzureRmApiManagementRegion -Location "East US" | Update-AzureRmApiManagementDeployment
```

<span data-ttu-id="84e3b-113">첫 번째 명령은 ContosoApi 이라는 리소스 그룹에서 **PsApiManagement** 의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="84e3b-114">마지막 명령은 해당 인스턴스에서 동부 라는 지역을 제거 하 고 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="84e3b-115">변수</span><span class="sxs-lookup"><span data-stu-id="84e3b-115">PARAMETERS</span></span>

### <span data-ttu-id="84e3b-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="84e3b-116">-ApiManagement</span></span>
<span data-ttu-id="84e3b-117">이 cmdlet가 추가 배포 영역을 제거 하는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="84e3b-118">-위치</span><span class="sxs-lookup"><span data-stu-id="84e3b-118">-Location</span></span>
<span data-ttu-id="84e3b-119">이 cmdlet이 제거 하는 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-119">Specifies the location of the region that this cmdlet removes.</span></span>

<span data-ttu-id="84e3b-120">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-120">Valid values are:</span></span> 

- <span data-ttu-id="84e3b-121">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="84e3b-121">North Central US</span></span>
- <span data-ttu-id="84e3b-122">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="84e3b-122">South Central US</span></span>
- <span data-ttu-id="84e3b-123">중부 US</span><span class="sxs-lookup"><span data-stu-id="84e3b-123">Central US</span></span>
- <span data-ttu-id="84e3b-124">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="84e3b-124">West Europe</span></span>
- <span data-ttu-id="84e3b-125">동유럽</span><span class="sxs-lookup"><span data-stu-id="84e3b-125">North Europe</span></span>
- <span data-ttu-id="84e3b-126">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="84e3b-126">West US</span></span>
- <span data-ttu-id="84e3b-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="84e3b-127">East US</span></span>
- <span data-ttu-id="84e3b-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="84e3b-128">East US 2</span></span>
- <span data-ttu-id="84e3b-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="84e3b-129">Japan East</span></span>
- <span data-ttu-id="84e3b-130">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="84e3b-130">Japan West</span></span>
- <span data-ttu-id="84e3b-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="84e3b-131">Brazil South</span></span>
- <span data-ttu-id="84e3b-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="84e3b-132">Southeast Asia</span></span>
- <span data-ttu-id="84e3b-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="84e3b-133">East Asia</span></span>
- <span data-ttu-id="84e3b-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="84e3b-134">Australia East</span></span>
- <span data-ttu-id="84e3b-135">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="84e3b-135">Australia Southeast</span></span>

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

### <span data-ttu-id="84e3b-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84e3b-136">-DefaultProfile</span></span>
<span data-ttu-id="84e3b-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84e3b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84e3b-138">CommonParameters</span></span>
<span data-ttu-id="84e3b-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84e3b-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84e3b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84e3b-141">입력</span><span class="sxs-lookup"><span data-stu-id="84e3b-141">INPUTS</span></span>

### <span data-ttu-id="84e3b-142">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="84e3b-142">PsApiManagement</span></span>
<span data-ttu-id="84e3b-143">' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84e3b-143">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="84e3b-144">출력</span><span class="sxs-lookup"><span data-stu-id="84e3b-144">OUTPUTS</span></span>

### <span data-ttu-id="84e3b-145">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="84e3b-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="84e3b-146">상속자</span><span class="sxs-lookup"><span data-stu-id="84e3b-146">NOTES</span></span>

## <span data-ttu-id="84e3b-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84e3b-147">RELATED LINKS</span></span>

[<span data-ttu-id="84e3b-148">추가-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="84e3b-148">Add-AzureRmApiManagementRegion</span></span>](./Add-AzureRmApiManagementRegion.md)

[<span data-ttu-id="84e3b-149">업데이트-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="84e3b-149">Update-AzureRmApiManagementRegion</span></span>](./Update-AzureRmApiManagementRegion.md)


