---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7EC166C7-151D-4DA0-9B10-165E735D4F12
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssExtension.md
ms.openlocfilehash: 20446fc7c93000b29680689001d9e3c40c4862e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525344"
---
# Add-AzureRmVmssExtension

## SYNOPSIS
VMSS에 확장을 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [[-Publisher] <String>] [[-Type] <String>] [[-TypeHandlerVersion] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [[-Setting] <Object>] [[-ProtectedSetting] <Object>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**추가-AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에 확장을 추가 합니다.

## 예제의

### 예제 1: VMSS에 확장 추가
```
PS C:\> Add-AzureRmVmssExtension -VirtualMachineScaleSet $VMSS -Name $ExtName -Publisher $Publisher -Type $ExtType -TypeHandlerVersion $ExtVer -AutoUpgradeMinorVersion $True
```

이 명령은 VMMS에 확장을 추가 합니다.

## 변수

### -AutoUpgradeMinorVersion
확장 버전이 새 부 버전으로 자동 업데이트 되어야 하는지 여부를 나타냅니다.

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ProtectedSetting
확장에 대 한 개인 구성을 문자열로 지정 합니다.
이 cmdlet은 개인 구성을 암호화 합니다.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Publisher
확장 게시자의 이름을 지정 합니다.
게시자는 확장명을 등록할 때 이름을 제공 합니다.
이는 [AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md) cmdlet을 사용 하 여 게시자를 가져올 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -설정
공용 구성을 해당 확장명에 대 한 문자열로 지정 합니다.
이 cmdlet은 공용 구성을 암호화 하지 않습니다.

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
확장명 유형을 지정 합니다.
[AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md) cmdlet을 사용 하 여 확장 형식을 가져올 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.
[AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md) cmdlet을 사용 하 여 확장 버전을 가져올 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSet
VMSS 개체를 지정 합니다.
[New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) 를 사용 하 여 개체를 만들 수 있습니다.

```yaml
Type: VirtualMachineScaleSet
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다. Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
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

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

###  
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[제거-AzureRmVmssExtension](./Remove-AzureRmVmssExtension.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMExtensionImageType](./Get-AzureRmVMExtensionImageType.md)

[Get-AzureRmVMExtensionImage](./Get-AzureRmVMExtensionImage.md)

[새로운 AzureRmVmssConfig](./New-AzureRmVmssConfig.md)
