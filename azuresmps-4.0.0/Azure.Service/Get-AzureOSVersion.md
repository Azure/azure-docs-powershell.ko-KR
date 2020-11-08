---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: FAB5E55D-95FC-4545-8BA6-EEFCFDB04200
online version: ''
schema: 2.0.0
ms.openlocfilehash: c311653b92219eb3bee0e3b1f8c8fe5caaee9846
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045637"
---
# Get-AzureOSVersion

## SYNOPSIS
모든 Azure 게스트 운영 체제를 나열 합니다.

## 구문과

```
Get-AzureOSVersion [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureOSVersion** cmdlet에는 사용 가능한 모든 Azure 게스트 운영 체제가 나열 됩니다.

## 예제의

### 예제 1: 사용 가능한 모든 운영 체제 가져오기
```
PS C:\> Get-AzureOSVersion
```

이 명령은 현재 구독에서 사용할 수 있는 모든 버전의 게스트 운영 체제 목록을 포함 하는 개체를 검색 합니다.

### 예제 2: 표에 운영 체제 정보 표시
```
PS C:\> Get-AzureOSVersion | Format-Table -AutoSize -Property "Family", "FamilyLabel", "Version"
```

이 명령은 현재 구독에서 사용할 수 있는 모든 버전의 게스트 운영 체제 목록을 포함 하는 개체를 검색 합니다.
이 명령은 파이프라인 연산자를 사용 하 여이를 **형식 테이블** cmdlet에 전달 합니다.
해당 cmdlet은 운영 체제 제품군, 운영 체제 패밀리 레이블 및 버전이 표시 되는 표로 서식 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-AzureOSDisk](./Get-AzureOSDisk.md)


