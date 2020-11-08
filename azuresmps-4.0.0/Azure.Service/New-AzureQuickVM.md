---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045909"
---
# New-AzureQuickVM

## SYNOPSIS
Azure 가상 컴퓨터를 구성 하 고 만듭니다.

## 구문과

### Windows (기본값)
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureQuickVM** Cmdlet은 Azure 가상 컴퓨터를 구성 하 고 만듭니다.
이 cmdlet은 가상 컴퓨터를 기존 Azure 서비스에 배포할 수 있습니다.
이 cmdlet은 새 가상 컴퓨터를 호스트 하는 Azure 서비스를 만들 수 있습니다.

## 예제의

### 예제 1: 가상 컴퓨터 만들기
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

이 명령은 기존 서비스에서 Windows 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.
Cmdlet은 지정 된 이미지의 가상 컴퓨터를 기반으로 합니다.
명령에서 *Waitforboot* 매개 변수를 지정 합니다.
따라서 cmdlet은 가상 컴퓨터가 시작 될 때까지 기다립니다.

### 예제 2: 인증서를 사용 하 여 가상 컴퓨터 만들기
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

첫 번째 명령은 저장소에서 인증서를 가져와 $certs 변수에 저장 합니다.

두 번째 명령은 이미지에서 기존 서비스로 Windows 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.
기본적으로 가상 컴퓨터에서 WinRM Https 수신기를 사용할 수 있습니다.
명령에서 *Waitforboot* 매개 변수를 지정 합니다.
따라서 cmdlet은 가상 컴퓨터가 시작 될 때까지 기다립니다.
명령이 WinRM 인증서를 업로드 하 고 호스팅된 서비스에 X509Certificates 합니다.

### 예제 3: Linux 운영 체제를 실행 하는 가상 컴퓨터 만들기
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

이 명령은 이미지에서 Linux 운영 체제를 실행 하는 가상 컴퓨터를 만듭니다.
이 명령은 새 가상 컴퓨터를 호스트 하는 서비스를 만듭니다.
명령에서 서비스 위치를 지정 합니다.

### 예제 4: 가상 컴퓨터 만들기 및 새 가상 컴퓨터를 호스트 하는 서비스 만들기
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

첫 번째 명령은 **가져오기-AzureLocation** cmdlet을 사용 하 여 위치를 가져온 다음 $Locations 배열 변수에 저장 합니다.

두 번째 명령은 **AzureVMImage** cmdlet을 사용 하 여 사용 가능한 이미지를 가져온 다음이를 $Images array 변수에 저장 합니다.

마지막 명령은 VirtualMachine25 이라는 큰 가상 컴퓨터를 만듭니다.
가상 컴퓨터에서 Windows 운영 체제를 실행 합니다.
$Images의 이미지 중 하나를 기준으로 합니다.
이 명령은 새 가상 컴퓨터에 대 한 ContosoService03 이라는 서비스를 만듭니다.
서비스가 $Locations 위치에 있습니다.

### 예제 5: 예약 된 IP 이름을 가진 가상 컴퓨터 만들기
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

첫 번째 명령은 위치를 가져온 다음 $Locations 배열 변수에 저장 합니다.

두 번째 명령은 사용할 수 있는 이미지를 가져온 다음 $Images 배열 변수에 저장 합니다.

마지막 명령은 $Images의 이미지 중 하나를 기반으로 VirtualMachine27 이라는 가상 컴퓨터를 만듭니다.
이 명령은 $Locations 위치에 서비스를 만듭니다.
가상 컴퓨터에는 예약 된 IP 이름이 있으며, 이전에 $ipName 변수에 저장 되어 있습니다.

## 변수

### -AdminUsername
이 cmdlet이 가상 컴퓨터에서 만드는 관리자 계정의 사용자 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AffinityGroup
가상 컴퓨터에 대 한 선호도 그룹을 지정 합니다.
이 cmdlet이 가상 컴퓨터에 대 한 Azure 서비스를 만드는 경우에만이 매개 변수 또는 *위치* 매개 변수를 지정 합니다.

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

### -AvailabilitySetName
이 cmdlet이 가상 컴퓨터를 만드는 가용성 집합의 이름을 지정 합니다.

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

### -인증서
이 cmdlet에서 서비스를 만드는 데 사용 하는 인증서 목록을 지정 합니다.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CustomDataFile 접속
가상 컴퓨터에 대 한 데이터 파일을 지정 합니다.
이 cmdlet은 파일의 내용을 Base64로 인코딩합니다.
파일의 길이는 64 킬로바이트 미만 이어야 합니다.

게스트 운영 체제가 Windows 운영 체제 이면이 cmdlet은이 데이터 를%SYSTEMDRIVE%\AzureData\CustomData.bin. 이라는 이진 파일로 저장 합니다.

