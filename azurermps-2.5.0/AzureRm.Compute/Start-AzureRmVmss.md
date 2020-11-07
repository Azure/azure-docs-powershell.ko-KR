---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2135b6244453cb7d958871c23b64016404d02502
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882650"
---
# Start-AzureRmVmss

## SYNOPSIS
Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 시작 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 시작 합니다.
*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.

## 예제의

### 예제 1: VMSS 내에서 가상 컴퓨터의 특정 집합 시작
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열에 지정 된 가상 컴퓨터의 특정 집합을 시작 합니다.

### 예제 2: VMSS 내의 모든 가상 컴퓨터 시작
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

이 명령은 ContosoVMSS 이라는 VMSS에 속하는 모든 가상 컴퓨터를 시작 합니다.

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
Cmdlet이 시작 되는 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.
예를 들면 다음과 같습니다. `-InstanceId "0", "3"`

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
이 cmdlet이 가상 컴퓨터를 시작 하는 VMSS의 이름을 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

###  
이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[Get-AzureRmVmss](./Get-AzureRmVmss.md)

[새로운 AzureRmVmss](./New-AzureRmVmss.md)

[제거-AzureRmVmss](./Remove-AzureRmVmss.md)

[다시 시작-AzureRmVmss](./Restart-AzureRmVmss.md)

[Set-AzureRmVmss](./Set-AzureRmVmss.md)

[중지-AzureRmVmss](./Stop-AzureRmVmss.md)

[업데이트-AzureRmVmss](./Update-AzureRmVmss.md)


