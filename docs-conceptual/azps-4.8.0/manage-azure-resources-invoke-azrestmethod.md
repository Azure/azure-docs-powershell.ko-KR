---
title: Invoke-AzRestMethod를 사용하여 Azure 리소스 관리
description: Azure PowerShell을 사용하여 Invoke-AzRestMethod cmdlet을 사용하여 리소스를 관리하는 방법입니다.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/24/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 55d7cc06178257a9288e2d27f810d1180369ddc4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "92001923"
---
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a><span data-ttu-id="e319e-103">Invoke-AzRestMethod를 사용하여 Azure 리소스 관리</span><span class="sxs-lookup"><span data-stu-id="e319e-103">Manage Azure resources with Invoke-AzRestMethod</span></span>

<span data-ttu-id="e319e-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod)는 Az PowerShell 모듈 버전 4.4.0에 도입된 Azure PowerShell cmdlet입니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-104">[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod) is an Azure PowerShell cmdlet that was introduced in Az PowerShell module version 4.4.0.</span></span> <span data-ttu-id="e319e-105">Az 컨텍스트를 사용하여 ARM(Azure Resource Management) 엔드포인트에 사용자 지정 HTTP 요청을 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-105">It allows you to make custom HTTP requests to the Azure Resource Management (ARM) endpoint using the Az context.</span></span>

<span data-ttu-id="e319e-106">이 cmdlet은 Az PowerShell 모듈에서 아직 사용할 수 없는 기능에 대해 Azure 서비스를 관리하려는 경우에 유용합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-106">This cmdlet is useful when you want to manage Azure services for features that aren't yet available in the Az PowerShell module.</span></span>

## <a name="how-to-use-invoke-azrestmethod"></a><span data-ttu-id="e319e-107">Invoke-AzRestMethod 사용 방법</span><span class="sxs-lookup"><span data-stu-id="e319e-107">How to use Invoke-AzRestMethod</span></span>

<span data-ttu-id="e319e-108">예를 들어, 특정 네트워크에 대해서만 ACR(Azure Container Registry) 액세스를 허용하거나 공용 액세스를 거부할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-108">As an example, you can allow access to Azure Container Registry (ACR) only for specific networks or deny public access.</span></span> <span data-ttu-id="e319e-109">Az PowerShell 모듈 버전 4.5.0부터 이 기능은 [Az.ContainerRegistry PowerShell 모듈](/powershell/module/Az.ContainerRegistry/)에서 아직 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-109">As of Az PowerShell module version 4.5.0, that feature isn't available yet in the [Az.ContainerRegistry PowerShell module](/powershell/module/Az.ContainerRegistry/).</span></span> <span data-ttu-id="e319e-110">그러나 `Invoke-AzRestMethod`를 사용하여 임시로 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-110">However, it can be managed in the interim with `Invoke-AzRestMethod`.</span></span>

## <a name="using-invoke-azrestmethod-with-get-operations"></a><span data-ttu-id="e319e-111">GET 작업으로 Invoke-AzRestMethod 사용</span><span class="sxs-lookup"><span data-stu-id="e319e-111">Using Invoke-AzRestMethod with GET operations</span></span>

<span data-ttu-id="e319e-112">다음 예제에서는 GET 작업으로 `Invoke-AzRestMethod` cmdlet을 사용하는 방법을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-112">The following example demonstrates how to use the `Invoke-AzRestMethod` cmdlet with a GET operation:</span></span>

```azurepowershell-interactive
$getParams = @{
  ResourceGroupName = 'myresourcegroup'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  Name = 'myacr'
  ApiVersion = '2019-12-01-preview'
  Method = 'GET'
}
Invoke-AzRestMethod @getParams
```

