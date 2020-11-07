---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B7A675D3-EF79-4EE2-9330-D4C690739006
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsize
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMSize.md
ms.openlocfilehash: 2ac1e336161d4cfad1bbef37ec98716456a8143c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697424"
---
# Get-AzVMSize

## SYNOPSIS
사용할 수 있는 가상 컴퓨터 크기를 가져옵니다.

## 구문과

### ListVirtualMachineSizeParamSet (기본값)
```
Get-AzVMSize [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForAvailabilitySet
```
Get-AzVMSize [-ResourceGroupName] <String> [-AvailabilitySetName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListAvailableSizesForVirtualMachine
```
Get-AzVMSize [-ResourceGroupName] <String> [-VMName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**Get-AzVMSize** cmdlet은 사용 가능한 가상 컴퓨터 크기를 가져옵니다.

## 예제의

### 예제 1: 위치에 대 한 가상 컴퓨터 크기 가져오기
```
PS C:\> Get-AzVMSize -Location "Central US"
```

이 명령은 지정 된 위치에서 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.

### 예제 2: 가용성 집합의 크기 가져오기
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -AvailabilitySetName "AvailabilitySet17"
```

이 명령은 AvailabilitySet17 이라는 가용성 집합에 배포할 수 있는 가상 컴퓨터에 사용할 수 있는 크기를 가져옵니다.

### 예제 3: 기존 가상 컴퓨터의 크기 가져오기
```
PS C:\> Get-AzVMSize -ResourceGroupName "ResourceGroup03" -VMName "VirtualMachine12"
```

이 명령은 VirtualMachine12 이라는 기존 가상 컴퓨터에 대해 사용 가능한 크기를 가져옵니다.
이 명령이 가져오는 크기에 맞게이 가상 컴퓨터의 크기를 조정할 수 있습니다.

## 변수

### -AvailabilitySetName
이 cmdlet에서 사용 가능한 가상 컴퓨터 크기를 가져오는 가용성 집합의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### -위치
이 cmdlet이 사용 가능한 가상 컴퓨터 크기를 가져오는 위치를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListVirtualMachineSizeParamSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForAvailabilitySet, ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
이 cmdlet이 크기를 조정할 수 있는 가상 컴퓨터 크기를 가져오는 가상 컴퓨터의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: ListAvailableSizesForVirtualMachine
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

## 출력

### PSVirtualMachineSize를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)


