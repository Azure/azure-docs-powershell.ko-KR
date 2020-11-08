---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045955"
---
# Set-AzurePublicIP

## SYNOPSIS
Azure 가상 컴퓨터에 공용 IP를 추가 합니다.

## 구문과

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Set AzurePublicIP** Cmdlet은 Azure 가상 컴퓨터에 공용 IP를 추가 합니다.
기존 가상 컴퓨터에 대해이 cmdlet을 실행 하는 경우에는 가상 컴퓨터를 업데이트 하 여 변경 내용을 구현 합니다.
도메인 이름 레이블을 지정 하 여 공용 IP에 해당 하는 DNS 항목을 만들 수 있습니다.

## 예제의

### 예제 1: 기존 가상 컴퓨터에 공용 IP 추가
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.
현재 cmdlet은 공용 IP 이름 (\ ip)을 추가 합니다.
이 명령은 가상 컴퓨터를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.

### 예제 2: 새 가상 컴퓨터에 공용 IP 추가
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

이 명령은 **새 AzureVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 구성 개체를 만듭니다.
이 명령은 추가 구성을 제공 하는 **AzureProvisioningConfig** cmdlet에 해당 개체를 전달 합니다.
현재 cmdlet은 공용 IP 이름 (\ ip)을 추가 합니다.
이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 구성을 전달 합니다.

### 예제 3: 공용 IP 및 레이블을 기존 가상 컴퓨터에 추가
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

이 명령은 ' Add-azurevm ' cmdlet을 사용 하 여 FTPInAzure 라는 서비스에서 가상 컴퓨터 (이름 **)** 인스턴스를 가져옵니다.
이 명령은 파이프라인 연산자를 사용 하 여 해당 가상 컴퓨터를 현재 cmdlet으로 전달 합니다.
현재 cmdlet은 공용 IP 이름에는 ip 주소와 레이블 ipname을 추가 합니다.
이 명령은 변경 내용을 구현 하는 가상 컴퓨터를 업데이트 합니다.

### 예제 4: 공용 IP 및 레이블을 새 가상 컴퓨터에 추가
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

이 명령은 가상 컴퓨터 구성 개체를 만든 다음 추가 구성을 제공 하는 **AzureProvisioningConfig** 에 해당 개체를 전달 합니다.
현재 cmdlet은 공용 IP 이름에는 ip 주소와 레이블 ipname을 추가 합니다.
명령이 가상 컴퓨터를 만듭니다.

## 변수

### -DomainNameLabel
공용 IP 주소에 해당 하는 DNS 항목에 사용할 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IdleTimeoutInMinutes
TCP 유휴 시간 제한 기간 (분)을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
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

### -PublicIPName
공용 IP 이름을 지정 합니다.

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

### -VM
이 cmdlet이 공용 IP를 추가 하는 가상 컴퓨터를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. ServiceManagement. IPersistentVM

## 상속자

## 관련 링크

[Get-AzurePublicIP](./Get-AzurePublicIP.md)

[다운로드-Add-azurevm](./Get-AzureVM.md)

[뉴욕](./New-AzureVM.md)

[새로운 AzureVMConfig](./New-AzureVMConfig.md)

[제거-AzurePublicIP](./Remove-AzurePublicIP.md)

[업데이트-Add-azurevm](./Update-AzureVM.md)


