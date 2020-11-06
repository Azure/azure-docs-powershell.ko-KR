---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525239"
---
# Update-AzureRmVmss

## SYNOPSIS
VMSS의 상태를 업데이트 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.

## 예제의

### 예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 LocalVMSS 라는 로컬 VMSS 개체의 상태로 업데이트 합니다.

## 변수

### -ResourceGroupName
VMSS가 속한 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
로컬 VMSS 개체를 지정 합니다.
VMSS 개체를 가져오려면 Get-AzureRmVmss cmdlet을 사용 합니다.
이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -VMScaleSetName
이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[새로운 AzureRmVmss](./New-AzureRmVmss.md)

[제거-AzureRmVmss](./Remove-AzureRmVmss.md)

[다시 시작-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[시작-AzureRmVmss](./Start-AzureRmVmss.md)

[중지-AzureRmVmss](./Stop-AzureRmVmss.md)


