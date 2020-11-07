---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6250EC11-79CF-428B-A72F-9BD72C1751F0
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVM.md
ms.openlocfilehash: 2f33b0dbee4f584553eac1047471adef08e3523b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877080"
---
# Get-AzVM

## SYNOPSIS
가상 컴퓨터의 속성을 가져옵니다.

## 구문과

### ListAllVirtualMachinesParamSet (기본값)
```
Get-AzVM [-Status] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Status] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetVirtualMachineInResourceGroupParamSet
```
Get-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Status] [-DisplayHint <DisplayHintType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ListNextLinkVirtualMachinesParamSet
```
Get-AzVM [-Status] [-NextLink] <Uri> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVM** Cmdlet은 Azure 가상 컴퓨터의 모델 뷰 및 인스턴스 뷰를 가져옵니다.
모델 보기는 가상 컴퓨터의 사용자 지정 속성입니다.
인스턴스 보기는 가상 컴퓨터의 인스턴스 수준 상태입니다.
가상 컴퓨터의 인스턴스 보기만 가져오려면 *Status* 매개 변수를 지정 합니다.

## 예제의

### 예제 1: 모델 및 인스턴스 보기 속성 가져오기
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 모델 보기 및 인스턴스 보기 속성을 가져옵니다.

### 예제 2: 인스턴스 뷰 속성 가져오기
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Status
```

이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 속성을 가져옵니다.
이 명령은 *Status* 매개 변수를 지정 합니다.
따라서이 명령은 인스턴스 보기 속성만 가져옵니다.

### 예제 3: 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성 가져오기
```
PS C:\> Get-AzVM -ResourceGroupName "ResourceGroup11"
```

이 명령은 ResourceGroup11 이라는 리소스 그룹의 모든 가상 컴퓨터에 대 한 속성을 가져옵니다.

### 예제 4: 구독에서 모든 가상 컴퓨터 가져오기
```
PS C:\> Get-AzVM
```

이 명령은 구독에 있는 모든 가상 컴퓨터를 가져옵니다.

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

### -DisplayHint
가상 컴퓨터 개체를 표시 하는 방법을 결정 합니다.

유효한 값은 다음과 같습니다.

--Compact: 최상위 수준 속성만 표시 합니다.

--확장: 모든 수준의 모든 속성을 표시 합니다.
```yaml
Type: DisplayHintType
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: 
Accepted values: Compact, Expand

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
가져올 가상 컴퓨터의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GetVirtualMachineInResourceGroupParamSet
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NextLink
다음 링크를 지정 합니다.

```yaml
Type: Uri
Parameter Sets: ListNextLinkVirtualMachinesParamSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ListVirtualMachineInResourceGroupParamSet, GetVirtualMachineInResourceGroupParamSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
이 cmdlet이 가상 컴퓨터의 인스턴스 보기만을 가져옵니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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

### PSVirtualMachine를 계산 합니다.

### Microsoft. a. PSVirtualMachineInstanceView

## 상속자

## 관련 링크

[새로운 AzVM](./New-AzVM.md)

[제거-AzVM](./Remove-AzVM.md)

[다시 시작-AzVM](./Restart-AzVM.md)

[시작-AzVM](./Start-AzVM.md)

[중지-AzVM](./Stop-AzVM.md)

[업데이트-AzVM](./Update-AzVM.md)


