---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 98f127386a606881a0f8359e605ee2b96168a9b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878906"
---
# New-AzADSpCredential

## SYNOPSIS
기존 서비스 사용자에 게 자격 증명을 추가 합니다.

## 구문과

### SpObjectIdWithPasswordParameterSet (기본값)
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SpObjectIdWithCertValueParameterSet
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithCertValueParameterSet
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SPNWithPasswordParameterSet
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectWithCertValueParameterSet
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipalObjectWithPasswordParameterSet
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
New-AzADSpCredential cmdlet을 사용 하 여 새 자격 증명을 추가 하거나 서비스 사용자를 위해 자격 증명을 롤백할 수 있습니다.
서비스 사용자는 개체 id 또는 서비스 사용자 이름 중 하나를 제공 하 여 식별 됩니다.

## 예제의

### 예제 1-생성 된 암호를 사용 하 여 새 서비스 사용자 자격 증명 만들기

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

새 암호 자격 증명이 개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 기존 서비스 계정에 추가 됩니다.

### 예제 2-인증서를 사용 하 여 새 서비스 사용자 자격 증명 만들기

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

제공 된 base64로 인코딩된 공개 X509 인증서 ("myapp.exe")는 해당 SPN을 사용 하 여 기존 서비스 주체에 추가 됩니다.

### 예제 3-파이핑을 사용 하 여 새 서비스 사용자 자격 증명 만들기

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

개체 id가 ' 1f99cf81-0146-4f4e-beae-2007d0668476 ' 인 서비스 사용자를 가져오고 생성 된 암호를 사용 하 여 해당 서비스 사용자에 대 한 새 서비스 사용자 자격 증명을 만들기 위해 New-AzADSpCredential에 대 한 파이프를 가져옵니다.

## 변수

### -CertValue
"비대칭" 자격 증명 형식의 값입니다.
Base 64 인코딩된 인증서를 나타냅니다.

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndDate
자격 증명 사용의 유효 종료 날짜입니다.
기본 끝 날짜 값은 오늘부터 1 년입니다.
"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 이전으로 설정 해야 합니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ObjectId
자격 증명을 추가할 서비스 주체의 개체 id입니다.

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalName
자격 증명을 추가할 서비스 주체의 이름 (SPN)입니다.

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServicePrincipalObject
자격 증명을 추가할 서비스 사용자 개체입니다.

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -시작 날짜
자격 증명 사용의 유효 시작 날짜입니다.
기본 시작 날짜 값은 오늘입니다.
"비대칭" 형식 자격 증명의 경우 X509 인증서가 유효한 날짜 또는 그 이후에이를 설정 해야 합니다.

```yaml
Type: System.DateTime
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
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### ActiveDirectory PSADServicePrincipal

### 시스템. 날짜/시간

## 출력

### ActiveDirectory Adcredential 자격 증명

### Microsoft. a. PSADCredentialWrapper

## 상속자

## 관련 링크

[Get-AzADSpCredential](./Get-AzADSpCredential.md)

[제거-AzADSpCredential](./Remove-AzADSpCredential.md)

[Get-AzADServicePrincipal](./Get-AzADServicePrincipal.md)



