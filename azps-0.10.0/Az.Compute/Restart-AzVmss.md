---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVmss.md
ms.openlocfilehash: b0e01f462bfb7576e942138cb42b3171fb6660b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876924"
---
# Restart-AzVmss

## SYNOPSIS
Vmss 또는 VMSS 내의 가상 컴퓨터를 다시 시작 합니다.

## 구문과

```
Restart-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzVmss** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)를 다시 시작 합니다.
이 cmdlet은 *InstanceId* 매개 변수를 사용 하 여 vmss 내부의 특정 가상 컴퓨터를 다시 시작 하는 데도 사용할 수 있습니다.

## 예제의

### 예제 1: VMSS 다시 시작
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS001 라는 VMSS를 다시 시작 합니다.

### 예제 2: VMSS 내에서 특정 가상 컴퓨터 다시 시작
```
PS C:\> Restart-AzVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 인 VMSS001 이라는 인스턴스 ID가 1 인 가상 컴퓨터를 다시 시작 합니다.

## 변수

### -AsJob
백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.

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

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InstanceId
다시 시작 해야 하는 인스턴스의 ID를 문자열 배열로 지정 합니다.

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
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
이 cmdlet이 다시 시작 하는 VMSS의 이름을 종류에 게 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

###  
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[Get-AzVmss](./Get-AzVmss.md)

[새로운 AzVmss](./New-AzVmss.md)

[제거-AzVmss](./Remove-AzVmss.md)

[Set-AzVmss](./Set-AzVmss.md)

[시작-AzVmss](./Start-AzVmss.md)

[중지-AzVmss](./Stop-AzVmss.md)

[업데이트-AzVmss](./Update-AzVmss.md)


