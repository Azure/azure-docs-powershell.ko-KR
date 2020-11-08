---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 3CD1A989-902C-48B3-81E9-7B78EDA5F880
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7003abf263fd4c669956f65c990246295cf7158d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045870"
---
# Remove-AzureAccount

## SYNOPSIS
Windows PowerShell에서 Azure 계정을 삭제 합니다.

## 구문과

```
Remove-AzureAccount -Name <String> [-Force] [-PassThru] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**제거-AzureAccount** cmdlet은 로밍 사용자 프로필의 구독 데이터 파일에서 Azure 계정 및 해당 구독을 삭제 합니다.
Microsoft Azure에서 계정을 삭제 하거나 실제 계정이 어떤 방식으로든 변경 되지 않습니다.

이 cmdlet을 사용 하는 것은 Azure 계정에서 로그 아웃 하는 것과 매우 유사 합니다.
계정에 다시 로그인 하려는 경우 **-azureaccount** 또는 **가져오기-Azureaccount 설정 파일** 을 사용 하 여 Windows PowerShell에 계정을 다시 추가 합니다.

또한 Azure PowerShell cmdlet에서 Azure 계정으로 로그인 하는 방식을 변경 하는 데 **-AzureAccount** cmdlet을 사용할 수 있습니다.
계정에 **가져오기-Azure# settingsfile** 의 관리 인증서와 **추가-azureaccount** 의 액세스 토큰이 모두 있는 경우 Azure PowerShell cmdlet은 액세스 토큰만 사용 합니다. 관리 인증서를 무시 합니다.
관리 인증서를 사용 하려면 **제거-AzureAccount** 를 실행 합니다.
**-AzureAccount** 가 관리 인증서와 액세스 토큰을 모두 찾으면 계정을 삭제 하는 대신 액세스 토큰만 삭제 합니다.
관리 인증서가 여전히 남아 있으므로 Windows PowerShell에서 계정을 계속 사용할 수 있습니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 계정 제거
```
PS C:\> Remove-AzureAccount -Name admin@contoso.com
```

이 명령은 admin@contoso.com 구독 데이터 파일에서를 제거 합니다.
명령이 완료 되 면 Windows PowerShell에서 해당 계정을 더 이상 사용할 수 없습니다.

## 변수

### -Force
확인 메시지를 표시 하지 않습니다.
기본적으로 **-Azureaccount 제거** 는 Windows PowerShell에서 계정을 제거 하기 전에 확인 메시지를 표시 합니다.

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

### -이름
제거할 계정의 이름을 지정 합니다.
매개 변수 값은 대/소문자를 구분 합니다.
와일드 카드 문자는 지원 되지 않습니다.

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

### -PassThru
명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.
기본적으로이 cmdlet은 출력을 반환 하지 않습니다.

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

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
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
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### 없음 또는 시스템 부울
*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.
그렇지 않으면 출력을 반환 하지 않습니다.

## 상속자

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[Get-AzureAccount](./Get-AzureAccount.md)


