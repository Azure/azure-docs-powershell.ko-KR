---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 69FBF1E7-E69A-42B5-AC17-C7CF8CAB3C9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5da323d5284de94aaadfc92abdf819f861695335
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047383"
---
# Set-WAPackVMRole

## SYNOPSIS
가상 컴퓨터 역할의 인스턴스 수 속성을 변경 합니다.

## 구문과

```
Set-WAPackVMRole -VMRole <VMRole> -InstanceCount <Int32> [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**WAPackVMRole** cmdlet은 가상 컴퓨터 역할의 인스턴스 수 속성을 변경 합니다.

## 예제의

### 예제 1: 가상 컴퓨터 역할의 인스턴스 수 지정
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Set-WAPackVMRole -VMRole $VMRole -InstanceCount 3
```

첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole01 이라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.

두 번째 및 마지막 명령은 $VMRole에 저장 된 가상 컴퓨터 역할의 새 인스턴스 수를 3으로 설정 합니다.

## 변수

### -InstanceCount
가상 컴퓨터 역할의 인스턴스 수를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: True
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

### -VMRole
가상 컴퓨터 역할을 지정 합니다.
가상 컴퓨터 역할을 얻으려면 **Get-WAPackVMRole** cmdlet을 사용 합니다.

```yaml
Type: VMRole
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

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[새로운 WAPackVMRole](./New-WAPackVMRole.md)

[제거-WAPackVMRole](./Remove-WAPackVMRole.md)


