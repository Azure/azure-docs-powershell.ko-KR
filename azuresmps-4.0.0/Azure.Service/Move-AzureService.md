---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F8418A93-8E6B-4A1C-B319-7CACE95AB600
online version: ''
schema: 2.0.0
ms.openlocfilehash: a1daf0cb8881beeb71f0b3fe68732d596c56ce12
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046240"
---
# Move-AzureService

## SYNOPSIS
클라우드 서비스를 Azure 리소스 관리자 스택으로 마이그레이션합니다.

## 구문과

### AbortMigrationParameterSet
```
Move-AzureService [-Abort] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### CommitMigrationParameterSet
```
Move-AzureService [-Commit] [-ServiceName] <String> [-DeploymentName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PrepareNewMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### PrepareExistingMigrationParameterSet
```
Move-AzureService [-Prepare] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateNewMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-CreateNewVirtualNetwork]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### ValidateExistingMigrationParameterSet
```
Move-AzureService [-Validate] [-ServiceName] <String> [-DeploymentName] <String> [-UseExistingVirtualNetwork]
 [-VirtualNetworkResourceGroupName] <String> [-VirtualNetworkName] <String> [-SubnetName] <String>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**이동-azureservice** cmdlet은 클라우드 서비스와 해당 서비스 내의 배포를 Azure 리소스 관리자 스택의 리소스 그룹으로 마이그레이션합니다.

## 예제의

### 예제 1: 서비스 마이그레이션 준비
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

이 명령은 ContosoService 라는 서비스를 Azure Resource Manager 스택으로 마이그레이션하도록 준비 합니다.
마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.

### 예제 2: 서비스 마이그레이션 시작
```
PS C:\> Move-AzureService -Commit -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

이 명령은 ContosoService 이라는 서비스를 Azure 리소스 관리자 스택으로 마이그레이션하기 시작 합니다.
마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.

### 예제 3: 서비스 마이그레이션 취소
```
PS C:\> Move-AzureService -Abort -ServiceName "ContosoService" -DeploymentName "ContosoVM"
```

이 명령은 ContosoService 이라는 서비스의 마이그레이션을 취소 하 여 Azure Resource Manager 스택에 있습니다.

### 예제 4: 기존 가상 네트워크에 대 한 서비스 마이그레이션 준비
```
PS C:\> Move-AzureService -Prepare -ServiceName "ContosoService" -DeploymentName "ContosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "VnetRG" -VirtualNetworkName "ContosoVNET" -SubnetName "ContosoSubnet"
```

이 명령은 ContosoService 라는 서비스를 Azure Resource Manager 스택으로 마이그레이션하도록 준비 합니다.
마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.
마이그레이션에서는 이전에 만든 가상 네트워크를 사용 합니다.

### 예제 5: 서비스 마이그레이션 유효성 검사
```
PS C:\> Move-AzureService -Validate -ServiceName "ContosoService" -DeploymentName "ContosoVM" -CreateNewVirtualNetwork
```

이 명령은 ContosoService 이라는 서비스에 대 한 마이그레이션을 유효성 검사 하 여 Azure Resource Manager 스택에 있습니다.
마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.

### 예제 6: 기존 가상 네트워크에 대 한 서비스 마이그레이션 유효성 검사
```
PS C:\> Move-AzureService -Validate -ServiceName "contosoService" -DeploymentName "contosoVM" -UseExistingVirtualNetwork -VirtualNetworkResourceGroupName "vnetRG" -VirtualNetworkName "contosoVNET" -SubnetName "contosoSubnet"
```

이 명령은 ContosoService 이라는 서비스에 대 한 마이그레이션을 유효성 검사 하 여 Azure Resource Manager 스택에 있습니다.
마이그레이션에는 ContosoVM 이라는 배포가 포함 됩니다.
마이그레이션에서는 이전에 만든 가상 네트워크를 사용 합니다.

## 변수

### -Abort
이 cmdlet이 서비스 마이그레이션을 취소 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -커밋
이 cmdlet이 서비스 마이그레이션을 시작 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateNewVirtualNetwork
이 cmdlet이 Azure Resource Manager 스택에 가상 네트워크를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, ValidateNewMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeploymentName
이 cmdlet이 마이그레이션하는 클라우드 서비스 배포의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -준비
이 cmdlet이 클라우드 서비스 마이그레이션을 준비 하는 것을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareNewMigrationParameterSet, PrepareExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -ServiceName
이 cmdlet이 마이그레이션하는 클라우드 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubnetName
가상 네트워크 내부의 서브넷 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UseExistingVirtualNetwork
이 cmdlet이 클라우드 서비스를 Azure Resource Manager 스택의 기존 가상 네트워크로 마이그레이션하는 것을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -유효성 검사
이 cmdlet이 마이그레이션에 대 한 클라우드 서비스의 유효성을 검사 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: ValidateNewMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkName
가상 네트워크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VirtualNetworkResourceGroupName
기존 가상 네트워크의 리소스 그룹 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: PrepareExistingMigrationParameterSet, ValidateExistingMigrationParameterSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[이동-AzureNetworkSecurityGroup](./Move-AzureNetworkSecurityGroup.md)

[이동-AzureReservedIP](./Move-AzureReservedIP.md)

[이동-AzureRouteTable](./Move-AzureRouteTable.md)

[이동-AzureStorageAccount](./Move-AzureStorageAccount.md)

[이동-AzureVirtualNetwork](./Move-AzureVirtualNetwork.md)


