---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 7EF20FC0-3E2A-4AFC-AC02-9B11C8952DB8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22263501f2a79a36c1ace1915ee6898c4833b52b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045563"
---
# Get-AzureStorSimpleDeviceVolumeContainer

## SYNOPSIS
장치에서 볼륨 컨테이너를 가져옵니다.

## 구문과

```
Get-AzureStorSimpleDeviceVolumeContainer -DeviceName <String> [-VolumeContainerName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureStorSimpleDeviceVolumeContainer** cmdlet은 장치 또는 볼륨 컨테이너에서 지정 된 이름의 볼륨 컨테이너 목록을 가져옵니다.
반환 된 개체에는 다음 속성이 포함 됩니다. 

- **BandwidthRate**
- **Encryption.encryptionkey**
- **InstanceId**
- **IsDefault**
- **Isa 사용**
- **성을**
- **OperationInProgress**
- **소유**
- **PrimaryStorageAccountCredential**
- **SecretsEncryptionThumbprint**
- **(가) Ecount**

## 예제의

### 예제 1: 장치에서 모든 컨테이너 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "8600-Bravo 001"
InstanceId                           Name                                             IsEncryptionEnabled  Owned BandwidthRate                                    PrimaryStorageAccountCredential                 VolumeCount                                    
----------                           ----                                             -------------------  ----- -------------                                    -------------------------------                 -----------                                    
127135b6-92de-4f53-850d-70e1f9a38cbe Test_Container                                   False                True  0                                                Test_Account                                    6
```

이 명령은 8600-Bravo 001 이라는 장치에서 볼륨 컨테이너의 목록을 가져옵니다.

### 예제 2: 이름을 사용 하 여 컨테이너 가져오기
```
PS C:\>Get-AzureStorSimpleDeviceVolumeContainer -DeviceName "Contoso63-AppVm" -VolumeContainerName "Container08"
VERBOSE: ClientRequestId: 8027c66a-869b-4ea3-97a2-e17d98ec751c_PS
VERBOSE: ClientRequestId: 344f9be5-0887-4d37-98ef-e45c557774f1_PS
VERBOSE: ClientRequestId: 14919be5-d6f5-4f81-b7f1-d7fafff2238c_PS


BandwidthRate                   : 256
EncryptionKey                   : 
InstanceId                      : 04ea9aad-7a56-4a50-b195-86061b0a810a
IsDefault                       : False
IsEncryptionEnabled             : False
Name                            : Container03
OperationInProgress             : None
Owned                           : True
PrimaryStorageAccountCredential : Microsoft.WindowsAzure.Management.StorSimple.Models.StorageAccountCredentialResponse
SecretsEncryptionThumbprint     : 
VolumeCount                     : 5

VERBOSE: Volume container with name: Container03 is found.
```

이 명령은 Contoso63-AppVm 이라는 장치에서 Container08 이라는 볼륨 컨테이너를 가져옵니다.

## 변수

### -장치 이름
StorSimple 장치의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 장치에서 볼륨 컨테이너를 가져옵니다.

```yaml
Type: String
Parameter Sets: (All)
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

### -VolumeContainerName
가져올 볼륨 컨테이너의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### DataContainer, IList\<DataContainer\>
*VolumeContainerName* 매개 변수를 지정 하는 경우이 Cmdlet은 **DataContainer** 개체를 반환 합니다.
해당 매개 변수를 지정 하지 않으면이 cmdlet은 **IList \<DataContainer\>** 개체를 반환 합니다.

## 상속자

## 관련 링크

[새로운 AzureStorSimpleDeviceVolumeContainer](./New-AzureStorSimpleDeviceVolumeContainer.md)

[제거-AzureStorSimpleDeviceVolumeContainer](./Remove-AzureStorSimpleDeviceVolumeContainer.md)


