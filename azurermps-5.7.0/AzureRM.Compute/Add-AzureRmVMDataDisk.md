---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 169E6694-82CD-4FCB-AB3D-E8A74001B8DB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMDataDisk.md
ms.openlocfilehash: 7566c1ef5c8e9cbf2134bc18b3aecf37d9f88bed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529027"
---
# Add-AzureRmVMDataDisk

## SYNOPSIS
가상 컴퓨터에 데이터 디스크를 추가 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmVMDataDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-DiskSizeInGB] <Int32>] [-Lun] <Int32> [-CreateOption] <DiskCreateOptionTypes>
 [[-SourceImageUri] <String>] [[-ManagedDiskId] <String>] [[-StorageAccountType] <StorageAccountTypes>]
 [<CommonParameters>]
```

## 설명은
**추가-AzureRmVMDataDisk** cmdlet은 가상 컴퓨터에 데이터 디스크를 추가 합니다.
가상 컴퓨터를 만들 때 데이터 디스크를 추가 하거나 기존 가상 컴퓨터에 데이터 디스크를 추가할 수 있습니다.

## 예제의

### 예제 1: 새 가상 컴퓨터에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskVhdUri01 = "https://contoso.blob.core.windows.net/test/data1.vhd"
PS C:\> $DataDiskVhdUri02 = "https://contoso.blob.core.windows.net/test/data2.vhd"
PS C:\> $DataDiskVhdUri03 = "https://contoso.blob.core.windows.net/test/data3.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk1' -Caching 'ReadOnly' -DiskSizeInGB 10 -Lun 0 -VhdUri $DataDiskVhdUri01 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk2' -Caching 'ReadOnly' -DiskSizeInGB 11 -Lun 1 -VhdUri $DataDiskVhdUri02 -CreateOption Empty
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name 'DataDisk3' -Caching 'ReadOnly' -DiskSizeInGB 12 -Lun 2 -VhdUri $DataDiskVhdUri03 -CreateOption Empty
```

첫 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.

다음 세 개의 명령은 1 개의 데이터 디스크 경로를 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03 변수에 할당 합니다.
이 방법은 다음 명령에 대 한 읽기 전용입니다.

마지막 세 개의 명령은 모두 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.
명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.
각 디스크의 URI는 $DataDiskVhdUri 01, $DataDiskVhdUri 02 및 $DataDiskVhdUri 03에 저장 됩니다.

### 예제 2: 기존 가상 컴퓨터에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -VhdUri "https://contoso.blob.core.windows.net/vhds/diskstandard03.vhd" -LUN 0 -Caching ReadOnly -DiskSizeinGB 1 -CreateOption Empty
PS C:\> Update-AzureRmVM -ResourceGroupName "ResourceGroup11" -VM $VirtualMachine
```

첫 번째 명령은 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.
명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.

두 번째 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.

마지막 명령은 ResourceGroup11의 $VirtualMachine에 저장 된 가상 컴퓨터의 상태를 업데이트 합니다.

### 예제 3: 일반화 된 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataImageUri = "https://contoso.blob.core.windows.net/system/Microsoft.Compute/Images/captured/dataimage.vhd"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "disk1" -SourceImageUri $DataImageUri -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption FromImage
```

첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.

다음 두 명령은 데이터 이미지 및 데이터 디스크에 대 한 경로를 $DataImageUri 및 $DataDiskUri 변수에 각각 할당 합니다.
이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.

마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.
명령은 디스크의 이름과 다른 디스크의 속성에 대 한 위치를 지정 합니다.

### 예제 4: 특수 사용자 이미지의 새 가상 컴퓨터에 데이터 디스크 추가
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1"
PS C:\> $DataDiskUri = "https://contoso.blob.core.windows.net/test/datadisk.vhd"
PS C:\> $VirtualMachine = Add-AzureRmVMDataDisk -VM $VirtualMachine -Name "dd1" -VhdUri $DataDiskUri -Lun 0 -DiskSizeinGB 10 -CreateOption Attach
```

첫 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.

다음 명령은 데이터 디스크의 경로를 $DataDiskUri 변수에 할당 합니다.
이 접근 방식은 다음 명령의 가독성을 개선 하는 데 사용 됩니다.

마지막 명령은 $VirtualMachine에 저장 된 가상 컴퓨터에 데이터 디스크를 추가 합니다.
명령은 디스크의 이름과 위치, 그리고 디스크의 다른 속성을 지정 합니다.

## 변수

### -캐싱
디스크의 캐싱 모드를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 읽기
- 쓰기
- 않아야

기본값은 ReadWrite입니다.
이 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.

이 설정은 디스크의 일관성 및 성능에 영향을 줍니다.

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만들거나, 빈 디스크를 만들거나, 기존 디스크를 연결 하는지 여부를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 붙일.
특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.
이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.
*VhdUri* 는 가상 컴퓨터에 데이터 디스크로 연결할 VHD (가상 하드 디스크)의 위치를 Azure platform에 알리기 위해 필요 합니다.
- 비울.
빈 데이터 디스크를 만들려면이를 지정 합니다.
- FromImage.
일반화 된 이미지 또는 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.
이 옵션을 지정 하는 경우 데이터 디스크로 연결할 VHD의 위치를 Azure platform에 알려 주는 데에도 *Sourceimageuri* 매개 변수를 지정 해야 합니다.
*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장 될 위치를 식별 하는 위치로 사용 됩니다.

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiskSizeInGB
가상 컴퓨터에 연결할 빈 디스크의 크기 (기가바이트)를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
데이터 디스크에 대 한 LUN (논리 단위 번호)을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
관리 디스크의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
추가할 데이터 디스크의 이름을 지정 합니다.

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

### -SourceImageUri
이 cmdlet이 연결 하는 디스크의 원본 URI를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
관리 되는 디스크의 저장소 계정 유형을 지정 합니다.

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VhdUri
플랫폼 이미지 또는 사용자 이미지를 사용할 때 만들 VHD (가상 하드 디스크) 파일에 대 한 URI (Uniform Resource Identifier)를 지정 합니다.
이 cmdlet은 이미지 blob (이진 대형 개체)를이 위치로 복사 합니다.
가상 컴퓨터를 시작할 위치입니다.

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

### -VM
데이터 디스크를 추가할 로컬 가상 컴퓨터 개체를 지정 합니다.
**Get-AzureRmVM** cmdlet을 사용 하 여 가상 컴퓨터 개체를 가져올 수 있습니다.
**새 AzureRmVMConfig** cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.

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

[제거-AzureRmVMDataDisk](./Remove-AzureRmVMDataDisk.md)

[Get-AzureRmVM](./Get-AzureRmVM.md)

[새로운 AzureRmVMConfig](./New-AzureRmVMConfig.md)
