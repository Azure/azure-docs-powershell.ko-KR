---
Module Name: Az.ServiceFabric
Module Guid: 60f3ba88-443f-46ff-88a3-318cfd11c1da
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.servicefabric
Help Version: 0.3.4.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceFabric/ServiceFabric/help/Az.ServiceFabric.md
ms.openlocfilehash: 6c58f25209a0acd227e2f04e7ca808916f283d46
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94057002"
---
# Az ServiceFabric 모듈
## 설명은
보안 클러스터 만들기, 클러스터 인증서를 통해 롤링, 클러스터에서 노드 추가 또는 제거 등의 엔드-2-엔드 작업을 자동화 하는 데 사용할 수 있는 Azure Service Fabric 모듈입니다. 모든 작업의 전체 목록은 아래에 나열 되어 있습니다.

## Az ServiceFabric Cmdlet
### [추가-AzServiceFabricClientCertificate](Add-AzServiceFabricClientCertificate.md)
클라이언트 인증을 위해 클러스터에 일반 이름 또는 지문을 추가 합니다.

### [추가-AzServiceFabricClusterCertificate](Add-AzServiceFabricClusterCertificate.md)
클러스터에 보조 클러스터 인증서를 추가 합니다.

### [추가-AzServiceFabricManagedClusterClientCertificate](Add-AzServiceFabricManagedClusterClientCertificate.md)
인증서 일반 이름 또는 지문을 클러스터에 추가 합니다. 이렇게 하면 클라이언트 인증을 위해 agains 인증서가 클러스터에 등록 됩니다.

### [추가-AzServiceFabricManagedNodeTypeVMExtension](Add-AzServiceFabricManagedNodeTypeVMExtension.md)
노드 형식에 vm 확장을 추가 합니다.

### [추가-AzServiceFabricManagedNodeTypeVMSecret](Add-AzServiceFabricManagedNodeTypeVMSecret.md)
노드 형식에 인증서 비밀을 추가 합니다.

### [추가-AzServiceFabricNode](Add-AzServiceFabricNode.md)
클러스터의 특정 노드 형식에 노드를 추가 합니다.

### [추가-AzServiceFabricNodeType](Add-AzServiceFabricNodeType.md)
기존 클러스터에 새 노드 형식을 추가 합니다.

### [Get-AzServiceFabricApplication](Get-AzServiceFabricApplication.md)
서비스 패브릭 응용 프로그램 세부 정보를 가져옵니다.

### [Get-AzServiceFabricApplicationType](Get-AzServiceFabricApplicationType.md)
서비스 패브릭 응용 프로그램 유형 세부 정보를 가져옵니다.

### [Get-AzServiceFabricApplicationTypeVersion](Get-AzServiceFabricApplicationTypeVersion.md)
서비스 패브릭 응용 프로그램 유형 버전 세부 정보를 가져옵니다.

### [Get-AzServiceFabricCluster](Get-AzServiceFabricCluster.md)
클러스터 리소스 세부 정보를 가져옵니다.

### [Get-AzServiceFabricManagedCluster](Get-AzServiceFabricManagedCluster.md)
관리 되는 클러스터 리소스 세부 정보를 가져옵니다.

### [Get-AzServiceFabricManagedNodeType](Get-AzServiceFabricManagedNodeType.md)
관리 노드 형식 리소스 세부 정보를 가져옵니다.

### [Get-AzServiceFabricService](Get-AzServiceFabricService.md)
지정 된 응용 프로그램 및 클러스터 아래에서 서비스 패브릭 서비스 세부 정보를 가져옵니다.

### [새로운 AzServiceFabricApplication](New-AzServiceFabricApplication.md)
지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램을 만듭니다.

### [새로운 AzServiceFabricApplicationType](New-AzServiceFabricApplicationType.md)
지정 된 리소스 그룹 및 클러스터 아래에 새 service fabric 응용 프로그램 종류를 만듭니다.

### [새로운 AzServiceFabricApplicationTypeVersion](New-AzServiceFabricApplicationTypeVersion.md)
지정 된 리소스 그룹 및 클러스터 아래에 새 응용 프로그램 종류 버전을 만듭니다.

### [새로운 AzServiceFabricCluster](New-AzServiceFabricCluster.md)
이 명령은 사용자가 제공 하는 인증서를 사용 하거나, 시스템에서 자체 서명 된 인증서를 생성 하 여 새 서비스 패브릭 클러스터를 설정 합니다. 제공 하는 기본 서식 파일 또는 사용자 지정 서식 파일을 사용할 수 있습니다. 자체 서명 된 인증서를 내보낼 폴더를 지정 하거나 나중에 키 자격 증명 모음에서 반입할 수 있는 옵션이 있습니다.

### [새로운 AzServiceFabricManagedCluster](New-AzServiceFabricManagedCluster.md)
새 관리 되는 클러스터를 만듭니다.

