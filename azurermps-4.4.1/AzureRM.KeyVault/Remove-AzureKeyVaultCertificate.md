---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537152"
---
# Remove-AzureKeyVaultCertificate

## SYNOPSIS
키 자격 증명 모음에서 인증서를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureKeyVaultCertificate** cmdlet은 키 자격 증명 모음에서 인증서를 제거 합니다.

## 예제의

### 예제 1: 인증서 제거
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

이 명령은 ContosoKV01 이라는 키 자격 증명 모음에서 SelfSigned01 이라는 인증서를 제거 합니다.
이 명령은 *Force* 매개 변수를 지정 합니다.
따라서 cmdlet에서 확인 메시지가 표시 되지 않습니다.

### 예제 3: 키 자격 증명 모음에서 삭제 된 인증서 영구 제거
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 ' MyCert ' 인증서를 영구적으로 제거 합니다.
이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며,이는 이전에이 키 보관소의 사용자에 게 명시적으로 부여 된 것 이어야 합니다.

## 변수

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InRemovedState
있는 경우 이전에 삭제 된 인증서를 영구적으로 제거 합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
이 cmdlet이 키 자격 증명 모음에서 제거할 인증서의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 인증서의 FQDN (정규화 된 도메인 이름)을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VaultName
이 cmdlet이 인증서를 제거할 키 보관소의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### Microsoft. KeyVault.-모델-CertificateBundle

## 상속자

## 관련 링크

[추가-AzureKeyVaultCertificate](./Add-AzureKeyVaultCertificate.md)

[Get-AzureKeyVaultCertificate](./Get-AzureKeyVaultCertificate.md)

[가져오기-AzureKeyVaultCertificate](./Import-AzureKeyVaultCertificate.md)

[실행 취소-AzureKeyVaultCertificateRemoval](./Undo-AzureKeyVaultCertificateRemoval.md)
