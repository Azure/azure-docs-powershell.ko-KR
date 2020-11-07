---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMDataDisk.md
ms.openlocfilehash: b927e9b61e4d76795e35f2356b900b959a94e082
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876873"
---
# Set-AzVMDataDisk

## SYNOPSIS
가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.

## 구문과

### ChangeWithName
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.

## 예제의

### 예제 1: 데이터 디스크의 캐싱 모드 수정
```
PS C:\> $VM = Get-AzVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzVM
```

첫 번째 명령은 **Get-AzVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.
명령이 $VM 변수에 저장 합니다.

두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.
이 명령은 결과를 변경 내용을 구현 하는 Update-AzVM cmdlet에 전달 합니다.
Cashing mode를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.

## 변수

### -캐싱
디스크의 캐싱 모드를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 읽기
- 쓰기

기본값은 ReadWrite입니다.
이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.

이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -DiskSizeInGB
데이터 디스크의 크기 (기가바이트)를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
이 cmdlet이 수정 하는 데이터 디스크의 LUN (논리 단위 번호)을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: ChangeWithLun
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
이 cmdlet이 수정 하는 데이터 디스크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ChangeWithName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
가상 컴퓨터 관리 디스크의 계정 유형입니다.

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### PSVirtualMachine
' VM ' 매개 변수는 파이프라인에서 ' PSVirtualMachine ' 형식의 값을 허용 합니다.

## 출력

### PSVirtualMachine를 계산 합니다.

## 상속자

## 관련 링크

[Get-AzVM](./Get-AzVM.md)

[업데이트-AzVM](./Update-AzVM.md)


