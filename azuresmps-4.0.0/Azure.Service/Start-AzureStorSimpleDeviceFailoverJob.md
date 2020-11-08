---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 53580FF1-D905-40FD-A5F0-D5FBCD036E0B
online version: ''
schema: 2.0.0
ms.openlocfilehash: a51fd8210d2fe7fb224ed43650a354e383ed4e54
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045776"
---
# Start-AzureStorSimpleDeviceFailoverJob

## SYNOPSIS
볼륨 컨테이너 그룹의 장애 조치 (failover) 작업을 시작 합니다.

## 구문과

### 비어 있음 (기본값)
```
Start-AzureStorSimpleDeviceFailoverJob
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceId <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceId <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByName
```
Start-AzureStorSimpleDeviceFailoverJob -DeviceName <String>
 -VolumecontainerGroups <System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]>
 -TargetDeviceName <String> [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleDeviceFailoverJob** cmdlet은 한 장치에서 다른 장치로 하나 이상의 볼륨 컨테이너 그룹의 장애 조치 (failover) 작업을 시작 합니다.

## 예제의

### 예제 1: 명명 된 장치 및 명명 된 대상 장치에 대 한 장애 조치 작업 시작
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceName "ChewD_App7") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Start-AzureStorSimpleDeviceFailoverJob -DeviceName "ChewD_App7" -TargetDeviceName "Fuller05" -Force
a3d902be-8ffb-42a4-bbf8-0a1b30db71b2_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

이 명령은 **AzureStorSimpleFailoverVolumeContainers** cmdlet을 사용 하 여 ChewD_App7 라는 장치에 대 한 장애 조치 볼륨 컨테이너를 가져옵니다.
명령이 **IsDCGroupEligibleForDR** 속성에 대 한 $True 이외의 값을 갖는 컨테이너가 **있는 Where 개체** cmdlet에 결과를 전달 합니다.
자세한 내용은을 입력 `Get-Help Where-Object` 하세요.
현재 cmdlet은 나머지 장애 조치 볼륨 컨테이너에 대 한 장애 조치 작업을 시작 합니다.
명령은 장치 이름 및 대상 디바이스 이름을 지정 합니다.
명령은 cmdlet이 시작 되는 작업의 인스턴스 ID를 반환 합니다.

### 예제 2: 장치 및 ID로 지정 된 대상 장치에 대 한 장애 조치 작업 시작
```
PS C:\>(Get-AzureStorSimpleFailoverVolumeContainers -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925") | Where-Object {$_.IsDCGroupEligibleForDR -eq $True} | Select-Object -First 1 | Start-AzureStorSimpleDeviceFailoverJob -DeviceId "3825f272-1efb-4c14-b63f-22605ce3b925" -TargetDeviceId "0ee59ae9-0293-46e2-ae56-bc308c8e5520" -Force
4c5ac0d0-4b66-465c-98f5-aec90505ad12_0ee59ae9-0293-46e2-ae56-bc308c8e5520
```

이 명령은 **AzureStorSimpleFailoverVolumeContainers** 를 사용 하 여 ChewD_App7 라는 장치에 대 한 장애 조치 볼륨 컨테이너를 가져옵니다.
명령이 **IsDCGroupEligibleForDR** 속성에 대 한 $True 이외의 값이 있는 containters를 삭제 하는 해당 결과를 **Where 개체** 에 전달 합니다.
Cmdlet은 해당 결과를 **개체 선택** cmdlet에 전달 하 여 현재 cmdlet에 전달할 첫 번째 개체를 선택 합니다.
자세한 내용은을 입력 `Get-Help Select-Object` 하세요.
현재 cmdlet은 선택한 장애 조치 볼륨 컨테이너에 대 한 장애 조치 작업을 시작 합니다.
명령은 장치 ID와 대상 디바이스 ID를 지정 합니다.
명령은 cmdlet이 시작 되는 작업의 인스턴스 ID를 반환 합니다.

## 변수

### -DeviceId
볼륨 컨테이너 그룹이 있는 StorSimple 장치의 인스턴스 ID를 지정 합니다.

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
볼륨 컨테이너 그룹이 있는 StorSimple 장치의 이름을 지정 합니다.

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

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -TargetDeviceId
이 cmdlet이 볼륨 컨테이너 그룹에 대해 장애 조치 하는 StorSimple 장치의 인스턴스 ID를 지정 합니다.

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

### -TargetDeviceName 이름
이 cmdlet이 볼륨 컨테이너 그룹에 대해 장애 조치 하는 StorSimple 장치의 이름을 지정 합니다.

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

### -VolumecontainerGroups
이 cmdlet이 다른 디바이스에 대해 장애 조치 하는 볼륨 컨테이너 그룹의 목록을 지정 합니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.WindowsAzure.Management.StorSimple.Models.DataContainerGroup]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 목록\<DataContainerGroup\>
이 cmdlet에 볼륨 컨테이너 그룹의 목록을 파이프 할 수 있습니다.

## 출력

### 이름

## 상속자

## 관련 링크

[Get-AzureStorSimpleFailoverVolumeContainers](./Get-AzureStorSimpleFailoverVolumeContainers.md)


