---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: b35ba1bcd976bbc563dd8e3ad6640279a5a8a1dd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963627"
---
# Az.ServiceFabric 모듈
## 설명
보안 클러스터 만들기, 클러스터 인증서 롤오프, 클러스터에서 노드 추가 또는 제거 등의 엔드-2 엔드 작업을 자동화하는 데 사용할 수 있는 Azure Service Fabric 모듈 모든 작업의 전체 목록은 아래에 나열되어 있습니다.

## Az.ServiceFabric Cmdlet
### [Add-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
클라이언트 인증을 위해 클러스터에 일반적인 이름 또는 지문을 추가합니다.

### [Add-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
클러스터에 보조 클러스터 인증서를 추가합니다.

### [Add-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
클러스터에 인증서 일반 이름 또는 지문을 추가합니다. 이렇게 하면 클라이언트 인증을 위해 클러스터가 다시 인증서를 등록합니다.

### [Add-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
노드 유형에 vm 확장을 추가합니다.

### [Add-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
노드 유형에 인증서 비밀을 추가합니다.

### [Add-AzServiceFabricNode](Add-AzServiceFabricNode.md)
클러스터의 특정 노드 유형에 노드를 추가합니다.

### [Add-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
기존 클러스터에 새 노드 형식을 추가합니다.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
Service Fabric 애플리케이션 세부 정보를 얻습니다.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
Service Fabric 애플리케이션 유형 세부 정보를 얻습니다.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
Service Fabric 애플리케이션 유형 버전 세부 정보를 얻습니다.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
클러스터 리소스 세부 정보를 얻습니다.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
관리되는 클러스터 리소스 세부 정보를 얻습니다.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
관리되는 노드 형식 리소스 세부 정보를 얻습니다.

### [Get-AzServiceFabricServicService](Get-AzServiceFabricService.md)
지정된 애플리케이션 및 클러스터에서 Service Fabric 서비스 세부 정보를 얻습니다.

### [New-AzServiceFabricApplication](New-AzServiceFabricApplication.md)
지정된 리소스 그룹 및 클러스터에서 새 서비스 패브릭 애플리케이션을 만들 수 있습니다.

### [New-AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
지정된 리소스 그룹 및 클러스터 아래에서 새 서비스 패브릭 애플리케이션 유형을 생성합니다.

### [New-AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
지정된 리소스 그룹 및 클러스터 아래에서 새 애플리케이션 형식 버전을 만드면 됩니다.

### [New-AzServiceFabricCluster](New-AzServiceFabricCluster.md)
이 명령은 사용자가 제공하는 인증서 또는 시스템이 생성한 자체 서명된 인증서를 사용하여 새 서비스 패브릭 클러스터를 설정합니다. 기본 템플릿 또는 사용자가 제공하는 사용자 지정 템플릿을 사용할 수 있습니다. 자체 서명된 인증서를 내보낼 폴더를 지정하거나 나중에 키 자격 증명 모음에서 해당 인증서를 인출할 수 있습니다.

### [New-AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
새 관리되는 클러스터를 만들 수 있습니다.

### [New-AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
새 노드 형식 리소스를 생성합니다.

### [New-AzServiceFabricService](New-AzServiceFabricService.md)
지정된 애플리케이션 및 클러스터에서 새 서비스 패브릭 서비스를 만들 수 있습니다.

### [Remove-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
클러스터에서 애플리케이션을 제거합니다. 이렇게 하면 애플리케이션에서 모든 서비스가 제거됩니다.

### [Remove-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
클러스터에서 Service 패브릭 애플리케이션 유형을 제거합니다. 이렇게 하면 이 리소스의 모든 형식 버전이 제거됩니다.

### [Remove-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
클러스터에서 Service 패브릭 애플리케이션 형식 버전을 제거합니다.

### [Remove-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
클러스터에 대한 클라이언트 인증에 사용되는 클라이언트 인증서 또는 인증서 주체 이름에서 제거합니다.

### [Remove-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
클러스터 보안에 사용되는 클러스터 인증서를 제거합니다.

### [Remove-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
클러스터 리소스를 제거합니다.

### [Remove-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
지문 또는 일반적인 이름으로 클라이언트 인증서를 Remvoe합니다.

### [Remove-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
노드 유형 내에서 노드 유형 또는 특정 노드를 제거합니다.

### [Remove-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
노드 형식에서 vm 확장을 제거합니다.

### [Remove-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
클러스터에서 특정 노드 유형에서 노드를 제거합니다.

### [Remove-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
클러스터에서 전체 노드 유형을 제거합니다.

### [Remove-AzServiceFabricServicService](Remove-AzServiceFabricService.md)
클러스터에서 서비스를 제거합니다.

### [Remove-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
클러스터에서 하나 또는 여러 Service Fabric 설정을 제거합니다.

### [Restart-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
노드 형식에서 특정 노드를 다시 시작합니다.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
클러스터 리소스 속성을 설정합니다.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
-Reimage 매개 변수를 사용하여 노드 형식 리소스 속성을 설정하거나 노드 형식의 특정 ndes에서 리미지 작업을 실행합니다.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
클러스터에 하나 또는 여러 Service Fabric 설정을 추가하거나 업데이트합니다.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
클러스터의 Service Fabric 업그레이드 유형을 변경합니다.

### [Update-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
서비스 패브릭 애플리케이션을 업데이트합니다. 이렇게 하면 애플리케이션 매개 변수를 업데이트하고/또는 애플리케이션 업그레이드를 트리거하는 애플리케이션 형식 버전을 업그레이드할 수 있습니다.

### [Update-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
클러스터의 노드 형식의 내구성 계층 또는 VmSku를 업데이트합니다.

### [Update-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
클러스터의 기본 노드 형식의 안정성 계층을 업데이트합니다.

