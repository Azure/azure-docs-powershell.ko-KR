---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2D09422F-82B1-4243-B835-8BF223A6F936
online version: ''
schema: 2.0.0
ms.openlocfilehash: a6f02f333601172341de4fe8a0bf629037f712a5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045975"
---
# New-AzureSiteRecoveryStorageMapping

## SYNOPSIS
Azure 저장소 개체와 복구 저장소 개체 간의 매핑을 만듭니다.

## 구문과

```
New-AzureSiteRecoveryStorageMapping -PrimaryStorage <ASRStorage> -RecoveryStorage <ASRStorage>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSiteRecoveryStorageMapping** Cmdlet은 Azure Site Recovery 관리 기본 Azure 저장소 개체와 복구 저장소 개체 간의 매핑을 만듭니다.

## 예제의

### 예제 1: 저장소 개체와 복구 저장소 개체 간의 매핑 만들기
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $Storages = Get-AzureSiteRecoveryStorage -Server $Servers[0]
PS C:\> New-AzureSiteRecoveryStorageMapping -PrimaryStorage $Storages[0] -RecoveryStorage $Storages[1]
```

첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.
명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.

두 번째 명령은 $Servers 배열의 첫 번째 서버에 대 한 사이트 복구 저장소를 가져온 다음 $Storages에 저장 합니다.

마지막 명령은 기본 네트워크와 복구 네트워크 간에 매핑을 만듭니다.
이 명령은 $Storages의 첫 번째 요소로 기본 저장소 개체를 지정 합니다.
명령은 $Storages의 두 번째 요소로 복구 저장소 개체를 지정 합니다.

## 변수

### -PrimaryStorage
복구 저장소에 매핑할 기본 저장소를 지정 합니다.
**Asrstorage** 개체를 얻으려면 Get-AzureSiteRecoveryStorage cmdlet을 사용 합니다.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -RecoveryStorage
복구 저장소 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 저장소 개체에 기본 저장소 개체를 매핑합니다.
**Asrstorage** 개체를 얻으려면 **get-help를 AzureSiteRecoveryStorage** 를 사용 합니다.

```yaml
Type: ASRStorage
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureSiteRecoveryStorage](./Get-AzureSiteRecoveryStorage.md)

[Get-AzureSiteRecoveryStorageMapping](./Get-AzureSiteRecoveryStorageMapping.md)

[제거-AzureSiteRecoveryStorageMapping](./Remove-AzureSiteRecoveryStorageMapping.md)


