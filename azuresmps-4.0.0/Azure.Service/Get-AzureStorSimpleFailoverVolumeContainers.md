---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: BABBA19E-5833-452C-9E36-811EAE7C20F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb326281058f0ff9280c4b87c0530241ece801e0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045561"
---
# Get-AzureStorSimpleFailoverVolumeContainers

## SYNOPSIS
장치 장애 조치에 대 한 볼륨 컨테이너 그룹을 가져옵니다.

## 구문과

### IdentifyById
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Get-AzureStorSimpleFailoverVolumeContainers -DeviceName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureStorSimpleFailoverVolumeContainers** cmdlet은 장치 장애 조치에 대 한 볼륨 컨테이너 그룹을 가져옵니다.
**시작-AzureStorSimpleDeviceFailover** cmdlet에 단일 **VolumeContainer** 그룹 또는 **VolumeContainer** 그룹의 배열을 전달 합니다.
**IsDCGroupEligibleForDR** 속성에 대 한 $True 값이 있는 그룹만 장애 조치에 적격 할 수 있습니다.

## 예제의

### 예제 1: 장애 조치 볼륨 컨테이너 가져오기
```
PS C:\>Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7"

DCGroup                    IneligibilityMessage          IsDCGroupEligibleForDR
-------                    --------------------          ----------------------
{VolumeContainer1889078...                                                 True
{VC_01}                    No cloud snapshot found                        False
{VolumeContainer7306959}   No cloud snapshot found                        False
{VolumeContainer407850151} No cloud snapshot found                        False
```

이 명령은 장애 조치 볼륨 컨테이너를 가져옵니다.
**IsDCGroupEligibleForDR** 속성에 대 한 $True 값이 있는 dcgroups만 장치 장애 조치에 사용할 수 있습니다.

## 변수

### -DeviceId
Cmdlet을 실행할 StorSimple 장치의 인스턴스 ID를 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -장치 이름
Cmdlet을 실행할 StorSimple 장치의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
Azure 프로필을 지정 합니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### IList\<DataContainerGroup\>
이 cmdlet은 **VolumeContainer** 그룹의 목록을 반환 합니다.

## 상속자

## 관련 링크

[시작-AzureStorSimpleDeviceFailoverJob](./Start-AzureStorSimpleDeviceFailoverJob.md)

[Get-AzureStorSimpleDeviceVolumeContainer](./Get-AzureStorSimpleDeviceVolumeContainer.md)


