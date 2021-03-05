---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 1ac6f9b17f954361d95e6855a618c7dbbf3d20f7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001787"
---
# Get-AzVmssVM

## SYNOPSIS
VMSS 가상 머신의 속성을 얻습니다.

## 구문

### DefaultParameter(기본값)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Get-AzVmssVM** cmdlet은 VMSS(Virtual Machine Scale Set) 가상 머신의 모델 보기 및 인스턴스 보기를 제공합니다.
모델 보기는 가상 머신의 사용자 지정 속성입니다.
인스턴스 보기는 가상 머신의 인스턴스 수준 상태입니다.
상태 매개 *변수를* 지정하여 가상 머신의 인스턴스 보기만 얻습니다.

## 예제

### 예제 1: VMSS 가상 머신의 속성 얻음
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

이 명령은 Group001이라는 리소스 그룹에 속하는 VMSS001이라는 VMSS 가상 머신의 속성을 얻습니다.
명령은 *InstanceView* 스위치 매개 변수를 지정하지 않습니다. cmdlet은 가상 머신의 모델 보기를 얻습니다.

### 예제 2: VMSS 가상 머신의 모델 보기 속성 얻음
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.
명령은 모델 보기를 얻을 수 $ID 변수에 저장된 인스턴스 ID를 얻습니다.

### 예제 3: VMSS 가상 머신의 인스턴스 보기 속성 얻음
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

이 명령은 Group002라는 리소스 그룹에 속하는 VMSS004라는 VMSS 가상 머신의 속성을 얻습니다.
명령은 *InstanceView* 스위치 매개 변수를 지정하기 때문에 cmdlet은 가상 머신의 인스턴스 보기를 얻습니다.
명령은 인스턴스 보기를 얻을 수 있는 $ID 변수에 저장된 인스턴스 ID를 얻습니다.

## 매개 변수

### -DefaultProfile
Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -InstanceId
모델 보기를 얻을 인스턴스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -InstanceView
이 cmdlet은 가상 머신의 인스턴스 보기만 얻게 됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMScaleSetName
VMSS의 이름을 종으로 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## 참고 사항

## 관련 링크

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


