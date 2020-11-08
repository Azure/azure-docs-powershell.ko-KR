---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2171943B-D1AC-45FD-99FD-DD0C14AFC60C
online version: ''
schema: 2.0.0
ms.openlocfilehash: 38990d3084cf5f494dc811ec6fe458003b8313c9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046355"
---
# Get-AzureDeployment

## SYNOPSIS
배포에 대 한 세부 정보를 가져옵니다.

## 구문과

```
Get-AzureDeployment [-ServiceName] <String> [[-Slot] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**가져오기-azuredeployment** Cmdlet은 Azure 배포의 세부 정보를 가져옵니다.
Azure 서비스의 이름과 배포 슬롯을 지정 합니다.

## 예제의

### 예제 1: 프로덕션 배포에 대 한 세부 정보 가져오기
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService"
```

이 명령은 ContosoService 이라는 서비스에 대 한 배포 세부 정보를 반환 합니다.
이 명령은 슬롯을 지정 하지 않습니다.
따라서이 명령은 기본 프로덕션 값을 사용 합니다.

### 예제 2: 스테이징 배포에 대 한 세부 정보 가져오기
```
PS C:\> Get-AzureDeployment -ServiceName "ContosoService" -Slot "Staging"
```

이 명령은 ContosoService의 스테이징 배포에 대 한 세부 정보를 반환 합니다.

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
서비스의 이름을 지정 합니다.

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
배포 환경을 지정 합니다.
유효한 값은 스테이징 또는 프로덕션입니다.
기본값은 실제 값입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[이동-AzureDeployment](./Move-AzureDeployment.md)

[새 AzureDeployment](./New-AzureDeployment.md)

[-AzureDeployment 제거](./Remove-AzureDeployment.md)

[Set AzureDeployment](./Set-AzureDeployment.md)


