---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC8C915A-A0BC-41DE-9DBF-3617536E3D1A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermcontainerserviceconfig
schema: 2.0.0
ms.openlocfilehash: 4a6f30d1f958094267b4ba8ddf09eb2e342ee889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882690"
---
# New-AzureRmContainerServiceConfig

## SYNOPSIS
컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmContainerServiceConfig [[-Location] <String>] [[-Tag] <Hashtable>]
 [[-OrchestratorType] <ContainerServiceOrchestratorTypes>] [[-MasterCount] <Int32>]
 [[-MasterDnsPrefix] <String>] [[-AgentPoolProfile] <ContainerServiceAgentPoolProfile[]>]
 [[-WindowsProfileAdminUsername] <String>] [[-WindowsProfileAdminPassword] <String>]
 [[-AdminUsername] <String>] [[-SshPublicKey] <String[]>] [[-VmDiagnosticsEnabled] <Boolean>]
 [-CustomProfileOrchestrator <String>] [-ServicePrincipalProfileClientId <String>]
 [-ServicePrincipalProfileSecret <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmContainerServiceConfig** cmdlet은 컨테이너 서비스에 대 한 로컬 구성 개체를 만듭니다.
이 개체를 New-AzureRmContainerService cmdlet에 제공 하 여 컨테이너 서비스를 만듭니다.

## 예제의

### 예제 1: 컨테이너 서비스 구성 만들기
```
PS C:\> $Container = New-AzureRmContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>"
PS C:\> $Container | Add-AzureRmContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
```

이 명령은 컨테이너를 만든 다음 $Container 변수에 저장 합니다.

명령은 컨테이너 서비스 구성에 대 한 다양 한 설정을 지정 합니다. 이 명령은 파이프라인 연산자를 사용 하 여 Add-AzureRmContainerServiceAgentPoolProfile cmdlet에 구성 개체를 전달 합니다. 해당 cmdlet은 에이전트 풀 프로필을 추가 합니다.

**New-AzureRmContainerService** 의 *ContainerService* 매개 변수에 대해 $Container에서 개체를 지정 합니다.

## 변수

### -AdminUsername
Linux 기반 컨테이너 서비스에 사용할 관리자 계정 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AgentPoolProfile
컨테이너 서비스에 대 한 에이전트 풀 프로필 개체의 배열을 지정 합니다.
Add-AzureRmContainerServiceAgentPoolProfile cmdlet을 사용 하 여 프로필을 추가 합니다.

```yaml
Type: ContainerServiceAgentPoolProfile[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CustomProfileOrchestrator
사용자 지정 프로필 orchestrator를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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
컨테이너 서비스를 만들 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MasterCount
만들 마스터 가상 컴퓨터 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -MasterDnsPrefix
마스터 가상 컴퓨터에 대 한 DNS 접두사를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OrchestratorType
컨테이너 서비스에 대 한 orchestrator 유형을 지정 합니다.
이 매개 변수에 허용 되는 값은 DCOS 및 Swarm입니다.

```yaml
Type: ContainerServiceOrchestratorTypes
Parameter Sets: (All)
Aliases: 
Accepted values: Swarm, DCOS, Custom, Kubernetes

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalProfileClientId
주 프로필 클라이언트 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalProfileSecret
주 프로필 비밀을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SshPublicKey
Linux 기반 컨테이너 서비스에 대 한 SSH 공개 키를 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### 태그
해시 테이블 형태의 키-값 쌍입니다. 예를 들어:

@ {key0 = "value0", key1 = $null, key2 = "value2"}

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VmDiagnosticsEnabled
이 구성으로 컨테이너 서비스 가상 컴퓨터에 대 한 진단을 사용할 수 있는지 여부를 나타냅니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsProfileAdminPassword
Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 암호를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WindowsProfileAdminUsername
Windows 운영 체제를 사용 하는 컨테이너 서비스에 대 한 관리자 사용자 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### PSContainerService의. m a.

## 상속자

## 관련 링크

[추가-AzureRmContainerServiceAgentPoolProfile](./Add-AzureRmContainerServiceAgentPoolProfile.md)

[새로운 AzureRmContainerService](./New-AzureRmContainerService.md)
