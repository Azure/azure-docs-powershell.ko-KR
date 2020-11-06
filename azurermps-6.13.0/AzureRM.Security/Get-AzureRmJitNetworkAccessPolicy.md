---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmJitNetworkAccessPolicy.md
ms.openlocfilehash: bd366b636a29a08bea9124b3c3f4b9b423dc4deb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526052"
---
# Get-AzureRmJitNetworkAccessPolicy

## SYNOPSIS
JIT 네트워크 액세스 정책을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 구독 범위 (기본값)
```
Get-AzureRmJitNetworkAccessPolicy [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ResourceGroupScope
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceGroupLevelResource
```
Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### 리소스
```
Get-AzureRmJitNetworkAccessPolicy -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
JIT (just-in-time) 네트워크 액세스 정책에서는 간단한 사용자가 VM에 대 한 임시 네트워크 연결을 만들 수 있도록 하는 정책 정의를 사용 합니다.
정책은 연결을 자동으로 닫기 전에 VM에 대 한 연결을 요청할 수 있는 포트, 프로토콜 및 원본 IP 주소와 최대 기간을 정의 합니다.
또한이 정책에 대 한 연결 요청을 볼 수 있습니다. 

## 예제의

### 예제 1
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

구독에 대 한 모든 JIT 네트워크 액세스 정책 가져오기

### 예제 2
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded

Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/northeurope/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

"MyService1" 리소스 그룹의 모든 JIT 네트워크 액세스 정책 가져오기

### 예제 3
```powershell
PS C:\> Get-AzureRmJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
Id                : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Security/locations/centralus/jitNetworkAccessPolicies/default
Name              : default
Kind              : Basic
VirtualMachines   : {/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/testService}
Requests          : {Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicyRequest}
ProvisioningState : Succeeded
```

특정 JIT 네트워크 액세스 정책을 가져옵니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
Location.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
리소스 이름입니다.

```yaml
Type: String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: String
Parameter Sets: ResourceGroupScope, ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceId
리소스 ID입니다.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### JitNetworkAccessPolicies. PSSecurityJitNetworkAccessPolicy에 대 한 Microsoft

## 상속자

## 관련 링크