<span data-ttu-id="e319e-113">최대의 유연성을 허용하기 위해 `Invoke-AzRestMethod`에 대한 대부분의 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-113">To allow maximum flexibility, most of the parameters for `Invoke-AzRestMethod` are optional.</span></span>
<span data-ttu-id="e319e-114">그러나 리소스 그룹 내에서 리소스를 관리하는 경우 리소스에 전체 ID를 제공하거나 리소스 그룹, 리소스 공급자 및 리소스 유형과 같은 매개 변수를 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-114">However, when you're managing resources within a resource group, you'll most likely need to provide either the full ID to the resource or parameters like resource group, resource provider, and resource type.</span></span>

<span data-ttu-id="e319e-115">둘 이상의 이름이 필요한 리소스를 대상으로 지정하는 경우 `ResourceType` 및 `Name` 매개 변수가 여러 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-115">The `ResourceType` and `Name` parameters can take multiple values when targeting resources that require more than one name.</span></span> <span data-ttu-id="e319e-116">예를 들어 Log Analytics 작업 영역에서 저장된 검색을 조작하기 위해 매개 변수는 `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`와 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-116">For example, to manipulate a saved search in a Log Analytics workspace, the parameters look like the following example: `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`.</span></span>

<span data-ttu-id="e319e-117">cmdlet은 배열의 위치를 기반으로 하는 매핑을 사용하여 `Id:'/workspaces/my-la/savedsearches/my-search'` 리소스를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-117">Using a mapping based on the position in the array, the cmdlet constructs the following resource: `Id:'/workspaces/my-la/savedsearches/my-search'`.</span></span>

