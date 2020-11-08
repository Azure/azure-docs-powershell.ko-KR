---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 0A1FD05F-6573-46D8-8217-C7EA432F6742
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd8ccb634c313f487b6777a9fcb66d872b35510e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046109"
---
# Remove-AzureSiteRecoveryStorageMapping

## SYNOPSIS
사이트 복구 자격 증명 모음에 대 한 저장소 개체 매핑을 제거 합니다.

## 구문과

```
Remove-AzureSiteRecoveryStorageMapping -StorageMapping <ASRStorageMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSiteRecoveryStorageMapping** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대 한 저장소 개체 매핑을 제거 합니다.

## 예제의

### 예제 1: 네트워크와 복구 네트워크 간의 매핑 제거
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $StorageMapping = Get-AzureSiteRecoveryStorageMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[1]
PS C:\> Remove-AzureSiteRecoveryStorageMapping -StorageMapping $StorageMapping
Get-AzureSiteRecoveryServerGet-AzureSiteRecoveryStorageMappingNew-AzureSiteRecoveryStorageMapping
```

첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.
명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.

두 번째 명령은 두 저장소 개체 간의 매핑을 가져온 다음 $StorageMapping 변수에 저장 합니다.
명령이 네트워크 매핑의 기본 서버를 $Servers의 첫 번째 요소로 지정 합니다.
명령은 복구 네트워크에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.

마지막 명령은 $StorageMapping에서 매핑을 제거 합니다.

## 변수

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -StorageMapping
네트워크 매핑을 지정 합니다.
**ASRStorageMapping** 을 얻으려면 **AzureSiteRecoveryStorage** cmdlet을 사용 하세요.

```yaml
Type: ASRStorageMapping
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

## 출력

## 상속자

## 관련 링크

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)


