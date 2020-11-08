---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: BB36A434-6BE3-46BF-B10A-FCD6C766CB84
online version: ''
schema: 2.0.0
ms.openlocfilehash: 87414a56778123053615bb36a06113e2b0b0633f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046110"
---
# Remove-AzureSiteRecoveryNetworkMapping

## SYNOPSIS
사이트 복구 자격 증명 모음에서 네트워크 매핑을 제거 합니다.

## 구문과

```
Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSiteRecoveryNetworkMapping** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에서 네트워크 매핑을 제거 합니다.

## 예제의

### 예제 1: 네트워크와 복구 네트워크 간의 매핑 제거
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -RecoveryServer $Servers[0]
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

첫 번째 명령 cmdlet은 **AzureSiteRecoveryServer** cmdlet을 사용 하 여 현재 Azure Site Recovery 자격 증명 모음에 대 한 서버를 가져옵니다.
명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.

두 번째 명령은 기본 네트워크와 복구 네트워크 간의 매핑을 가져온 다음 $NetworkMapping 변수에 저장 합니다.
명령이 네트워크 매핑의 기본 서버를 $Servers의 첫 번째 요소로 지정 합니다.
명령은 복구 네트워크에 대 한 서버를 $Servers의 두 번째 요소로 지정 합니다.

마지막 명령은 $NetworkMapping에서 네트워크 매핑을 제거 합니다.

### 예제 2: 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑 제거
```
PS C:\> $Servers = Get-AzureSiteRecoveryServer
PS C:\> $NetworkMapping = Get-AzureSiteRecoveryNetworkMapping -PrimaryServer $Servers[0] -Azure
PS C:\> Remove-AzureSiteRecoveryNetworkMapping -NetworkMapping $NetworkMapping
```

첫 번째 명령 cmdlet은 현재 사이트 복구 자격 증명 모음에 대 한 서버를 가져옵니다.
명령은 사이트 복구 서버를 $Servers 배열 변수에 저장 합니다.

두 번째 명령은 기본 네트워크와 Azure 가상 컴퓨터 네트워크 간의 매핑을 가져온 다음 $NetworkMapping 변수에 저장 합니다.
명령은 $Servers의 첫 번째 요소로 네트워크의 기본 서버를 지정 합니다.
명령은 *Azure* 매개 변수를 지정 합니다.
따라서 명령은 Azure virtual machine 네트워크에 대 한 매핑을 가져옵니다.

마지막 명령은 $NetworkMapping에서 네트워크 매핑을 제거 합니다.

## 변수

### -NetworkMapping
제거할 네트워크 매핑을 지정 합니다.

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureSiteRecoveryNetworkMapping](./Get-AzureSiteRecoveryNetworkMapping.md)

[새로운 AzureSiteRecoveryNetworkMapping](./New-AzureSiteRecoveryNetworkMapping.md)

[Get-AzureSiteRecoveryServer](./Get-AzureSiteRecoveryServer.md)