<span data-ttu-id="e319e-118">`APIVersion` 매개 변수를 사용하면 미리 보기 버전을 포함하여 특정 API 버전을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-118">The `APIVersion` parameter allows you to use a specific API version, including preview ones.</span></span> <span data-ttu-id="e319e-119">Azure 리소스 공급자에 대해 지원되는 API 버전은 [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub 리포지토리에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-119">The supported API versions for Azure Resource providers can be found in the [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub repository.</span></span>

<span data-ttu-id="e319e-120">ACR의 2019-12-01 미리 보기 버전에 대한 정의는 [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-120">You can find the definition for the 2019-12-01-preview version of ACR in the following location: [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview).</span></span>

## <a name="using-invoke-azrestmethod-with-patch-operations"></a><span data-ttu-id="e319e-121">PATCH 작업과 함께 Invoke-AzRestMethod 사용</span><span class="sxs-lookup"><span data-stu-id="e319e-121">Using Invoke-AzRestMethod with PATCH operations</span></span>

<span data-ttu-id="e319e-122">`Invoke-AzRestMethod` cmdlet을 사용하여 `myresourcegroup` 리소스 그룹에서 `myacr`이라는 기존 ACR에 대한 공용 액세스를 사용하지 않도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-122">You can disable public access to the existing ACR named `myacr` in the `myresourcegroup` resource group using the `Invoke-AzRestMethod` cmdlet.</span></span>

<span data-ttu-id="e319e-123">공용 네트워크 액세스를 사용하지 않도록 설정하려면 다음 예와 같이 `publicNetwokAccess` 매개 변수의 값을 변경하는 API에 **PATCH** 호출을 수행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-123">To disable the public network access, you need to make a **PATCH** call to the API that changes the value of the `publicNetwokAccess` parameter as shown in the following example:</span></span>

```azurepowershell-interactive
$patchParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
     "publicNetworkAccess": "Disabled"
     } }'
  Method = 'PATCH'
}
Invoke-AzRestMethod @patchParams
```

<span data-ttu-id="e319e-124">`Payload` 속성은 수정할 속성의 경로를 표시하는 JSON 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-124">The `Payload` property is a JSON string that shows the path of the property to be modified.</span></span>

<span data-ttu-id="e319e-125">이 API에 대한 모든 매개 변수는 이 API와 연관된 **rest-api-spec** 파일에 설명되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-125">All the parameters for this API are described in the **rest-api-spec** file associated with this API.</span></span>
<span data-ttu-id="e319e-126">publicNetworkAccess 매개 변수에 대한 특정 정의는 API의 2019-12-01 미리 보기 버전의 [ 컨테이너 레지스트리 JSON 파일](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json)에서 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-126">The specific definition for the publicNetworkAccess parameter can be found in the [container registry JSON file](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json) for the 2019-12-01 preview version of the API.</span></span>

<span data-ttu-id="e319e-127">특정 IP 주소에서 레지스트리에 대한 액세스만 허용하려면 다음 예와 같이 페이로드를 수정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-127">To only allow access to the registry from a specific IP address, the payload needs to be modified as shown in the following example:</span></span>

```azurepowershell-interactive
$specificIpParams = @{
  ResourceGroupName = 'myresourcegroup'
  Name = 'myacr'
  ResourceProviderName = 'Microsoft.ContainerRegistry'
  ResourceType = 'registries'
  ApiVersion = '2019-12-01-preview'
  Payload = '{ "properties": {
      "networkRuleSet": {
      "defaultAction": "Deny",
      "ipRules": [ {
         "action": "Allow",
         "value": "24.22.123.123"
         } ]
      }
  } }'
  -Method = 'PATCH'
}
Invoke-AzRestMethod @specificIpParams
```

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a><span data-ttu-id="e319e-128">Get-AzResource, New-AzResource 및 Remove-AzResource의 비교</span><span class="sxs-lookup"><span data-stu-id="e319e-128">Comparison to Get-AzResource, New-AzResource, and Remove-AzResource</span></span>

<span data-ttu-id="e319e-129">`*-AzResource` cmdlet을 사용하면 리소스 유형, API 버전 및 업데이트할 속성을 지정하여 Azure에 대한 REST API 호출을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-129">The `*-AzResource` cmdlets allow you to customize the REST API call to Azure by specifying the resource type, the API version, and the properties to be updated.</span></span> <span data-ttu-id="e319e-130">하지만 먼저 속성을 `PSObject`로 만들어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-130">However, the properties need to be created first as a `PSObject`.</span></span> <span data-ttu-id="e319e-131">이 프로세스를 통해 복잡성 수준을 더 추가하고 쉽게 복잡해질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-131">This process adds an additional level of complexity and can easily become complicated.</span></span>

<span data-ttu-id="e319e-132">`Invoke-AzRestMethod`는 Azure 리소스를 보다 간편하게 관리할 수 있는 방법을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-132">`Invoke-AzRestMethod` offers a simple way to manage Azure resources.</span></span> <span data-ttu-id="e319e-133">이전 예제와 같이, JSON 문자열을 빌드하고 이 문자열을 사용하면 `PSObjects`를 미리 만들지 않고도 REST API 호출을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-133">As shown in the previous example, you can build a JSON string and use it to customize the REST API call without having to precreate any `PSObjects`.</span></span>

<span data-ttu-id="e319e-134">`*-AzResource` cmdlet에 대해 이미 잘 알고 있는 경우 계속 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-134">If you're already familiar with the `*-AzResource` cmdlets, you can continue using them.</span></span> <span data-ttu-id="e319e-135">지원을 중지할 계획은 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-135">We have no plans to stop supporting them.</span></span> <span data-ttu-id="e319e-136">`Invoke-AzRestMethod`를 사용하여 새 cmdlet을 도구 키트에 추가했습니다.</span><span class="sxs-lookup"><span data-stu-id="e319e-136">With `Invoke-AzRestMethod`, we have added a new cmdlet to your toolkit.</span></span>

## <a name="see-also"></a><span data-ttu-id="e319e-137">관련 항목</span><span class="sxs-lookup"><span data-stu-id="e319e-137">See Also</span></span>

* [<span data-ttu-id="e319e-138">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e319e-138">Get-AzResource</span></span>](/powershell/module/az.resources/get-azresource)
* [<span data-ttu-id="e319e-139">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e319e-139">New-AzResource</span></span>](/powershell/module/az.resources/new-azresource)
* [<span data-ttu-id="e319e-140">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="e319e-140">Remove-AzResource</span></span>](/powershell/module/az.resources/remove-azresource)
