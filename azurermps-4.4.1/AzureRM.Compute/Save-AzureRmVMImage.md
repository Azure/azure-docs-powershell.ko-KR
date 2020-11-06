---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2B5BC27-6D51-45BC-AE6A-F7FED11B8651
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Save-AzureRmVMImage.md
ms.openlocfilehash: cadcaccc2bb93dee5298ca92561c5bef36b5d9ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537379"
---
# Save-AzureRmVMImage

## SYNOPSIS
가상 컴퓨터를 VMImage로 저장 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### ResourceGroupNameParameterSetName (기본값)
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### IdParameterSetName
```
Save-AzureRmVMImage [-Name] <String> [-DestinationContainerName] <String> [-VHDNamePrefix] <String>
 [-Overwrite] [[-Path] <String>] [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmVMImage** cmdlet은 가상 컴퓨터를 VMImage로 저장 합니다.
가상 컴퓨터 이미지를 만들기 전에 가상 컴퓨터를 sysprep 하 고 Set-AzureRmVM cmdlet을 사용 하 여 일반화 된 것으로 표시 합니다.

이 cmdlet의 출력은 JSON (JavaScript 개체 표기법) 템플릿입니다.
캡처한 이미지에서 가상 컴퓨터를 배포할 수 있습니다.

## 예제의

### 예제 1: 가상 컴퓨터 캡처
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized 
PS C:\> Save-AzureRmVMImage -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -DestinationContainerName "VMContainer01" -VHDNamePrefix "VM07"
```

첫 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 일반화 된 것으로 표시 합니다.

두 번째 명령은 VirtualMachine07 이라는 가상 컴퓨터를 VMImage로 캡처합니다.
**Output** 속성은 JSON 템플릿을 반환 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationContainerName
"시스템" 컨테이너 내에서 이미지를 포함 하려는 컨테이너의 이름을 지정 합니다.

컨테이너가 없는 경우 생성 됩니다.
VMImage를 구성 하는 Vhd (가상 하드 디스크)는이 매개 변수에서 지정 하는 컨테이너에 위치 합니다.
Vhd가 여러 저장소 계정에 걸쳐 분산 되어 있는 경우이 cmdlet은 각 저장소 계정에이 이름을 가진 하나의 컨테이너를 만듭니다.
저장 된 이미지의 URL은 다음과 유사 합니다. 

https://. \<storageAccountName\> blob.core.windows.net/system/Microsoft.Compute/Images/ \<imagesContainer\> . / \<vhdPrefix-osDisk\>

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
가상 컴퓨터의 리소스 ID를 지정 합니다.

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

### -이름
이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Overwrite
이 cmdlet이 대상 컨테이너에서 동일한 접두사를 가진 Vhd를 덮어쓰도록 지정 합니다.

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
VHD의 경로를 지정 합니다.

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
가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.

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
VMImage의 저장소 프로필을 구성 하는 blob 이름에 접두사를 지정 합니다.

예를 들어 운영 체제 디스크에 대 한 접두사 vhdPrefix는 vhdPrefix-osdisk .와 같은 이름으로 \<guid\> 반환 됩니다. .vhd.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureRmVMImage](./Get-AzureRmVMImage.md)

[Get-AzureRmVMImageOffer](./Get-AzureRmVMImageOffer.md)

[Get-AzureRmVMImagePublisher](./Get-AzureRmVMImagePublisher.md)

[Get-AzureRmVMImageSku](./Get-AzureRmVMImageSku.md)

[Set-AzureRmVM](./Set-AzureRmVM.md)


