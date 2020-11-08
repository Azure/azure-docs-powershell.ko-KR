---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2AEA385F-E180-4564-A62A-9E913C665801
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1fff3ea97c51ee5597e585f3275b25e513c22008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045480"
---
# Reset-AzureRoleInstance

## SYNOPSIS
특정 역할의 단일 역할 인스턴스 또는 모든 역할 인스턴스의 재부팅 또는 다시 부팅을 요청 합니다.

## 구문과

```
Reset-AzureRoleInstance [-ServiceName] <String> -Slot <String> -InstanceName <String> [-Reboot] [-Reimage]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**AzureRoleInstance** cmdlet은 배포에서 실행 되는 역할 인스턴스의 다시 부팅을 요청 합니다.
이 작업은 동기적으로 실행 됩니다.
역할 인스턴스를 다시 부팅 하면 Azure에서 해당 인스턴스를 오프 라인 상태로 전환 하 고 해당 인스턴스에 대 한 기본 운영 체제를 다시 시작 하 고 인스턴스를 다시 온라인 상태로 만듭니다.
로컬 디스크에 기록 된 모든 데이터는 다시 부팅 하는 동안 유지 됩니다.
메모리 내에 있는 모든 데이터는 손실 됩니다.

역할 인스턴스가 Reimaging 역할 유형에 따라 다른 동작이 발생 합니다.
웹 또는 작업자 역할의 경우 역할이 reimaged 경우 Azure가 오프 라인으로 전환 하 고 Azure 게스트 운영 체제의 새 설치를 가상 컴퓨터에 기록 합니다.
그러면 역할이 다시 온라인 상태가 됩니다.
VM 역할의 경우 역할을 reimaged 하는 경우 Azure가 오프 라인으로 전환 하 고, 제공 된 사용자 지정 이미지를 다시 적용 하 고, 역할을 온라인 상태로 만듭니다.

Azure는 역할이 reimaged 때 로컬 저장소 리소스에 데이터를 유지 관리 하려고 시도 합니다. 그러나 일시적인 하드웨어 장애가 발생 하는 경우 로컬 저장소 리소스가 손실 될 수 있습니다.
응용 프로그램에서 Azure 드라이브와 같은 영속적 데이터 원본에 기록 하는 데이터를 유지 해야 하는 경우 사용 하는 것이 좋습니다.
로컬 저장소 리소스에 정의 된 것과는 다른 로컬 디렉터리에 기록 된 데이터는 역할이 reimaged 경우 손실 됩니다.

## 예제의

### 예제 1: 역할 인스턴스 다시 부팅
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -InstanceName "MyWebRole_IN_0" -Reboot
```

이 명령은 MySvc01 서비스의 스테이징 배포에서 MyWebRole_IN_0 이라는 역할 인스턴스를 다시 부팅 합니다.

### 예제 2: 역할 인스턴스를 이미지로 만듭니다.
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc01" -Slot "Staging" -Reimage
```

이 명령은 MySvc01 클라우드 서비스의 스테이징 배포에서 역할 인스턴스를 다시 이미지 합니다.

### 예제 3: 모든 역할 인스턴스 이미지로
```
PS C:\> ReSet-AzureRoleInstance -ServiceName "MySvc1" -Slot "Production" -Reimage
```

이 명령은 MySvc01 서비스의 프로덕션 배포에 있는 모든 역할 인스턴스를 다시 이미지 합니다.

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

### -InstanceName
다시 부팅 하거나 재부팅할 역할 인스턴스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -다시 부팅
이 cmdlet이 지정 된 역할 인스턴스를 재부팅 하도록 지정 하거나 지정 하지 않은 경우 모든 역할 인스턴스를 지정 합니다.
*Reboot* 또는 *이미지로* 매개 변수 중 하나만 포함 해야 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이미지로
이 cmdlet이 지정 된 역할 인스턴스를 다시 이미지 하도록 지정 하거나 지정 하지 않은 경우 모든 역할 인스턴스를 배치 합니다.
*Reboot* 또는 *이미지로* 매개 변수 중 하나만 포함 해야 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
역할 인스턴스가 실행 되는 배포 환경을 지정 합니다.
유효한 값은 프로덕션 및 준비입니다.
*Deploymentname* 또는 *Slot* 매개 변수 중 하나만 포함할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Set-AzureRole](./Set-AzureRole.md)


