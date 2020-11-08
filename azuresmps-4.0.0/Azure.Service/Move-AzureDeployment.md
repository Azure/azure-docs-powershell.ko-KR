---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046244"
---
# Move-AzureDeployment

## SYNOPSIS
프로덕션 및 스테이징 간에 배포를 교환 합니다.

## 구문과

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**AzureDeployment Move** cmdlet은 프로덕션 및 스테이징 환경에서 배포의 가상 IP 주소를 바꿉니다.
이 cmdlet은 스테이징 환경에서 현재 실행 되는 배포를 프로덕션 환경에 교환 하 고 프로덕션 환경에서 스테이징 환경으로 실행 하는 배포를 바꿉니다.
스테이징 환경에 배포가 있고 프로덕션 환경에 배포 되지 않은 경우 cmdlet은 배포를 프로덕션으로 이동 합니다.
프로덕션 환경에 배포가 있고 스테이징 환경에 배포 되지 않은 경우에는 cmdlet이 실패 합니다.

## 예제의

### 예제 1: 서비스의 배포 교환
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

이 명령은 프로덕션 환경과 스테이징 환경 간에 ContosoService 이라는 서비스의 배포를 바꿉니다.

## 변수

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
이 cmdlet이 프로덕션 및 스테이징 배포를 바꾸는 서비스의 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### ManagementOperationContext

## 상속자

## 관련 링크

[다운로드-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[새 AzureDeployment](./New-AzureDeployment.md)

[-AzureDeployment 제거](./Remove-AzureDeployment.md)

[Set AzureDeployment](./Set-AzureDeployment.md)


