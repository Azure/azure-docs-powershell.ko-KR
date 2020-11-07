---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 8F7AF1B8-D769-452C-92CF-4486C3EB894D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmosdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMOSDisk.md
ms.openlocfilehash: 378d0d33d6cc1ceb2eca4773d93f76afbf75cf4b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876866"
---
# Set-AzVMOSDisk

## SYNOPSIS
가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.

## 구문과

### DefaultParamSet (기본값)
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### WindowsDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Windows]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### LinuxParamSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>] [-StorageAccountType <StorageAccountTypes>]
 [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### LinuxDiskEncryptionParameterSet
```
Set-AzVMOSDisk [-VM] <PSVirtualMachine> [[-Name] <String>] [[-VhdUri] <String>]
 [[-Caching] <CachingTypes>] [[-SourceImageUri] <String>] [[-CreateOption] <DiskCreateOptionTypes>] [-Linux]
 [-DiskEncryptionKeyUrl] <String> [-DiskEncryptionKeyVaultId] <String> [[-KeyEncryptionKeyUrl] <String>]
 [[-KeyEncryptionKeyVaultId] <String>] [-DiskSizeInGB <Int32>] [-ManagedDiskId <String>]
 [-StorageAccountType <StorageAccountTypes>] [-WriteAccelerator] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
**AzVMOSDisk** cmdlet은 가상 컴퓨터에서 운영 체제 디스크 속성을 설정 합니다.

## 예제의

### 예제 1: 플랫폼 이미지에서 가상 컴퓨터의 속성 설정
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential) 
PS C:\> $VirtualMachine = Set-AzVMSourceImage -VM $VirtualMachine -PublisherName "Canonical" -Offer "UbuntuServer" -Skus "15.10" -Version "latest" -Caching ReadWrite
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption FromImage
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져온 다음 해당 개체를 $AvailabilitySet 변수에 저장 합니다.
두 번째 명령은 가상 컴퓨터 개체를 만든 다음 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.
마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.

### 예제 2: 일반화 된 사용자 이미지의 가상 컴퓨터에 대 한 속성 설정
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine -Linux -ComputerName "MainComputer" -Credential (Get-Credential)
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "https://mystorageaccount.blob.core.windows.net/vhds/myOSImage.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption fromImage -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.
두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.
마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.

### 예제 3: 특수화 된 사용자 이미지에서 가상 컴퓨터의 속성 설정
```
PS C:\> $AvailabilitySet = Get-AzAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet13" 
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:\> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -VhdUri "https://mystorageaccount.blob.core.windows.net/disks/" -CreateOption Attach -Linux
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName "ResourceGroup11"
```

첫 번째 명령은 ResourceGroup11 이라는 리소스 그룹에서 AvailablitySet13 이라는 가용성 집합을 가져와 해당 개체를 $AvailabilitySet 변수에 저장 합니다.
두 번째 명령은 가상 컴퓨터 개체를 만들어 $VirtualMachine 변수에 저장 합니다.
명령에서 가상 컴퓨터에 이름과 크기를 할당 합니다.
가상 머신이 $AvailabilitySet에 저장 된 가용성 집합에 속합니다.
마지막 명령은 $VirtualMachine의 가상 컴퓨터에 대 한 속성을 설정 합니다.

### 예제 4: 가상 컴퓨터 운영 체제 디스크에서 디스크 암호화 설정 설정
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine17" -VMSize "Standard_A1"
PS C:> $VirtualMachine = Set-AzVMOSDisk -VM $VirtualMachine -Name "OsDisk12" -VhdUri "os.vhd" -Caching ReadWrite -Windows -CreateOption "Attach" -DiskEncryptionKeyUrl "https://mytestvault.vault.azure.net/secrets/Test1/514ceb769c984379a7e0230bddaaaaaa" -DiskEncryptionKeyVaultId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myresourcegroup/providers/Microsoft.KeyVault/vaults/mytestvault"
PS C:> New-AzVM -VM $VirtualMachine -ResouceGroupName " ResourceGroup11"
```

이 예제에서는 가상 컴퓨터 운영 체제 디스크에 대 한 디스크 암호화 설정을 설정 합니다.

## 변수

### -캐싱
운영 체제 디스크의 캐싱 모드를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 읽기
- 쓰기

기본값은 ReadWrite입니다.
캐싱 값을 변경 하면 가상 컴퓨터가 다시 시작 됩니다.

이 설정은 디스크의 성능에 영향을 줍니다.

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CreateOption
이 cmdlet이 플랫폼 또는 사용자 이미지를 사용 하 여 가상 머신에서 디스크를 만들거나 기존 디스크를 연결 하는지 여부를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 붙일.
특수 디스크에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.
이 옵션을 지정 하는 경우 *Sourceimageuri* 매개 변수를 지정 하지 마세요.
대신 Set-AzVMSourceImage cmdlet을 사용 합니다.
또한 *Windows* 또는 *Linux* 매개 변수 사용을 사용 하 여 azure2 플랫폼에 VHD의 운영 체제 유형을 알려 주어 야 합니다.
*VhdUri* 매개 변수는 azure2 platform에 연결할 디스크의 위치를 알려 줄 수 있을 만큼 충분 합니다. 
- FromImage.
플랫폼 이미지 또는 일반화 된 사용자 이미지에서 가상 컴퓨터를 만들려면이 옵션을 지정 합니다.
일반화 된 사용자 이미지의 경우 **AzVMSourceImage** cmdlet을 사용 하는 대신 운영 체제 디스크 VHD의 위치와 유형을 Azure 플랫폼에 알리기 위해 *Sourceimageuri* 매개 변수와 *Windows* 또는 *Linux* 매개 변수를 지정 해야 합니다.
플랫폼 이미지의 경우 *VhdUri* 매개 변수만 있으면 충분 합니다. 
- 비울.

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: 5
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

### -DiskEncryptionKeyUrl
디스크 암호화 키의 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskEncryptionKeyVaultId
디스크 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: True
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DiskSizeInGB
운영 체제 디스크의 크기 (GB)를 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyUrl
키 암호화 키의 위치를 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyEncryptionKeyVaultId
키 암호화 키를 포함 하는 키 보관소의 리소스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: WindowsDiskEncryptionParameterSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Linux
사용자 이미지의 운영 체제를 Linux로 표시 합니다.
사용자 이미지 기반 가상 컴퓨터 배포에 대해이 매개 변수를 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: LinuxParamSet, LinuxDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManagedDiskId
관리 디스크의 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
운영 체제 디스크의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskName, DiskName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceImageUri
사용자 이미지 시나리오에 대 한 VHD의 URI를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceImage

Required: False
Position: 4
Default value: None
Accept pipeline input: False
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
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VhdUri
VHD (가상 하드 디스크)의 URI (Uniform Resource Identifier)를 지정 합니다.

이미지 기반 가상 컴퓨터의 경우이 매개 변수는 플랫폼 이미지 또는 사용자 이미지가 지정 된 경우 만들 VHD 파일을 지정 합니다.
가상 컴퓨터를 시작 하기 위해 이미지 BLOB (이진 대형 개체)를 복사 하는 위치입니다.

디스크 기반 가상 컴퓨터 부팅 시나리오의 경우이 매개 변수는 가상 컴퓨터가 시작에 직접 사용 하는 VHD 파일을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: OSDiskVhdUri, DiskVhdUri

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VM
운영 체제 디스크 속성을 설정할 로컬 가상 컴퓨터 개체를 지정 합니다.
가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Windows
사용자 이미지의 운영 체제가 Windows 임을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: WindowsParamSet, WindowsDiskEncryptionParameterSet
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WriteAccelerator
OS 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.

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

[Get-AzAvailabilitySet](./Get-AzAvailabilitySet.md)

[새로운 AzVMConfig](./New-AzVMConfig.md)


