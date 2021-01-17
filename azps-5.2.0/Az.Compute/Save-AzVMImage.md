---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/save-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Save-AzVMImage.md
ms.openlocfilehash: 0d2a4ade662ec23a4a139460bce8fe5387683120
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370049"
---
# Save-AzVMImage

## SYNOPSIS
가상 머신을 VMImage로 저장합니다.

## 구문

### ResourceGroupNameParameterSetName(기본값)
```
Save-AzVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite]
 [[-Path] <String>] [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzVMImage [-DestinationContainerName] <String> [-VHDNamePrefix] <String> [-Overwrite] [[-Path] <String>]
 [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**Save-AzVMImage** cmdlet은 가상 머신을 VMImage로 저장합니다.
가상 머신 이미지를 만들기 전에 가상 머신을 sysprep한 다음, Set-AzVM cmdlet을 사용하여 일반화된 것으로 표시합니다.
이 cmdlet의 출력은 JSON(JavaScript Object Notation) 템플릿입니다.
캡처한 이미지에서 가상 머신을 배포할 수 있습니다.

## 예제

### 예제 1: 가상 머신 캡처
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

첫 번째 명령은 VirtualMachine07이라는 가상 머신을 일반화된 것으로 표시합니다.
두 번째 명령은 VirtualMachine07이라는 가상 머신을 VMImage로 캡처합니다.
Output **속성은** JSON 템플릿을 반환합니다.

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.

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

### -DestinationContainerName
이미지를 보유하려는 "시스템" 컨테이너 내부에 있는 컨테이너의 이름을 지정합니다.
컨테이너가 없는 경우 컨테이너가 만들어집니다.
VMImage를 구성하는 VHD(가상 하드 디스크)는 이 매개 변수가 지정하는 컨테이너에 상주합니다.
VHD가 여러 저장소 계정에 분산된 경우 이 cmdlet은 각 저장소 계정에 이 이름이 있는 하나의 컨테이너를 만듭니다.
저장된 이미지의 URL은 \<storageAccountName\> .https:// \<imagesContainer\> / \<vhdPrefix-osDisk\> .blob.core.windows.net/system/Microsoft.Compute/Images/ .xx-x.vhd와 유사합니다.

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

### -Id
가상 머신의 리소스 ID를 지정합니다.

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
이 cmdlet이 대상 컨테이너에서 동일한 연결선이 있는 모든 VHD를 덮어 입력합니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
캡처된 이미지의 템플릿이 저장되는 파일 경로입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
가상 머신의 리소스 그룹의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VHDNamePrefix
VMImage의 저장소 프로필을 구성하는 Blob의 이름에 대한 prefix를 지정합니다.
예를 들어 운영 체제 디스크에 대한 vhdPrefix의 경우 이름 vhdPrefix-osdisk가 \<guid\> 됩니다. vhd.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VirtualHardDiskNamePrefix

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation

## 참고 사항

## 관련 링크

[Get-AzVMImage](./Get-AzVMImage.md)

[Get-AzVMImageOffer](./Get-AzVMImageOffer.md)

[Get-AzVMImagePublisher](./Get-AzVMImagePublisher.md)

[Get-AzVMImageSku](./Get-AzVMImageSku.md)

[Set-AzVM](./Set-AzVM.md)


