---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 53BD6ED4-EA66-448B-8B18-F078C0738AF5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 90f02a261dc804f46a7ef503879a8ce9f43fad35
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047400"
---
# New-WAPackQuickVM

## SYNOPSIS
템플릿을 기반으로 가상 컴퓨터를 만듭니다.

## 구문과

```
New-WAPackQuickVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**새-WAPackQuickVM** cmdlet은 템플릿을 기반으로 가상 컴퓨터를 만듭니다.

## 예제의

### 예제 1: 템플릿을 기반으로 가상 컴퓨터 만들기
```
PS C:\> $Credentials = Get-Credential
PS C:\> $TemplateId = Get-WAPackVMTemplate -Id 66242D17-189F-480D-87CF-8E1D749998C8
PS C:\> New-WAPackQuickVM -Name "VirtualMachine023" -Template $TemplateId -VMCredential $Credentials
```

첫 번째 명령은 **PSCredential** 개체를 만든 다음 $Credentials 변수에 저장 합니다.
Cmdlet에서 계정과 암호를 묻는 메시지를 표시 합니다.
자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.

두 번째 명령은 **WAPackVMTemplate** cmdlet을 사용 하 여 템플릿을 가져옵니다.
명령은 서식 파일의 ID를 지정 합니다.
명령이 $TemplateID 변수에 템플릿 개체를 저장 합니다.

마지막 명령은 VirtualMachine023 이라는 가상 컴퓨터를 만듭니다.
명령은 $TemplateId에 저장 된 서식 파일의 가상 컴퓨터를 기준으로 합니다.

## 변수

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
템플릿 개체를 가져오려면 **WAPackVMTemplate** cmdlet을 사용 합니다.

```yaml
Type: VMTemplate
Parameter Sets: (All)
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
Parameter Sets: (All)
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

[새-WAPackVM](./New-WAPackVM.md)

[Get-WAPackVMTemplate](./Get-WAPackVMTemplate.md)


