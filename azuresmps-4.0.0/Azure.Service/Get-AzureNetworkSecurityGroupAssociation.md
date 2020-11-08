---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 6AF7D392-8C8B-4695-95D0-E927093F654A
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21eb1b7bcad200e67659f830bfb3bbef42fe0f8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046582"
---
# Get-AzureNetworkSecurityGroupAssociation

## SYNOPSIS
가상 머신, 네트워크 어댑터 또는 PaaS 역할에 대 한 네트워크 보안 그룹을 가져옵니다.

## 구문과

### Getnetworksecuritygrouationnetworkforsubnet
```
Get-AzureNetworkSecurityGroupAssociation -VirtualNetworkName <String> -SubnetName <String> [-Detailed]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GetNetworkSecurityGroupAssociationForIaaSRole
```
Get-AzureNetworkSecurityGroupAssociation -VM <PersistentVMRoleContext> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Getnetworksecuritygroupayationasrole
```
Get-AzureNetworkSecurityGroupAssociation [-Slot <String>] -RoleName <String> -ServiceName <String>
 [-NetworkInterfaceName <String>] [-Detailed] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureNetworkSecurityGroupAssociation** cmdlet은 가상 머신, 네트워크 어댑터 또는 플랫폼 as 서비스 (PaaS) 역할에 대 한 네트워크 보안 그룹을 가져옵니다.

## 예제의

### 예제 1: 가상 컴퓨터용 네트워크 보안 그룹 가져오기
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "ContosoVM06" | Get-AzureNetworkSecurityGroupAssociation
```

이 명령은 ContosoService 이라는 서비스에 대 한 ContosoVM06 이라는 가상 컴퓨터를 가져오고 현재 cmdlet에 해당 가상 컴퓨터 개체를 전달 합니다.
현재 cmdlet은 해당 가상 컴퓨터와 연결 된 네트워크 보안 그룹을 가져옵니다.

## 변수

### -세부 정보
이 cmdlet이 가상 컴퓨터와 연결 된 네트워크 보안 그룹의 세부 정보를 반환 하는 것을 나타냅니다.
이러한 세부 정보에는 위치 및 규칙이 포함 됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkInterfaceName
이 cmdlet이 네트워크 보안 그룹을 가져오는 네트워크 어댑터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RoleName
이 cmdlet이 네트워크 보안 그룹을 가져오는 PaaS 역할의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
클라우드 서비스의 이름을 지정 합니다.
PaaS 역할은이 매개 변수에서 지정 하는 서비스에 속합니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole, GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
PaaS 슬롯을 지정 합니다.
이 cmdlet에서 네트워크 보안 그룹을 가져오는 PaaS 역할에이 매개 변수에서 지정 하는 슬롯이 있습니다.
유효한 값은 다음과 같습니다. 

- 프로덕션용
- 대기 

기본값은 실제 값입니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForPaaSRole
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetName
이 cmdlet이 네트워크 보안 그룹을 가져오는 서브넷의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
이 cmdlet이 네트워크 보안 그룹을 가져오는 서브넷을 포함 하는 가상 네트워크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetNetworkSecurityGroupAssociationForSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
이 cmdlet이 네트워크 보안 그룹을 적용 하는 가상 컴퓨터를 지정 합니다.

```yaml
Type: PersistentVMRoleContext
Parameter Sets: GetNetworkSecurityGroupAssociationForIaaSRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. ServiceManagement를 INetworkSecurityGroup으로 그룹화 합니다.

## 상속자

## 관련 링크

[제거-AzureNetworkSecurityGroupAssociation](./Remove-AzureNetworkSecurityGroupAssociation.md)

[Set-AzureNetworkSecurityGroupAssociation](./Set-AzureNetworkSecurityGroupAssociation.md)


