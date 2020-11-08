---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046165"
---
# Remove-AzureDeployment

## SYNOPSIS
클라우드 서비스의 배포를 삭제 합니다.

## 구문과

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**-Azuredeployment** Cmdlet은 Azure 클라우드 서비스의 배포를 삭제 합니다.
배포를 삭제 하려면 먼저 일시 중단 합니다.

## 예제의

### 예제 1: 배포 제거
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

이 명령은 ContosoService 이라는 Azure 서비스의 배포를 제거 합니다.
이 명령은 슬롯을 지정 하지 않으므로 프로덕션 환경에서 서비스를 제거 합니다.

### 예제 2: 배포 및 가상 하드 디스크 제거
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

이 명령은 프로덕션 환경에서 ContosoService 이라는 서비스의 배포를 제거 합니다.
또한이 명령은 기본 가상 하드 디스크를 제거 합니다.

## 변수

### -DeleteVHD
이 cmdlet이 blob 저장소에서 배포 및 Vhd (가상 하드 디스크)를 제거 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
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
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
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

### -ServiceName
이 cmdlet이 배포를 삭제 하는 서비스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -슬롯
이 cmdlet이 배포를 삭제 하는 배포 환경을 지정 합니다.
유효한 값은 스테이징 및 프로덕션입니다.
기본값은 실제 값입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ManagementOperationContext

## 상속자

## 관련 링크

[다운로드-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[이동-AzureDeployment](./Move-AzureDeployment.md)

[새 AzureDeployment](./New-AzureDeployment.md)

[Set AzureDeployment](./Set-AzureDeployment.md)