### [새로운 AzServiceFabricManagedNodeType](New-AzServiceFabricManagedNodeType.md)
새 노드 형식 리소스를 만듭니다.

### [새로운 AzServiceFabricService](New-AzServiceFabricService.md)
지정 된 응용 프로그램 및 클러스터 아래에 새 service fabric 서비스를 만듭니다.

### [제거-AzServiceFabricApplication](Remove-AzServiceFabricApplication.md)
클러스터에서 응용 프로그램을 제거 합니다. 이렇게 하면 응용 프로그램 아래에 있는 서비스가 모두 제거 됩니다.

### [제거-AzServiceFabricApplicationType](Remove-AzServiceFabricApplicationType.md)
서비스 패브릭 제거 클러스터의 응용 프로그램 유형입니다. 이 리소스 아래에 모든 유형의 버전이 제거 됩니다.

### [제거-AzServiceFabricApplicationTypeVersion](Remove-AzServiceFabricApplicationTypeVersion.md)
서비스 패브릭 제거 클러스터의 응용 프로그램 유형 버전입니다.

### [제거-AzServiceFabricClientCertificate](Remove-AzServiceFabricClientCertificate.md)
클라이언트 인증에 사용 되지 않는 클라이언트 인증서 또는 인증서 주체 이름 (s)을 제거 합니다.

### [제거-AzServiceFabricClusterCertificate](Remove-AzServiceFabricClusterCertificate.md)
클러스터 보안에 사용 되지 않도록 클러스터 인증서를 제거 합니다.

### [제거-AzServiceFabricManagedCluster](Remove-AzServiceFabricManagedCluster.md)
클러스터 리소스를 제거 합니다.

### [제거-AzServiceFabricManagedClusterClientCertificate](Remove-AzServiceFabricManagedClusterClientCertificate.md)
Remvoe는 손도장 또는 일반 이름으로 클라이언트 인증서를 인증 합니다.

### [제거-AzServiceFabricManagedNodeType](Remove-AzServiceFabricManagedNodeType.md)
노드 형식 또는 노드 형식 내의 특정 노드를 제거 합니다.

### [제거-AzServiceFabricManagedNodeTypeVMExtension](Remove-AzServiceFabricManagedNodeTypeVMExtension.md)
노드 형식에서 vm 확장을 제거 합니다.

### [제거-AzServiceFabricNode](Remove-AzServiceFabricNode.md)
클러스터에서 특정 노드 유형에 서 노드를 제거 합니다.

### [제거-AzServiceFabricNodeType](Remove-AzServiceFabricNodeType.md)
클러스터에서 전체 노드 유형을 제거 합니다.

### [제거-AzServiceFabricService](Remove-AzServiceFabricService.md)
클러스터에서 서비스를 제거 합니다.

### [제거-AzServiceFabricSetting](Remove-AzServiceFabricSetting.md)
클러스터에서 하나 또는 여러 개의 서비스 패브릭 설정을 제거 합니다.

### [다시 시작-AzServiceFabricManagedNodeType](Restart-AzServiceFabricManagedNodeType.md)
노드 형식에서 특정 노드를 다시 시작 합니다.

### [Set-AzServiceFabricManagedCluster](Set-AzServiceFabricManagedCluster.md)
클러스터 리소스 속성을 설정 합니다.

### [Set-AzServiceFabricManagedNodeType](Set-AzServiceFabricManagedNodeType.md)
-이미지로 매개 변수를 사용 하 여 노드 형식의 특정 ndes에 대해 노드 형식 리소스 속성을 설정 하거나 이미지로 된 작업을 실행 합니다.

### [Set-AzServiceFabricSetting](Set-AzServiceFabricSetting.md)
하나 또는 여러 개의 서비스 패브릭 설정을 클러스터에 추가 하거나 업데이트 합니다.

### [Set-AzServiceFabricUpgradeType](Set-AzServiceFabricUpgradeType.md)
클러스터의 Service Fabric 업그레이드 유형을 변경 합니다.

### [업데이트-AzServiceFabricApplication](Update-AzServiceFabricApplication.md)
서비스 패브릭 응용 프로그램을 업데이트 합니다. 이렇게 하면 응용 프로그램 매개 변수를 업데이트 하 고 응용 프로그램 업그레이드를 트리거할 응용 프로그램 유형 버전을 업그레이드할 수 있습니다.

### [업데이트-AzServiceFabricDurability](Update-AzServiceFabricDurability.md)
클러스터의 노드 형식에 대 한 내구성 계층 또는 VmSku를 업데이트 합니다.

### [업데이트-AzServiceFabricReliability](Update-AzServiceFabricReliability.md)
클러스터에서 기본 노드 유형의 안정성 계층을 업데이트 합니다.

