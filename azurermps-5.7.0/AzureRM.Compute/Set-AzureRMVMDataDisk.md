---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C453485D-67A7-480E-83F6-527D4F5EBC93
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMDataDisk.md
ms.openlocfilehash: 2f961f144bc322cb1b1b12001ed006bc783ed67e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531753"
---
# Set-AzureRmVMDataDisk

## SYNOPSIS
가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ChangeWithName
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Name] <String> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

### ChangeWithLun
```
Set-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [-Lun] <Int32> [[-Caching] <CachingTypes>]
 [[-DiskSizeInGB] <Int32>] [<CommonParameters>]
```

## 설명은
**AzureRmVMDataDisk** cmdlet은 가상 컴퓨터 데이터 디스크의 속성을 수정 합니다.

## 예제의

### 예제 1: 데이터 디스크의 캐싱 모드 수정
```
PS C:\> $VM = Get-AzureRMVM -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
PS C:\> Set-AzureRmVMDataDisk -VM $VM -Name "DataDisk01" -Caching ReadWrite | Update-AzureRmVM
```

첫 번째 명령은 **Get-AzureRmVM** 를 사용 하 여 ContosoVM07 이라는 가상 컴퓨터를 가져옵니다.
명령이 $VM 변수에 저장 합니다.

두 번째 명령은 $VM의 가상 컴퓨터에서 DataDisk01 이라는 데이터 디스크에 대 한 캐싱 모드를 수정 합니다.
이 명령은 결과를 변경 내용을 구현 하는 Update-AzureRmVM cmdlet에 전달 합니다.
캐싱 모드를 변경 하면 가상 컴퓨터가 다시 시작 됩니다.

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

### -VM
이 cmdlet이 데이터 디스크를 수정할 가상 컴퓨터를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 Get-AzureRmVM cmdlet을 사용 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
이 cmdlet은 입력을 허용 하지 않습니다.

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVM](./Get-AzureRmVM.md)

[업데이트-AzureRmVM](./Update-AzureRmVM.md)


