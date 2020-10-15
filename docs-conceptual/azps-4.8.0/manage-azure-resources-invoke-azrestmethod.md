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
# <a name="manage-azure-resources-with-invoke-azrestmethod"></a>Invoke-AzRestMethod를 사용하여 Azure 리소스 관리

[Invoke-AzRestMethod](/powershell/module/az.accounts/invoke-azrestmethod)는 Az PowerShell 모듈 버전 4.4.0에 도입된 Azure PowerShell cmdlet입니다. Az 컨텍스트를 사용하여 ARM(Azure Resource Management) 엔드포인트에 사용자 지정 HTTP 요청을 할 수 있습니다.

이 cmdlet은 Az PowerShell 모듈에서 아직 사용할 수 없는 기능에 대해 Azure 서비스를 관리하려는 경우에 유용합니다.

## <a name="how-to-use-invoke-azrestmethod"></a>Invoke-AzRestMethod 사용 방법

예를 들어, 특정 네트워크에 대해서만 ACR(Azure Container Registry) 액세스를 허용하거나 공용 액세스를 거부할 수 있습니다. Az PowerShell 모듈 버전 4.5.0부터 이 기능은 [Az.ContainerRegistry PowerShell 모듈](/powershell/module/Az.ContainerRegistry/)에서 아직 사용할 수 없습니다. 그러나 `Invoke-AzRestMethod`를 사용하여 임시로 관리할 수 있습니다.

## <a name="using-invoke-azrestmethod-with-get-operations"></a>GET 작업으로 Invoke-AzRestMethod 사용

다음 예제에서는 GET 작업으로 `Invoke-AzRestMethod` cmdlet을 사용하는 방법을 보여 줍니다.

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

최대의 유연성을 허용하기 위해 `Invoke-AzRestMethod`에 대한 대부분의 매개 변수는 선택 사항입니다.
그러나 리소스 그룹 내에서 리소스를 관리하는 경우 리소스에 전체 ID를 제공하거나 리소스 그룹, 리소스 공급자 및 리소스 유형과 같은 매개 변수를 제공해야 합니다.

둘 이상의 이름이 필요한 리소스를 대상으로 지정하는 경우 `ResourceType` 및 `Name` 매개 변수가 여러 값을 사용할 수 있습니다. 예를 들어 Log Analytics 작업 영역에서 저장된 검색을 조작하기 위해 매개 변수는 `-ResourceType @('workspaces', 'savedsearches') -Name @('my-la', 'my-search')`와 같습니다.

cmdlet은 배열의 위치를 기반으로 하는 매핑을 사용하여 `Id:'/workspaces/my-la/savedsearches/my-search'` 리소스를 구성합니다.

`APIVersion` 매개 변수를 사용하면 미리 보기 버전을 포함하여 특정 API 버전을 사용할 수 있습니다. Azure 리소스 공급자에 대해 지원되는 API 버전은 [azure-rest-api-specs](https://github.com/Azure/azure-rest-api-specs) GitHub 리포지토리에서 찾을 수 있습니다.

ACR의 2019-12-01 미리 보기 버전에 대한 정의는 [azure-rest-api-specs/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/](https://github.com/Azure/azure-rest-api-specs/tree/master/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview)에서 찾을 수 있습니다.

## <a name="using-invoke-azrestmethod-with-patch-operations"></a>PATCH 작업과 함께 Invoke-AzRestMethod 사용

`Invoke-AzRestMethod` cmdlet을 사용하여 `myresourcegroup` 리소스 그룹에서 `myacr`이라는 기존 ACR에 대한 공용 액세스를 사용하지 않도록 설정할 수 있습니다.

공용 네트워크 액세스를 사용하지 않도록 설정하려면 다음 예와 같이 `publicNetwokAccess` 매개 변수의 값을 변경하는 API에 **PATCH** 호출을 수행해야 합니다.

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

`Payload` 속성은 수정할 속성의 경로를 표시하는 JSON 문자열입니다.

이 API에 대한 모든 매개 변수는 이 API와 연관된 **rest-api-spec** 파일에 설명되어 있습니다.
publicNetworkAccess 매개 변수에 대한 특정 정의는 API의 2019-12-01 미리 보기 버전의 [ 컨테이너 레지스트리 JSON 파일](https://github.com/Azure/azure-rest-api-specs/blob/2a9da9a79d0a7b74089567ec4f0289f3e0f31bec/specification/containerregistry/resource-manager/Microsoft.ContainerRegistry/preview/2019-12-01-preview/containerregistry.json)에서 찾을 수 있습니다.

특정 IP 주소에서 레지스트리에 대한 액세스만 허용하려면 다음 예와 같이 페이로드를 수정해야 합니다.

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

## <a name="comparison-to-get-azresource-new-azresource-and-remove-azresource"></a>Get-AzResource, New-AzResource 및 Remove-AzResource의 비교

`*-AzResource` cmdlet을 사용하면 리소스 유형, API 버전 및 업데이트할 속성을 지정하여 Azure에 대한 REST API 호출을 사용자 지정할 수 있습니다. 하지만 먼저 속성을 `PSObject`로 만들어야 합니다. 이 프로세스를 통해 복잡성 수준을 더 추가하고 쉽게 복잡해질 수 있습니다.

`Invoke-AzRestMethod`는 Azure 리소스를 보다 간편하게 관리할 수 있는 방법을 제공합니다. 이전 예제와 같이, JSON 문자열을 빌드하고 이 문자열을 사용하면 `PSObjects`를 미리 만들지 않고도 REST API 호출을 사용자 지정할 수 있습니다.

`*-AzResource` cmdlet에 대해 이미 잘 알고 있는 경우 계속 사용할 수 있습니다. 지원을 중지할 계획은 없습니다. `Invoke-AzRestMethod`를 사용하여 새 cmdlet을 도구 키트에 추가했습니다.

## <a name="see-also"></a>관련 항목

* [Get-AzResource](/powershell/module/az.resources/get-azresource)
* [New-AzResource](/powershell/module/az.resources/new-azresource)
* [Remove-AzResource](/powershell/module/az.resources/remove-azresource)
