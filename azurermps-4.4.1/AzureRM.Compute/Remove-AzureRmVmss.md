---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F2EE87-97C4-416A-9AE1-9FBD72062F0F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmss.md
ms.openlocfilehash: 703fc0d83fb17e1131c44cbd06593887ebcce020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525639"
---
# Remove-AzureRmVmss

## SYNOPSIS
Vmss 또는 VMSS 내에 있는 가상 컴퓨터를 제거 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Remove-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVmss** Cmdlet은 AZURE에서 Vmss (가상 컴퓨터 크기 집합)를 제거 합니다.
이 cmdlet을 사용 하 여 VMSS 내의 특정 가상 컴퓨터를 제거할 수도 있습니다.
*InstanceId* 매개 변수를 사용 하 여 vmss 내의 특정 가상 컴퓨터를 제거할 수 있습니다.

## 예제의

### 예제 1: VMSS 제거
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMScaleSet001"
```

이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS 인 VMScaleSet001를 제거 합니다.

### 예제 2: VMSS 내에서 가상 컴퓨터 제거
```
PS C:\> Remove-AzureRmVmss -ResourceGroupName "Group002" -VMScaleSetName "VMScaleSet002" -InstanceId "3";
```

이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 인 VMScaleSet002 이라는 인스턴스 ID가 3 인 가상 컴퓨터를 제거 합니다.

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

### -InstanceId
시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.
예를 들면 다음과 같습니다. `-InstanceId "0", "3"`

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS가 속한 리소스 그룹의 이름을 지정 합니다.

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

### -VMScaleSetName
이 cmdlet이 제거 하는 VMSS의 이름을 종류로 합니다.
*InstanceId* 매개 변수를 지정 하면 cmdlet이이 매개 변수로 명명 된 vmss에서 지정 된 가상 컴퓨터를 제거 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[새로운 AzureRmVmss](./New-AzureRmVmss.md)

[다시 시작-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[시작-AzureRmVmss](./Start-AzureRmVmss.md)

[중지-AzureRmVmss](./Stop-AzureRmVmss.md)

[업데이트-AzureRmVmss](./Update-AzureRmVmss.md)


