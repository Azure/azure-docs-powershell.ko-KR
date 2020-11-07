---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 63D48BA4-EE80-4740-90B9-0EE05B3F6536
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmssvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVmssVM.md
ms.openlocfilehash: 43c6f96556cb283ef21f24df00d6a6ddb9c5397a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877034"
---
# Get-AzVmssVM

## SYNOPSIS
VMSS 가상 컴퓨터의 속성을 가져옵니다.

## 구문과

### DefaultParameter (기본값)
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### FriendMethod
```
Get-AzVmssVM [[-ResourceGroupName] <String>] [[-VMScaleSetName] <String>] [[-InstanceId] <String>]
 [-InstanceView] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVmssVM** CMDLET은 Vmss (가상 컴퓨터 크기 집합) 가상 컴퓨터의 모델 보기와 인스턴스 보기를 가져옵니다.
모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.
인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.
가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.

## 예제의

### 예제 1: VMSS 가상 컴퓨터의 속성 가져오기
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group001" -VMScaleSetName "VMSS001"
```

이 명령은 Group001 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS001의 속성을 가져옵니다.
Command는 *Instanceview* 스위치 매개 변수를 지정 하지 않으므로 cmdlet에서 가상 컴퓨터의 모델 뷰를 가져옵니다.

### 예제 2: VMSS 가상 컴퓨터의 모델 뷰 속성 가져오기
```
PS C:\> Get-AzVmssVM -ResourceGroupName "Group002" -VMScaleSetName "VMSS004" -InstanceId $ID
```

이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.
명령은 모델 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.

### 예제 3: VMSS 가상 컴퓨터의 인스턴스 보기 속성 가져오기
```
PS C:\> Get-AzVmssVM -InstanceView  -ResourceGroupName $rgname  -VMScaleSetName $vmssName -InstanceId $ID
```

이 명령은 Group002 이라는 리소스 그룹에 속하는 VMSS 가상 컴퓨터 VMSS004의 속성을 가져옵니다.
이 명령은 *Instanceview* 스위치 매개 변수를 지정 하므로 cmdlet은 가상 컴퓨터의 인스턴스 뷰를 가져옵니다.
명령에서는 인스턴스 뷰를 가져올 변수 $ID에 저장 된 인스턴스 ID를 가져옵니다.

## 변수

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
모델 보기를 가져올 인스턴스 ID를 지정 합니다.

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

### -InstanceView
이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
VMSS의 리소스 그룹 이름을 지정 합니다.

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

### -VMScaleSetName
VMSS의 이름을 종류로 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

### 이 cmdlet은 출력을 생성 하지 않습니다.

## 상속자

## 관련 링크

[Set-AzVmssVM](./Set-AzVmssVM.md)

[Get-AzVmss](./Get-AzVmss.md)


