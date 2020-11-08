---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045982"
---
# New-AzureSSHKey

## SYNOPSIS
기존 인증서를 새 Linux 기반 Azure 가상 컴퓨터에 삽입 하는 SSH 키 개체를 만듭니다.

## 구문과

### 쌍
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### publickey
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureSSHKey** cmdlet은 이미 Azure에 추가 된 인증서에 대 한 SSH 키 개체를 만듭니다.
이 SSH 키 개체 **는 뉴욕을 사용 하** 여 새 가상 컴퓨터에 대 한 구성 개체를 만들거나 **new-AzureQuickVM** 가 있는 새 가상 컴퓨터를 만들 때 **AzureProvisioningConfig** 에서 사용할 수 있습니다.
가상 컴퓨터 만들기 스크립트의 일부로 포함 되는 경우 지정 된 SSH 공개 키 또는 키 쌍이 새 가상 컴퓨터에 추가 됩니다.

## 예제의

### 예제 1: 인증서 설정 개체 만들기
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

이 명령은 기존 인증서에 대 한 인증서 설정 개체를 만든 다음 나중에 사용 하기 위해 변수에 개체를 저장 합니다.

### 예제 2: 서비스에 인증서 추가
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

이 명령은 Azure 서비스에 인증서를 추가한 다음 인증서를 사용 하는 새 Linux 가상 컴퓨터를 만듭니다.

## 변수

### -지문
인증서의 지문을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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

### -키 쌍
이 cmdlet이 새 가상 컴퓨터 구성에 SSH 키 쌍을 삽입 하기 위한 개체를 만들기 위해 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Path
SSH 공개 키 또는 키 쌍을 저장할 경로를 지정 합니다.

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

### -PublicKey
이 cmdlet이 새 가상 컴퓨터 구성에 SSH 공개 키를 삽입 하기 위한 개체를 만들기 위해 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
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

[추가-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[새로운 AzureVMConfig](./New-AzureVMConfig.md)

[뉴욕](./New-AzureVM.md)

[새로운 AzureQuickVM](./New-AzureQuickVM.md)


