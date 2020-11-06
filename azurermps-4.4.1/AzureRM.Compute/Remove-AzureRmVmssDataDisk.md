---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: b32734bbca2ec0fd554a073b2e0b5acf077874ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525636"
---
# Remove-AzureRmVmssDataDisk

## SYNOPSIS
VMSS에서 데이터 디스크를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### NameParameterSet
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### LunParameterSet
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVmssDataDisk** CMDLET은 Vmss (가상 컴퓨터 배율 집합) 인스턴스에서 데이터 디스크를 제거 합니다.

## 예제의

### 예제 1
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

이 명령은 VMSS 개체에서 이름이 ' DataDisk1 ' 인 데이터 디스크를 제거 합니다.

### 예제 2
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거 합니다.

## 변수

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

### -Lun
디스크의 논리 단위 번호를 지정 합니다.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
디스크의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS 개체를 지정 합니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### VirtualMachineScaleSet를 통해 계산 합니다.
System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]

## 출력

### VirtualMachineScaleSet를 통해 계산 합니다.

## 상속자

## 관련 링크

