---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: a8ac31efd77d5b8ff5c07920bb14b44f80ac0955
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877063"
---
# Get-AzVMExtension

## SYNOPSIS
가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.

## 구문과

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVMExtension** cmdlet은 가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.
속성을 가져올 확장명의 이름을 지정 합니다.
확장의 인스턴스 보기만 가져오려면 Status 매개 변수를 지정 합니다.

## 예제의

### 예제 1: 확장의 속성 가져오기
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"
```

이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 속성을 가져옵니다.

### 예제 2: 확장의 인스턴스 뷰 가져오기
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status
```

이 명령은 리소스 그룹 ResourceGroup11에 있는 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 인스턴스 보기를 가져옵니다.

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

### -이름
확장명의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 확장에 대 한 속성을 가져옵니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
가상 컴퓨터의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에서 확장의 속성을 가져옵니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
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

### Microsoft. a. PSVirtualMachineExtension

## 상속자

## 관련 링크

[제거-AzVMExtension](./Remove-AzVMExtension.md)

[Set-AzVMExtension](./Set-AzVMExtension.md)


