---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 42042533-9F84-4189-8C9F-01FD62F89DC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: db14b17e42d23e481468f563768b606d8baa2802
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047406"
---
# Remove-WAPackVNet

## SYNOPSIS
가상 네트워크 개체를 제거 합니다.

## 구문과

```
Remove-WAPackVNet -VNet <VMNetwork> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**Remove-WAPackVNet** cmdlet은 가상 네트워크 개체를 제거 합니다.

## 예제의

### 예제 1: 가상화 된 네트워크 제거
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet01"
PS C:\> Remove-WAPackVM -VNet $VNet
```

첫 번째 명령은 **Get-help Apackvnet** cmdlet을 사용 하 여 ContosoVNet01 이라는 가상화 된 네트워크를 가져온 다음 해당 개체를 $VNet 변수에 저장 합니다.
두 번째 명령은 $VNet에 저장 되어 있는 가상화 된 네트워크를 제거 합니다.
명령에서 확인 하 라는 메시지를 표시 합니다.

### 예제 2: 확인 하지 않고 가상화 된 네트워크 제거
```
PS C:\> $VNet = Get-WAPackVNet -Name "ContosoVNet02"
PS C:\> Remove-WAPackVNet -VNet $VNet -Force
```

첫 번째 명령은 ContosoVNet02 ( **Get-WAPackVNet** cmdlet을 사용 하 여 명명 된 클라우드 서비스를 가져온 다음 해당 개체를 $VNet 변수에 저장 합니다.
두 번째 명령은 $VNet에 저장 되어 있는 가상화 된 네트워크를 제거 합니다.
이 명령에는 *Force* 매개 변수가 포함 됩니다.
명령에 확인 메시지가 표시 되지 않습니다.

## 변수

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -PassThru
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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

### -VNet
가상화 된 네트워크를 지정 합니다.
가상 네트워크를 얻으려면 **Get WAPackVNet** cmdlet을 사용 합니다.

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-WAPackVNet](./Get-WAPackVNet.md)

[새-WAPackVNet](./New-WAPackVNet.md)


