---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045932"
---
# New-AzureCertificateSetting

## SYNOPSIS
인증서에 대 한 인증서 설정 개체를 서비스에 만듭니다.

## 구문과

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureCertificateSetting** Cmdlet은 Azure 서비스에 있는 인증서에 대 한 인증서 설정 개체를 만듭니다.

인증서 설정 개체를 사용 하 여 **추가-AzureProvisioningConfig** cmdlet을 사용 하 여 구성 개체를 만들 수 있습니다.
구성 개체를 사용 하 여 **새 add-azurevm** cmdlet을 사용 하 여 가상 컴퓨터를 만듭니다.
인증서 설정 개체를 사용 하 여 **새 AzureQuickVM** cmdlet을 사용 하 여 가상 컴퓨터를 만들 수 있습니다.

## 예제의

### 예제 1: 인증서 설정 개체 만들기
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

이 명령은 기존 인증서에 대 한 인증서 설정 개체를 만듭니다.

### 예제 2: 구성 설정 개체를 사용 하는 가상 컴퓨터 만들기
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

첫 번째 명령은 **AzureCertificate** cmdlet을 사용 하 여 ContosoService 이라는 인증서 ContosoCert를 서비스에 추가 합니다.

두 번째 명령은 인증서 설정 개체를 만든 다음 $CertificateSetting 변수에 저장 합니다.

세 번째 명령은 **AzureVMImage** cmdlet을 사용 하 여 이미지 리포지토리에서 이미지를 가져옵니다.
이 명령은 $Image 변수에 이미지를 저장 합니다.

마지막 명령은 **AzureVMConfig** cmdlet을 사용 하 여 $Image의 이미지를 기반으로 가상 컴퓨터 구성 개체를 만듭니다.
이 명령은 파이프라인 연산자를 사용 하 여 **AzureProvisioningConfig** cmdlet에 해당 개체를 전달 합니다.
해당 cmdlet은 구성에 프로 비전 정보를 추가 합니다.
이 명령은 가상 컴퓨터를 만드는 **새 add-azurevm** cmdlet에 개체를 전달 합니다.

## 변수

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

### -StoreName
인증서를 저장할 인증서 저장소를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 주소록
- AuthRoot
- CertificateAuthority
- 허가
- 내
- 루트
- 개인 사용자
- 용 게시자

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[추가-AzureCertificate](./Add-AzureCertificate.md)

[추가-AzureProvisioningConfig](./Add-AzureProvisioningConfig.md)

[Get-AzureCertificate](./Get-AzureCertificate.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[새로운 AzureQuickVM](./New-AzureQuickVM.md)

[뉴욕](./New-AzureVM.md)

[제거-AzureCertificate](./Remove-AzureCertificate.md)


