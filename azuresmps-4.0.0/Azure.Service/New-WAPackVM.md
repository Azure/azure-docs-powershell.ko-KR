---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047398"
---
# New-WAPackVM

## SYNOPSIS
가상 컴퓨터를 만듭니다.

## 구문과

### CreateVMFromTemplate (기본값)
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateLinuxVMFromTemplate
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### CreateVMFromOSDisk
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**새-WAPackVM** cmdlet은 가상 컴퓨터를 만듭니다.

## 예제의

### 예제 1: 템플릿을 사용 하 여 Windows 운영 체제의 가상 컴퓨터 만들기
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.
Cmdlet에서 계정과 암호를 묻는 메시지를 표시 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 ContosoTemplate04 이라는 가상 컴퓨터 템플릿을 가져온 다음이를 $Template 변수에 저장 합니다.

마지막 명령은 $Template 변수에 저장 된 템플릿을 기반으로 ContosoV023 이라는 가상 컴퓨터를 만듭니다.
명령에서 *windows* 매개 변수를 지정 하므로 가상 컴퓨터에서 windows 운영 체제 버전을 실행 해야 합니다.

### 예제 2: 템플릿을 사용 하 여 Linux 운영 체제에 대 한 가상 컴퓨터 만들기
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.

두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 ContosoTemplate19 이라는 가상 컴퓨터 템플릿을 가져온 다음이를 $Template 변수에 저장 합니다.

마지막 명령은 $Template 변수에 저장 된 템플릿을 기반으로 ContosoV028 이라는 가상 컴퓨터를 만듭니다.
명령은 *linux* 매개 변수를 지정 하므로 가상 컴퓨터는 linux 운영 체제 버전을 실행 해야 합니다.

### 예제 3: 운영 체제 디스크 및 크기 프로필에서 가상 컴퓨터 만들기
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

첫 번째 명령은 **WAPackVMOSDisk** cmdlet을 사용 하 여 ContosoDiskOS 이라는 운영 체제 디스크를 가져온 다음이를 $OSDisk 변수에 저장 합니다.

두 번째 명령은 MediumSizeVM **Apackvmsizeprofile** cmdlet을 사용 하 여 명명 된 크기 프로필을 가져온 다음이를 $SizeProfile 변수에 저장 합니다.

마지막 명령은 $OSDisk에 저장 된 운영 체제 디스크에서 ContosoV073 이라는 가상 컴퓨터와 $SizeProfile에 저장 된 크기 프로필을 만듭니다.

## 변수

### -AdministratorSSHKey
관리자 계정에 대 한 SSH (보안 셸) 키를 지정 합니다.

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Linux
Cmdlet이 Linux 운영 체제를 실행 하는 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
가상 컴퓨터의 이름을 지정 합니다.

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

### -OSDisk
운영 체제 디스크를 **VirtualHardDisk** 개체로 지정 합니다.
운영 체제 디스크를 얻으려면 **WAPackVMOSDisk** cmdlet을 사용 합니다.

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProductKey
제품 키를 지정 합니다.
제품 키는 제품 라이선스를 식별 하는 25 자리 숫자입니다.
가상 컴퓨터 또는 호스트에 설치 하려는 운영 체제의 제품 키를 사용 합니다.

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
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

### -Template
템플릿을 지정 합니다.
Cmdlet이 지정 된 템플릿을 기반으로 가상 컴퓨터를 만듭니다.
템플릿 개체를 가져오려면 Get-WAPackVMTemplate cmdlet을 사용 합니다.

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMCredential
로컬 관리자 계정에 대 한 자격 증명을 지정 합니다.
**PSCredential** 개체를 가져오려면 **Get-Credential** cmdlet을 사용 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMSizeProfile
가상 머신의 크기 프로필을 **HardwareProfile** 개체로 지정 합니다.
크기 프로필을 얻으려면 **Get-WAPackVMSizeProfile** cmdlet을 사용 합니다.

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VNet
가상 네트워크를 지정 합니다.
Cmdlet이 가상 컴퓨터를 지정 된 가상 네트워크에 연결 합니다.
가상 네트워크를 가져오려면 **Get-WAPackVNet** cmdlet을 사용 합니다.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Windows
Cmdlet이 Windows 운영 체제를 실행 하는 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
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

## 출력

## 상속자

## 관련 링크

[Get-WAPackVM](./Get-WAPackVM.md)

[제거-WAPackVM](./Remove-WAPackVM.md)

[다시 시작-WAPackVM](./Restart-WAPackVM.md)

[Resume-WAPackVM](./Resume-WAPackVM.md)

[Set-WAPackVM](./Set-WAPackVM.md)

[시작-WAPackVM](./Start-WAPackVM.md)

[중지-WAPackVM](./Stop-WAPackVM.md)

[일시 중단-WAPackVM](./Suspend-WAPackVM.md)

[Get-WAPackVMSizeProfile](./Get-WAPackVMSizeProfile.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)

[Get-WAPackVMOSDisk](./Get-WAPackVMOSDisk.md)


