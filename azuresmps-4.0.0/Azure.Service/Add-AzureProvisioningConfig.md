---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046382"
---
# Add-AzureProvisioningConfig

## SYNOPSIS
Azure 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.

## 구문과

### Windows (기본값)
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### Linux
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### WindowsDomain
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**추가-AzureProvisioningConfig** Cmdlet은 Azure 가상 컴퓨터 구성에 프로 비전 구성 정보를 추가 합니다.
구성 개체를 사용 하 여 가상 컴퓨터를 만들 수 있습니다.

이 cmdlet은 독립 실행형 Windows 서버, Active Directory 도메인에 연결 된 Windows 서버, Linux 기반 서버 등의 다양 한 프로비저닝 구성을 지원 합니다.

Active Directory 도메인에 가입 된 서버를 만들려면 Active Directory 도메인의 정규화 된 도메인 이름 및 도메인에 대 한 가상 컴퓨터 가입 권한이 있는 사용자의 도메인 자격 증명을 지정 합니다.

## 예제의

### 예제 1: 독립 실행형 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

이 명령은 **새 AzureVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 구성 개체를 만듭니다.
이 명령은 파이프라인 연산자를 사용 하 여 현재 cmdlet에 해당 개체를 전달 합니다.
현재 cmdlet은 Windows 운영 체제를 실행 하는 가상 컴퓨터에 대 한 프로 비전 구성을 추가 합니다.
구성에는 관리자 사용자 이름 및 암호가 포함 됩니다.
이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 구성을 전달 합니다.

### 예제 2: 도메인 가입 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 contoso 도메인과 참가할 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.
명령에는 가상 컴퓨터를 도메인에 가입 하는 데 필요한 사용자 이름 및 암호가 포함 됩니다.
구성에는 사용자가 처음 로그온 할 때 사용자 암호를 변경 해야 합니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

### 예제 3: Linux 기반 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 Linux 운영 체제를 실행 하는 가상 컴퓨터에 대 한 프로 비전 구성을 추가 합니다.
구성에는 루트 사용자 이름 및 암호가 포함 됩니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

### 예제 4: WinRM 용 인증서를 포함 하는 가상 컴퓨터 만들기
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

첫 번째 명령은 인증서 저장소에서 인증서를 가져온 다음 $certs 배열 변수에 저장 합니다.

두 번째 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 WinRM에 대 한 인증서를 포함 하는 프로비저닝 구성을 추가 합니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

### 예제 5: HTTP를 통해 WinRM을 사용 하도록 설정한 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 HTTP를 통해 WinRM이 설정 된 프로비저닝 구성을 추가 합니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

### 예제 6: HTTPS를 통해 WinRM을 사용 하지 않도록 설정 된 가상 컴퓨터 만들기
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

이 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 HTTPS를 통해 WinRM을 사용 하지 않도록 설정 하는 프로비저닝 구성을 추가 합니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

### 예제 7: 키 내보내기를 사용 하지 않고 가상 컴퓨터 만들기
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

첫 번째 명령은 인증서 저장소에서 인증서를 가져온 다음 $certs 배열 변수에 저장 합니다.

두 번째 명령은 가상 컴퓨터 구성 개체를 만든 다음 현재 cmdlet에 전달 합니다.
현재 cmdlet은 인증서를 포함 하 고 개인 키를 내보내지 않는 가상 컴퓨터에 대 한 프로비저닝 구성을 추가 합니다.
이 명령은 프로비저닝 개체를 기반으로 가상 컴퓨터를 만듭니다.

## 변수

### -AdminUsername
이 구성이 가상 컴퓨터에 만든 관리자 계정의 사용자 이름을 지정 합니다.

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -인증서
이 구성이 가상 컴퓨터에 설치 하는 인증서 집합을 지정 합니다.

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
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

게스트 운영 체제가 Windows 운영 체제 이면이 구성에서는이 데이터 를%SYSTEMDRIVE%\AzureData\CustomData.bin. 이라는 이진 파일로 저장 합니다.

게스트 운영 체제가 Linux 인 경우이 구성은 ovf-env.xml 파일을 사용 하 여 데이터를 전달 합니다.
구성에서는 파일을/var/lib/waagent 디렉터리로 복사 합니다.
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

### -Disable자동 업데이트
이 구성이 자동 업데이트를 사용 하지 않도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableGuestAgent
이 구성이이 구성을 통해 IaaS (인프라) 게스트 에이전트로 비활성화 됨을 나타냅니다.

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

### -DisableSSH
이 구성이 SSH를 사용 하지 않도록 설정 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DisableWinRMHttps
이 구성이 HTTPS에서 WinRM (Windows Remote Management)을 사용 하지 않도록 지정 합니다.
기본적으로, WinRM은 HTTPS를 통해 사용 하도록 설정 됩니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -도메인
도메인에 컴퓨터를 추가할 수 있는 권한이 있는 계정의 도메인 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainPassword
도메인에 컴퓨터를 추가할 수 있는 권한이 있는 사용자 계정의 암호를 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DomainUserName
도메인에 컴퓨터를 추가할 수 있는 권한이 있는 사용자 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnableWinRMHttp
이 구성을 통해 WinRM over HTTP를 사용할 수 있음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
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

### -JoinDomain
참가할 도메인의 FQDN (정규화 된 도메인 이름)을 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
이 구성으로 Linux 구성이 생성 됨을 나타냅니다.

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
이 구성이 가상 컴퓨터에 만든 Linux 관리 계정의 사용자 이름을 지정 합니다.

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

### -MachineObjectOU
구성에서 컴퓨터 계정을 만드는 OU (조직 구성 단위)의 정규화 된 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -없음에 대 한 Dpendpoint
이 구성이 원격 데스크톱 끝점 없이 가상 컴퓨터를 만들기를 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHEndpoint
이 구성이 SSH 끝점 없이 가상 컴퓨터를 만들기를 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoSSHPassword
이 구성이 SSH 암호 없이 가상 컴퓨터를 생성 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NoWinRMEndpoint
이 구성이 가상 컴퓨터에 대 한 WinRM 끝점을 추가 하지 않음을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -암호
관리자 계정의 암호를 지정 합니다.

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

### -ResetPasswordOnFirstLogon
가상 컴퓨터에서 처음 로그온 할 때 사용자가 암호를 변경 해야 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
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

### -표준 시간대
가상 컴퓨터의 표준 시간대를 지정 합니다 (예: 태평양 표준시 또는 캐나다 중부 표준시).

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
가상 컴퓨터 개체를 지정 합니다.

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
이 구성으로 Windows 운영 체제를 실행 하는 독립 실행형 가상 컴퓨터가 생성 됨을 나타냅니다.

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

### -WindowsDomain
이 구성으로 Active Directory 도메인에 연결 된 Windows server가 생성 됨을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WinRMCertificate
이 구성이 WinRM 끝점에 연결 하는 인증서를 지정 합니다.

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
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
Parameter Sets: Windows, WindowsDomain
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

[뉴욕](./New-AzureVM.md)

[새로운 AzureVMConfig](./New-AzureVMConfig.md)


