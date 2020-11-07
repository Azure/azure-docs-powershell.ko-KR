---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 7dd38e0336cc6850345f8e21a81c857eec309b0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869401"
---
# <span data-ttu-id="0abac-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0abac-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="0abac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0abac-102">SYNOPSIS</span></span>
<span data-ttu-id="0abac-103">PsApiManagement 인스턴스에서 기존 배포 영역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="0abac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0abac-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0abac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0abac-105">DESCRIPTION</span></span>
<span data-ttu-id="0abac-106">**AzApiManagementRegion** Cmdlet은 ApiManagement의 인스턴스를 제공 하 고, **Additionalregions** 컬렉션에서 **PsApiManagementRegion** 형식의 인스턴스를 제거 합니다. **ApiManagement. PsApiManagement** 의 인스턴스가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="0abac-107">이 cmdlet은 배포를 단독으로 수정 하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="0abac-108">API Management의 배포를 업데이트 하려면 수정 된 **PsApiManagementInstance** 를 **update-AzApiManagement** 에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Update-AzApiManagement**.</span></span>

## <span data-ttu-id="0abac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0abac-109">EXAMPLES</span></span>

### <span data-ttu-id="0abac-110">예제 1: PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="0abac-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="0abac-111">이 명령은 **PsApiManagement** 인스턴스에서 동부 라는 지역을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="0abac-112">예제 2: 일련의 명령을 사용 하 여 PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="0abac-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Update-AzApiManagementDeployment
```

<span data-ttu-id="0abac-113">첫 번째 명령은 ContosoApi 이라는 리소스 그룹에서 **PsApiManagement** 의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="0abac-114">마지막 명령은 해당 인스턴스에서 동부 라는 지역을 제거 하 고 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="0abac-115">변수</span><span class="sxs-lookup"><span data-stu-id="0abac-115">PARAMETERS</span></span>

### <span data-ttu-id="0abac-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="0abac-116">-ApiManagement</span></span>
<span data-ttu-id="0abac-117">이 cmdlet가 추가 배포 영역을 제거 하는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="0abac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0abac-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="0abac-119">-위치</span><span class="sxs-lookup"><span data-stu-id="0abac-119">-Location</span></span>
<span data-ttu-id="0abac-120">이 cmdlet이 제거 하는 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="0abac-121">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="0abac-122">유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="0abac-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="0abac-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0abac-123">CommonParameters</span></span>
<span data-ttu-id="0abac-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0abac-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0abac-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0abac-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0abac-126">입력</span><span class="sxs-lookup"><span data-stu-id="0abac-126">INPUTS</span></span>

### <span data-ttu-id="0abac-127">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="0abac-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="0abac-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0abac-128">System.String</span></span>

## <span data-ttu-id="0abac-129">출력</span><span class="sxs-lookup"><span data-stu-id="0abac-129">OUTPUTS</span></span>

### <span data-ttu-id="0abac-130">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="0abac-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="0abac-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0abac-131">NOTES</span></span>

## <span data-ttu-id="0abac-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0abac-132">RELATED LINKS</span></span>

[<span data-ttu-id="0abac-133">추가-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0abac-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="0abac-134">업데이트-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="0abac-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


