---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047351"
---
# Set-AzureVMDscExtension

## SYNOPSIS
가상 컴퓨터에서 DSC 확장을 구성 합니다.

## 구문과

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureVMDscExtension** cmdlet은 가상 컴퓨터에서 DSC (원하는 상태 구성) 확장을 구성 합니다.

## 예제의

### 예제 1: 가상 컴퓨터에서 DSC 확장 구성
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

이 명령은 가상 컴퓨터에서 DSC 확장을 구성 합니다.

MyConfiguration.ps1.zip 패키지는 **AzureVMDscConfiguration** 명령을 사용 하 여 이전에 Azure storage에 업로드 되어 있어야 하며 MyConfiguration.ps1 스크립트와이에 종속 된 모듈을 포함 해야 합니다.

MyConfiguration 인수는 실행할 스크립트 내의 특정 DSC 구성을 나타냅니다.
- *Configurationargument* 매개 변수는 구성 함수에 전달 되는 인수를 사용 하 여 해시 테이블을 지정 합니다.

### 예제 2: 구성 데이터 경로를 사용 하 여 가상 컴퓨터에서 DSC 확장 구성
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

이 명령은 구성 데이터 경로를 사용 하 여 가상 컴퓨터에서 DSC 확장을 구성 합니다.

## 변수

### -ConfigurationArchive
이전에 게시-AzureVMDscConfiguration에 업로드 한 구성 패키지 (.zip 파일)의 이름을 지정 합니다.
이 매개 변수는 경로 없이 파일 이름만 지정 해야 합니다.

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

### -ConfigurationArgument
구성 함수에 대 한 인수를 지정 하는 해시 테이블을 지정 합니다.
키는 매개 변수 이름 및 매개 변수 값에 대 한 값에 해당 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 기본 형식
- 이름
- 배열의
- PSCredential

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
구성 함수에 대 한 데이터를 지정 하는 psd1 파일의 경로를 지정 합니다.
이 파일에는 구성 및 환경 데이터 구분에 설명 된 해시 테이블이 포함 되어야 합니다 https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .

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

### -ConfigurationName
DSC 확장에 의해 호출 되는 구성 스크립트 또는 모듈의 이름을 지정 합니다.

이 매개 변수의 값은 *Configurationarchive* 에 패키지 된 스크립트 또는 모듈에 포함 된 구성 함수 중 하나의 이름 이어야 합니다.

이 cmdlet은 사용자가이 매개 변수를 생략 하 고 확장명을 제외한 경우 *Configurationarchive* 매개 변수에 지정 된 파일의 이름입니다.
예를 들어 *Configurationarchive* 가 "SalesWebSite.ps1.zip" 이면 *ConfigurationName* 에 대 한 기본값은 "saleswebsite"입니다.

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

### -ContainerName
*Configurationarchive* 가 있는 Azure storage 컨테이너의 이름을 지정 합니다.

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

### -DataCollection
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

### -Force
이 cmdlet이 기존 blob을 덮어쓰도록 지정 합니다.

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

### -ReferenceName
확장을 참조 하는 데 사용할 수 있는 사용자 정의 문자열을 지정 합니다.
이 매개 변수는 확장이 가상 컴퓨터에 처음 추가 될 때 지정 됩니다.
후속 업데이트의 경우 확장을 업데이트 하는 동안 이전에 사용한 참조 이름을 지정 해야 합니다.
확장명에 할당 된 *Referencename* 은 **Get-add-azurevm** cmdlet을 사용 하 여 반환 됩니다.

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

### -StorageContext
구성 스크립트에 액세스 하는 데 사용 되는 보안 설정을 제공 하는 Azure storage 컨텍스트를 지정 합니다.
이 컨텍스트는 *ContainerName* 매개 변수에 지정 된 컨테이너에 대 한 읽기 액세스를 제공 합니다.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
모든 저장소 서비스에 대 한 DNS 끝점 접미사 (예, "core.contoso.net")를 지정 합니다.

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

### -버전
사용할 DSC 확장의 특정 버전을 지정 합니다.
이 매개 변수를 지정 하지 않으면 기본값은 "1. *"로 설정 됩니다.

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

### -VM
영구 가상 머신 개체를 지정 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WmfVersion
가상 컴퓨터에 설치할 WMF (Windows Management Framework) 버전을 지정 합니다.
DSC 확장은 WMF 업데이트 에서만 사용할 수 있는 DSC 기능에 따라 달라 집니다.
이 매개 변수는 가상 컴퓨터에 설치할 업데이트 버전을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 4.0.
새 버전이 이미 설치 되어 있지 않은 경우 WMF 4.0를 설치 합니다.
- 5.0.
WMF 5.0 최신 릴리스를 설치 합니다.
- 비최신.
최신 WMF, 현재 WMF 5.0을 설치 합니다.

기본값은 최신 값입니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureVMDscExtension](./Get-AzureVMDscExtension.md)

[제거-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[제거-AzureVMDscExtension](./Remove-AzureVMDscExtension.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[게시-AzureVMDscConfiguration](./Publish-AzureVMDscConfiguration.md)


