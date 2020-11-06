---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E8C9D68E-7C68-43D0-B348-72E9713CB99F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmssInstance.md
ms.openlocfilehash: 75b8190c34d5335904d40d386cabc76e8cbf0b0f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525232"
---
# Update-AzureRmVmssInstance

## SYNOPSIS
VMSS 인스턴스의 수동 업그레이드를 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Update-AzureRmVmssInstance [-ResourceGroupName] <String> [-VMScaleSetName] <String> [-InstanceId] <String[]>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
Update-AzureRmVmssInstance cmdlet은 지정 된 VMSS (가상 컴퓨터 크기 집합) 인스턴스의 수동 업그레이드를 시작 합니다.
이는 VMSS Scale 집합의 업그레이드 정책이 수동으로 설정 된 경우에 사용 됩니다.

## 예제의

### 예제 1: VMSS 인스턴스의 업그레이드 시작
```
PS C:\> Update-AzureRmVmssInstance -ResourceGroupName "Group011" -VMScaleSetName "VMScaleSet001" -InstanceId "0"
```

이 명령은 인스턴스 ID가 0 인 VMScaleSet001 이라는 VMSS의 업그레이드를 시작 합니다.

## 변수

### -InstanceId
문자열 배열로 업그레이드할 인스턴스의 ID 또는 ID를 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS의 리소스 그룹 이름을 지정 합니다.

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

### -VMScaleSetName
이 cmdlet이 업그레이드 하는 VMSS 인스턴스의 이름을 지정 합니다.

```yaml
Type: String
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

###  
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[업데이트-AzureRmVmss](./Update-AzureRmVmss.md)


