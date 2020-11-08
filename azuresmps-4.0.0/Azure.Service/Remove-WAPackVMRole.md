---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 9999E0EE-4A32-4C18-A6EC-2A073DC08710
online version: ''
schema: 2.0.0
ms.openlocfilehash: e5dfe0f42987ba51613ff9bafa000713456dfaf7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047411"
---
# Remove-WAPackVMRole

## SYNOPSIS
가상 컴퓨터 역할 개체를 제거 합니다.

## 구문과

### FromVMRoleObject (기본값)
```
Remove-WAPackVMRole -VMRole <VMRole> [-PassThru] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### FromCloudService
```
Remove-WAPackVMRole -VMRole <VMRole> -CloudServiceName <String> [-PassThru] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
이러한 항목은 더 이상 사용 되지 않으며 향후에 제거 될 예정입니다.
이 항목에서는 0.8.1 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
Azure PowerShell 콘솔에서 사용 중인 모듈의 버전을 확인 하려면를 입력 `(Get-Module -Name Azure).Version` 합니다.

**WAPackVMRole** cmdlet은 가상 컴퓨터 역할 개체를 제거 합니다.

## 예제의

### 예제 1: WAP 포털을 사용 하 여 만든 가상 컴퓨터 역할 제거
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole01"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole
```

첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole01 이라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.

두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.
명령에서 확인 하 라는 메시지를 표시 합니다. 이 가상 컴퓨터 역할을 WAP 포털을 사용 하 여 만든 것으로 가정 하면 클라우드 서비스 이름을 지정할 필요가 없습니다.

### 예제 2: 클라우드 서비스를 수동으로 만든 후 생성 된 가상 컴퓨터 역할 제거
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole02"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -CloudServiceName "ContosoCloudService02"
```

첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 "ContosoVMRole02" 라는 가상 컴퓨터 역할을 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.

두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.
명령에서 확인 하 라는 메시지를 표시 합니다.
포털을 사용 하 여이 가상 컴퓨터 역할이 만들어지지 않았다고 가정할 경우 사용자는 클라우드 서비스 이름을 지정 해야 합니다.
이 경우에는 "ContosoCloudService02"입니다.

### 예제 3: 확인 하지 않고 가상 컴퓨터 역할 제거
```
PS C:\> $VMRole = Get-WAPackVMRole -Name "ContosoVMRole03"
PS C:\> Remove-WAPackVMRole -VMRole $VMRole -Force
```

첫 번째 명령은 **WAPackVMRole** cmdlet을 사용 하 여 ContosoVMRole03 이라는 클라우드 서비스를 가져온 다음 해당 개체를 $VMRole 변수에 저장 합니다.

두 번째 명령은 $VMRole에 저장 된 가상 컴퓨터 역할을 제거 합니다.
이 명령에는 *Force* 매개 변수가 포함 됩니다.
명령에 확인 메시지가 표시 되지 않습니다.

## 변수

### -CloudServiceName
가상 컴퓨터 역할의 클라우드 서비스 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: FromCloudService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -VMRole
가상 컴퓨터 역할을 지정 합니다.
가상 컴퓨터 역할을 얻으려면 **get-WAPackVMRole** cmdlet을 사용 합니다.

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

## 출력

## 상속자

## 관련 링크

[Get-WAPackVMRole](./Get-WAPackVMRole.md)

[새로운 WAPackVMRole](./New-WAPackVMRole.md)

[Set-WAPackVMRole](./Set-WAPackVMRole.md)


