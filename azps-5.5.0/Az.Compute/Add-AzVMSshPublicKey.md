---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199353"
---
# Add-AzVMSshPublicKey

## SYNOPSIS
VM을 만들 때만 가상 머신에 대한 SSH에 대한 공개 키를 추가합니다.

## 구문

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVMSshPublicKey** cmdlet은 SSH(Secure Shell)를 통해 Linux 가상 머신에 연결하는 데 사용할 수 있는 공개 키를 추가합니다. 이 명령은 VM을 생성한 후 사용할 수 없습니다. Update-AzVM 없이 VM을 생성한 후에 이 명령을 사용하려고 하면 오류가 없습니다. Update-AzVM과 함께 명령을 사용하는 경우 명령이 오류가 발생합니다.

## 예제

### 예제 1: 가상 머신에 공개 키 추가
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.
이 명령은 가상 머신을 $VirtualMachine 저장합니다.
두 번째 명령은 Path 매개 변수가 지정하는 VirtualMachine07의 위치에 공개 키를 추가합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -KeyData
공개 키의 기본 64 인코딩을 지정합니다.
SSH를 사용하거나 이 매개 변수가 지정하는 키를 사용하여 Linux 가상 머신에 연결할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
이 cmdlet이 SSH 공개 키를 저장하는 가상 머신에서 파일의 전체 경로를 지정합니다.
파일이 이미 있는 경우 이 cmdlet은 파일에 키를 추가합니다.

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

### -VM
이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.
가상 머신 개체를 얻습니다. [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.
[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

### System.String

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine

## 참고 사항

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)
