---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 17D7EBD2-FE3F-4D24-A1AA-8C45B9B1FEF5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementRegion.md
ms.openlocfilehash: 2e6ae18054f7ad3e122169522d111adfe612b955
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010048"
---
# <span data-ttu-id="e7792-101">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e7792-101">Remove-AzApiManagementRegion</span></span>

## <span data-ttu-id="e7792-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7792-102">SYNOPSIS</span></span>
<span data-ttu-id="e7792-103">PsApiManagement 인스턴스에서 기존 배포 지역을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-103">Removes an existing deployment region from PsApiManagement instance.</span></span>

## <span data-ttu-id="e7792-104">구문</span><span class="sxs-lookup"><span data-stu-id="e7792-104">SYNTAX</span></span>

```
Remove-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e7792-105">설명</span><span class="sxs-lookup"><span data-stu-id="e7792-105">DESCRIPTION</span></span>
<span data-ttu-id="e7792-106">**Remove-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** 형식의 인스턴스를 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement의** 추가Region 컬렉션에서 제거합니다. </span><span class="sxs-lookup"><span data-stu-id="e7792-106">The **Remove-AzApiManagementRegion** cmdlet removes instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** from a collection of **AdditionalRegions** of provided the instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="e7792-107">이 cmdlet은 배포 자체를 수정하지 않고 메모리 내 **PsApiManagement 인스턴스를** 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-107">This cmdlet does not modify deployment by itself but updates the instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="e7792-108">API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagementInstance를** **Set-AzApiManagement** 에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-108">To update a deployment of an API Management, pass the modified **PsApiManagementInstance** to **Set-AzApiManagement**.</span></span>

## <span data-ttu-id="e7792-109">예제</span><span class="sxs-lookup"><span data-stu-id="e7792-109">EXAMPLES</span></span>

### <span data-ttu-id="e7792-110">예제 1: PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="e7792-110">Example 1: Remove a region from a PsApiManagement instance</span></span>
```
PS C:\>Remove-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US"
```

<span data-ttu-id="e7792-111">이 명령은 **PsApiManagement** 인스턴스에서 미국 동부라는 지역을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-111">This command removes the region named East US from the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="e7792-112">예제 2: 일련의 명령을 사용하여 PsApiManagement 인스턴스에서 지역 제거</span><span class="sxs-lookup"><span data-stu-id="e7792-112">Example 2: Remove a region from a PsApiManagement instance using a series of commands</span></span>
```
PS C:\>Get-AzApiManagement -ResourceGroupName "Contoso" -Name ContosoApi | Remove-AzApiManagementRegion -Location "East US" | Set-AzApiManagement
```

<span data-ttu-id="e7792-113">이 첫 번째 명령은 ContosoApi라는 Contoso라는 리소스 그룹에서 **PsApiManagement의** 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-113">This first command gets an instance of **PsApiManagement** from the resource group named Contoso named ContosoApi.</span></span>
<span data-ttu-id="e7792-114">그런 다음 최종 명령은 해당 인스턴스에서 미국 동부라는 지역을 제거한 다음 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-114">The final command then removes the region named East US from that instance then updates the deployment.</span></span>

## <span data-ttu-id="e7792-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7792-115">PARAMETERS</span></span>

### <span data-ttu-id="e7792-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e7792-116">-ApiManagement</span></span>
<span data-ttu-id="e7792-117">이 cmdlet에서 추가 배포 지역을 제거하는 **PsApiManagement** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-117">Specifies the **PsApiManagement** instance that this cmdlet removes the additional deployment region from.</span></span>

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

### <span data-ttu-id="e7792-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7792-118">-DefaultProfile</span></span>

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

### <span data-ttu-id="e7792-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e7792-119">-Location</span></span>
<span data-ttu-id="e7792-120">이 cmdlet이 제거한 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-120">Specifies the location of the region that this cmdlet removes.</span></span>
<span data-ttu-id="e7792-121">Api Management 서비스에 대해 지원되는 지역 사이에 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-121">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="e7792-122">유효한 위치를 얻게 Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | 여기서 {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="e7792-122">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="e7792-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7792-123">CommonParameters</span></span>
<span data-ttu-id="e7792-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e7792-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7792-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e7792-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7792-126">입력</span><span class="sxs-lookup"><span data-stu-id="e7792-126">INPUTS</span></span>

### <span data-ttu-id="e7792-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e7792-127">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="e7792-128">System.String</span><span class="sxs-lookup"><span data-stu-id="e7792-128">System.String</span></span>

## <span data-ttu-id="e7792-129">출력</span><span class="sxs-lookup"><span data-stu-id="e7792-129">OUTPUTS</span></span>

### <span data-ttu-id="e7792-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e7792-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e7792-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e7792-131">NOTES</span></span>

## <span data-ttu-id="e7792-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7792-132">RELATED LINKS</span></span>

[<span data-ttu-id="e7792-133">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e7792-133">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="e7792-134">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="e7792-134">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)