게스트 운영 체제가 Linux 인 경우이 cmdlet은 ovf-env.xml 파일을 사용 하 여 데이터를 전달 합니다.
설치는 해당 파일을/var/lib/waagent 디렉터리로 복사 합니다.
또한 에이전트는/var/lib/waagent/CustomData.에 Base64로 인코딩된 데이터를 저장 합니다.

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

### -DisableGuestAgent
이 cmdlet이 IaaS (인프라) 제공 게스트 에이전트를 사용 하지 않도록 지정 합니다.

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

### -DisableWinRMHttps
이 cmdlet이 HTTPS에서 WinRM (Windows Remote Management)을 사용 하지 않도록 지정 합니다.
기본적으로, WinRM은 HTTPS를 통해 사용 하도록 설정 됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DnsSettings
새 배포에 대 한 DNS 설정을 정의 하는 DNS 서버 개체의 배열을 지정 합니다.
**DnsServer** 개체를 만들려면 **새 azuredns** cmdlet을 사용 합니다.

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
이 cmdlet이 HTTP를 통해 WinRM을 사용할 수 있음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostCaching
운영 체제 디스크에 대 한 호스트 캐싱 모드를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 읽기
- 쓰기

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

### -ImageName
이 cmdlet에서 운영 체제 디스크를 만드는 데 사용 하는 디스크 이미지의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -InstanceSize
인스턴스의 크기를 지정 합니다.
유효한 값은 다음과 같습니다. 

- ExtraSmall
- Small
- 높음이나
- 용량의
- ExtraLarge
- 5
- A6
- (A
- A8
- A9
- Basic_A0
- Basic_A1
- Basic_A2
- Basic_A3
- Basic_A4
- Standard_D1
- Standard_D2
- Standard_D3
- Standard_D4
- Standard_D11
- Standard_D12
- Standard_D13
- Standard_D14

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

### -Linux
이 cmdlet이 Linux 기반 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LinuxUser
이 cmdlet에서 가상 컴퓨터에 만든 Linux 관리 계정의 사용자 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -위치
가상 컴퓨터를 호스트 하는 Azure datacenter를 지정 합니다.
이 매개 변수를 지정 하는 경우 cmdlet은 지정 된 위치에 Azure 서비스를 만듭니다.
이 cmdlet이 가상 컴퓨터에 대 한 Azure 서비스를 만드는 경우에만이 매개 변수 또는 *AffinityGroup* 매개 변수를 지정 합니다.

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

### -MediaLocation
이 cmdlet이 가상 컴퓨터 디스크를 만드는 Azure 저장소 위치를 지정 합니다.

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

### -이름
이 cmdlet이 만드는 가상 컴퓨터의 이름을 지정 합니다.

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

### -NoExportPrivateKey
이 구성이 개인 키를 업로드 하지 않음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
이 cmdlet이 가상 컴퓨터에 대 한 WinRM 끝점을 추가 하지 않음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -암호
관리 계정에 대 한 암호를 지정 합니다.

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
예약 된 IP 이름을 지정 합니다.

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
역방향 DNS 조회에 대 한 정규화 된 도메인 이름을 지정 합니다.

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

### -ServiceName
이 cmdlet가 새 가상 컴퓨터를 추가 하는 새 또는 기존 Azure 서비스의 이름을 지정 합니다.

새 서비스를 지정 하는 경우이 cmdlet이이를 만듭니다.
새 서비스를 만들려면 *Location* 또는 *AffinityGroup* 매개 변수를 지정 해야 합니다.

기존 서비스를 지정 하는 경우 *위치* 또는 *AffinityGroup* 를 지정 하지 마세요.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHKeyPairs
SSH 키 쌍을 지정 합니다.

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SSHPublicKeys
SSH 공개 키를 지정 합니다.

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubnetNames
가상 컴퓨터의 서브넷 이름 배열을 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
가상 컴퓨터에 대 한 가상 네트워크의 이름을 지정 합니다.

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
이 cmdlet이 가상 컴퓨터가 상태 ReadyRole에 도달할 때까지 대기 하 고 있음을 나타냅니다.
가상 머신이 다음 상태 중 하나에 도달 하는 경우 cmdlet이 실패 합니다. FailedStartingVM, ProvisioningFailed 또는 ProvisioningTimeout.

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

### -Windows
이 cmdlet이 Windows 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
이 cmdlet이 WinRM 끝점에 연결 하는 인증서를 지정 합니다.

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -X509Certificates
호스팅된 서비스에 배포 되는 X509 인증서의 배열을 지정 합니다.

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
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

[가져오기-AzureLocation](./Get-AzureLocation.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[새 AzureDns](./New-AzureDns.md)


