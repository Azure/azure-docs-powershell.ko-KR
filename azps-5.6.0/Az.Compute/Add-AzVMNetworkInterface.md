---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BF80D456-DAB1-4B51-B50F-A75C2C66A472
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMNetworkInterface.md
ms.openlocfilehash: efe587cf01fa2adf16e4b6beaaa319312f3c9fa5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969568"
---
# Add-AzVMNetworkInterface

## SYNOPSIS
가상 머신에 네트워크 인터페이스를 추가합니다.

## 구문

### GetNicFromNicId(기본값)
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine> [-Id] <String> [-Primary]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetNicFromNicObject
```
Add-AzVMNetworkInterface [-VM] <PSVirtualMachine>
 [-NetworkInterface] <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVMNetworkInterface** cmdlet은 가상 머신에 네트워크 인터페이스를 추가합니다.
가상 머신을 만들거나 기존 가상 머신에 인터페이스를 추가할 때 인터페이스를 추가할 수 있습니다.

## 예제

### 예제 1: 새 가상 머신에 네트워크 인터페이스 추가
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
```

첫 번째 명령은 가상 머신 개체를 만든 다음, 가상 머신 개체를 $VirtualMachine 변수에 저장합니다.
명령은 가상 머신에 이름과 크기를 할당합니다.
두 번째 명령은 네트워크에 저장된 가상 머신에 네트워크 인터페이스를 $VirtualMachine.

### 예제 2: 기존 가상 머신에 네트워크 인터페이스 추가
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzVMNetworkInterface -VM $VirtualMachine -Id "/subscriptions/46fc8ea4-2de6-4179-8ab1-365da4121af4/resourceGroups/contoso/providers/Microsoft.Network/networkInterfaces/sshNIC"
PS C:\> Update-AzVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.
명령은 가상 머신을 $VirtualMachine 저장합니다.
두 번째 명령은 네트워크에 저장된 가상 머신에 네트워크 인터페이스를 $VirtualMachine.
마지막 명령은 ResourceGroup11에 저장된 가상 머신의 $VirtualMachine 업데이트합니다.

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

### -Id
가상 머신에 추가할 네트워크 인터페이스의 ID를 지정합니다.
[Get-AzNetworkInterface](/powershell/module/az.network/get-aznetworkinterface) cmdlet을 사용하여 네트워크 인터페이스를 얻을 수 있습니다.

```yaml
Type: System.String
Parameter Sets: GetNicFromNicId
Aliases: NicId, NetworkInterfaceId

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NetworkInterface
네트워크 인터페이스를 지정합니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference]
Parameter Sets: GetNicFromNicObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Primary
이 cmdlet은 네트워크 인터페이스를 기본 인터페이스로 추가하고 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetNicFromNicId
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
네트워크 인터페이스를 추가할 로컬 가상 머신 개체를 지정합니다.
가상 머신을 만들 경우 **New-AzVMConfig** cmdlet을 사용하세요.
기존 가상 머신을 얻은 경우 **Get-AzVM** cmdlet을 사용하세요.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## 입력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

### System.Collections.Generic.List'1[[Microsoft.Azure.Management.Internal.Network.Common.INetworkInterfaceReference, Microsoft.Azure.PowerShell.Clients.Network, Version=1.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## 참고 사항

## 관련 링크

[New-AzVMConfig](./New-AzVMConfig.md)

[Get-AzVM](./Get-AzVM.md)

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)
