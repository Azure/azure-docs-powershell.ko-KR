---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046200"
---
# New-AzureVM

## SYNOPSIS
Azure 가상 컴퓨터를 만듭니다.

## 구문과

### ExistingService (기본값)
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### CreateService
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**뉴욕** cmdlet은 새 가상 컴퓨터를 기존 Azure 서비스에 추가 하거나, *위치* 또는 *AffinityGroup* 가 지정 된 경우 현재 구독에 가상 컴퓨터와 서비스를 만듭니다.

## 예제의

### 예제 1: Windows 구성에 대 한 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 지정 된 선호도 그룹에 가상 컴퓨터를 만듭니다.

### 예제 2: Linux 용 가상 컴퓨터 만들기 구성
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

이 명령은 Linux에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 지정 된 선호도 그룹에 가상 컴퓨터를 만듭니다.

### 예제 3: 가상 컴퓨터 만들기 및 데이터 디스크 추가
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

처음 두 명령은 **get-AzureVMImage** cmdlet을 사용 하 여 사용할 수 있는 이미지를 가져오고 둘 중 하나를 $Image 변수에 저장 합니다.

이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 Azure data disk를 사용 하 여 가상 컴퓨터를 만듭니다.

### 예제 4: 예약 된 IP 주소를 사용 하 여 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

이 명령은 Windows 운영 체제에 대 한 가상 컴퓨터 구성을 기반으로 하는 프로비저닝 구성을 만들고이를 사용 하 여 예약 된 IP 주소를 사용 하 여 가상 컴퓨터를 만듭니다.

## 변수

### -AffinityGroup
클라우드 서비스가 상주 하는 Azure 선호도 그룹을 지정 합니다.
이 매개 변수는이 cmdlet이 클라우드 서비스를 만들 때만 필요 합니다.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DeploymentLabel
배포에 대 한 레이블을 지정 합니다.

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

### -DeploymentName
배포 이름을 지정 합니다.
지정 하지 않으면이 cmdlet은 배포 이름으로 서비스 이름을 사용 합니다.

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

### -DnsSettings
새 배포에 대 한 DNS 설정을 정의 하는 DNS 서버 개체를 지정 합니다.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

### -InternalLoadBalancerConfig
내부 부하 분산 장치를 지정 합니다.
이 매개 변수는 사용 되지 않습니다.

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -위치
새 서비스를 호스팅하는 위치를 지정 합니다.
서비스가 이미 있는 경우에는이 매개 변수를 지정 하지 마세요.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -ReservedIPName
예약 된 IP 주소의 이름을 지정 합니다.

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

### -ReverseDnsFqdn
역방향 DNS에 대 한 정규화 된 도메인 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceDescription
새 서비스에 대 한 설명을 지정 합니다.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceLabel
새 서비스에 대 한 레이블을 지정 합니다.

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
새 또는 기존 서비스 이름을 지정 합니다.

서비스가 없으면이 cmdlet이 해당 서비스를 만듭니다.
*Location* 또는 *AffinityGroup* 매개 변수를 사용 하 여 서비스를 만들 위치를 지정 합니다.

서비스가 존재 하는 경우에는 *위치* 또는 *AffinityGroup* 매개 변수가 필요 하지 않습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Vm
만들 가상 컴퓨터 개체의 목록을 지정 합니다.

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -VNetName
이 cmdlet이 가상 컴퓨터를 배포 하는 가상 네트워크 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WaitForBoot
이 cmdlet이 가상 머신이 **ReadyRole** state에 도달할 때까지 대기 하도록 지정 합니다.
FailedStartingVM, ProvisioningFailed, ProvisioningTimeout 중에 가상 머신이 다음 상태 중 하나에 속하면이 cmdlet이 실패 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[-AzureDataDisk 추가](./Add-AzureDataDisk.md)

[추가-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[새로운 AzureVMConfig](./New-AzureVMConfig.md)


