---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssvmdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssVMDataDisk.md
ms.openlocfilehash: 5e7901f3e2d18b0707ccf9c5f62f9ab55789a45e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195092"
---
# Add-AzVmssVMDataDisk

## SYNOPSIS
Vmss VM에 데이터 디스크를 추가합니다.

## 구문

```
Add-AzVmssVMDataDisk [-VirtualMachineScaleSetVM] <PSVirtualMachineScaleSetVM> [-Lun] <Int32>
 [-CreateOption] <String> [-ManagedDiskId] <String> [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-Caching <CachingTypes>] [-DiskSizeInGB <Int32>] [-WriteAccelerator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Add-AzVmssVMDataDisk** cmdlet은 Vmss VM에 데이터 디스크를 추가합니다.

## 예제

### 예제 1: Vmss VM에 관리되는 데이터 디스크를 추가합니다.
```powershell
PS C:\> $disk = Get-AzDisk -ResourceGroupName $rgname -DiskName $diskname0
PS C:\> $VmssVM = Get-AzVmssVM -ResourceGroupName "myrg" -VMScaleSetName "myvmss" -InstanceId 0
PS C:\> $VmssVM = Add-AzVmssVMDataDisk -VirtualMachineScaleSetVM $VmssVM -Lun 0 -DiskSizeInGB 10 -CreateOption Attach -StorageAccountType Standard_LRS -ManagedDiskId $disk.Id
PS C:\> Update-AzVmssVM -VirtualMachineScaleSetVM $VmssVM
```

첫 번째 명령은 기존 관리 디스크를 얻습니다.
다음 명령은 리소스 그룹 이름, vmss 이름 및 인스턴스 ID로 제공된 기존 Vmss VM을 얻습니다.
다음 명령은 관리 디스크를 VM에 로컬로 저장된 VM에 $VmssVM.
마지막 명령은 추가된 데이터 디스크로 Vmss VM을 업데이트합니다.

## PARAMETERS

### -캐싱
디스크의 캐싱 모드를 지정합니다.
이 매개 변수에 허용되는 값은
- ReadOnly
- ReadWrite
- None 기본값은 ReadWrite입니다.
이 값을 변경하면 가상 머신이 다시 시작됩니다.
이 설정은 디스크의 일관성 및 성능에 영향을 미치고 있습니다.

```yaml
Type: Microsoft.Azure.Management.Compute.Models.CachingTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CreateOption
이 cmdlet이 플랫폼 또는 사용자 이미지에서 가상 머신에 디스크를 만드는지, 빈 디스크를 만드는지 또는 기존 디스크를 연결할지 여부를 지정합니다.
이 매개 변수에 허용되는 값은
- 연결합니다.
특수한 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.
이 옵션을 지정할 때 *SourceImageUri* 매개 변수를 지정하지 않습니다.
*VhdUri는* Azure 플랫폼에 VHD(가상 하드 디스크)의 위치를 가상 머신에 데이터 디스크로 연결하기 위해 필요한 모든 것입니다.
- 비어 있습니다.
빈 데이터 디스크를 만들 수 있습니다.
- FromImage.
일반화된 이미지 또는 디스크에서 가상 머신을 만들 때 이 옵션을 지정합니다.
이 옵션을 지정할 때 Azure 플랫폼에 데이터 디스크로 연결할 VHD의 위치를 알려 주기 위해 *SourceImageUri* 매개 변수를 지정해야 합니다.
*VhdUri* 매개 변수는 가상 머신에서 사용할 때 데이터 디스크 VHD가 저장될 위치를 식별하는 위치로 사용됩니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionSetId
고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.  관리 디스크에만 지정할 수 있습니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
가상 머신에 연결할 빈 디스크의 크기를 기가바이트로 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Lun
데이터 디스크에 대한 LUN(논리 단위 번호)을 지정합니다.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagedDiskId
관리 디스크의 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountType
관리 디스크의 저장소 계정 유형을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VirtualMachineScaleSetVM
데이터 디스크를 추가할 로컬 가상 머신 확장 집합 VM 개체를 지정합니다.
**Get-AzVmssVM** cmdlet을 사용하여 가상 머신 확장 집합 VM 개체를 얻을 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WriteAccelerator
관리되는 데이터 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

### System.Int32

### System.String

### Microsoft.Azure.Management.Compute.Models.CachingTypes

## 출력

### Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSetVM

## 참고 사항

## 관련 링크
