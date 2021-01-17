---
Module Name: Az.Peering
Module Guid: 6c848b97-4dd4-49ef-b385-43c64905d25a
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.peering.md
Help Version: 0.1.0
Locale: e-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Az.Peering.md
ms.openlocfilehash: 568c235bee84238d53849e8fb9dc3258e907cb18
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491735"
---
# Az.Peering 모듈
## 설명
Microsoft 피어링 서비스를 사용하면 고객과 Microsoft가 Azure에 연결하고 네트워크 리소스를 다른 개체로 ARM 있습니다.

## Az.Peering Cmdlet
### [Get-AzLegacyPeering](Get-AzLegacyPeering.md)
레거시 피어링 리소스를 Azure 리소스 관리(ARM) 리소스로 변환하는 데 사용됩니다. 

### [Get-AzPeerAsn](Get-AzPeerAsn.md)
다음에서 PeerAsn 개체를 ARM.

### [Get-AzPeering](Get-AzPeering.md)
구독에 대한 피어링 리소스를 얻습니다.

### [Get-AzPeeringLocation](Get-AzPeeringLocation.md)
Microsoft에서 제공하는 피어링 위치를 얻습니다.

### [Get-AzPeeringReceivedRoute](Get-AzPeeringReceivedRoute.md)
피어링에 대해 수신된 경로를 나열합니다.

### [Get-AzPeeringRegisteredAsn](Get-AzPeeringRegisteredAsn.md)
인터넷 교환 경로 서버 형식 피어링에 등록된 ASN을 얻습니다.

### [Get-AzPeeringRegisteredPrefix](Get-AzPeeringRegisteredPrefix.md)
피어링에 대해 등록된 Prefix를 얻거나 나열합니다.

### [Get-AzPeeringService](Get-AzPeeringService.md)
단일 개체의 피어링 서비스 개체 목록을 얻습니다.

### [Get-AzPeeringServiceCountry](Get-AzPeeringServiceCountry.md)
피어링 서비스에 사용할 수 있는 국가를 나열합니다.

### [Get-AzPeeringServiceLocation](Get-AzPeeringServiceLocation.md)
Microsoft에서 제공하는 피어링 서비스 위치 목록을 얻습니다.

### [Get-AzPeeringServicePrefix](Get-AzPeeringServicePrefix.md)
구독에 대한 피어링 서비스 Prefix 목록을 얻습니다.

### [Get-AzPeeringServiceProvider](Get-AzPeeringServiceProvider.md)
Microsoft와 파트너 관계에 있는 피어링 서비스 공급자 목록을 얻습니다.

### [New-AzPeerAsn](New-AzPeerAsn.md)
새 피어 ASN을 만듭니다. 

### [New-AzPeerAsnContactDetail](New-AzPeerAsnContactDetail.md)
PeerAsn에 대한 메모리 내 연락처 세부 정보를 만듭니다. 

### [New-AzPeering](New-AzPeering.md)
새 피어링 리소스 ARM 만듭니다.

### [New-AzPeeringDirectConnectionObject](New-AzPeeringDirectConnectionObject.md)
피어링을 만들거나 수정하는 데 사용할 메모리 내 PSObject를 만듭니다.

### [New-AzPeeringExchangeConnectionObject](New-AzPeeringExchangeConnectionObject.md)
피어링을 만들거나 수정하는 데 사용할 메모리 내 PSObject를 만듭니다.

### [New-AzPeeringRegisteredAsn](New-AzPeeringRegisteredAsn.md)
피어링을 위해 등록된 ASN 만들기

### [New-AzPeeringRegisteredPrefix](New-AzPeeringRegisteredPrefix.md)
피어링 개체에 대해 등록된 Prefix를 작성합니다.

### [New-AzPeeringService](New-AzPeeringService.md)
새 피어링 서비스를 만듭니다.

### [New-AzPeeringServicePrefix](New-AzPeeringServicePrefix.md)
새 피어링 서비스 prefix를 만듭니다.

### [Remove-AzPeerAsn](Remove-AzPeerAsn.md)
피어 Asn 제거

### [Remove-AzPeering](Remove-AzPeering.md)
피어링을 삭제하거나 제거합니다. 이렇게 하면 모든 자식 리소스 또는 리소스에 대한 경고가 삭제됩니다.

### [Remove-AzPeeringRegisteredAsn](Remove-AzPeeringRegisteredAsn.md)
부모 피어링 리소스에서 등록된 ASN을 삭제하거나 제거합니다.

### [Remove-AzPeeringRegisteredPrefix](Remove-AzPeeringRegisteredPrefix.md)
부모 피어링 리소스에서 등록된 prefix를 삭제하거나 제거합니다.

### [Remove-AzPeeringServicePrefix](Remove-AzPeeringServicePrefix.md)
새 피어링 서비스 prefix를 제거합니다.

### [Set-AzPeerAsn](Set-AzPeerAsn.md)
연락처 정보 업데이트

### [Set-AzPeeringDirectConnectionObject](Set-AzPeeringDirectConnectionObject.md)
직접 연결 정보를 설정하거나 업데이트합니다. 

### [Set-AzPeeringExchangeConnectionObject](Set-AzPeeringExchangeConnectionObject.md)
Exchange 연결 정보를 설정하거나 업데이트합니다. 

### [Set-AzPeeringRegisteredAsn](Set-AzPeeringRegisteredAsn.md)
부모 피어링 리소스에서 등록된 ASN을 설정하거나 업데이트합니다.

### [Set-AzPeeringRegisteredPrefix](Set-AzPeeringRegisteredPrefix.md)
부모 피어링 리소스에서 등록된 prefix를 설정하거나 업데이트합니다.

### [Update-AzPeering](Update-AzPeering.md)
피어링을 설정합니다. 이 명령을 또는 에 함께 `Set-AzDirectPeeringConnectionObject` 사용 `Set-AzExchangePeeringConnectionObject`

