---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C50472E-CE36-4BF1-92C9-A3B9B183ACD1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 929b439c58c344a1902c497bbad6e056e3755025
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046314"
---
# Get-AzureRole

## SYNOPSIS
Microsoft Azure 서비스의 역할 목록을 반환 합니다.

## 구문과

```
Get-AzureRole [-ServiceName] <String> [[-Slot] <String>] [[-RoleName] <String>] [-InstanceDetails]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## 설명은
**AzureRole** Cmdlet은 Microsoft Azure 서비스의 역할에 대 한 세부 정보를 포함 하는 list 개체를 반환 합니다.
*RoleName* 매개 변수를 지정 하는 경우 **Get-AzureRole** 는 해당 역할에 대 한 정보만 반환 합니다.
*Instancedetails* 매개 변수를 지정 하면 추가, 인스턴스 관련 세부 정보가 반환 됩니다.

## 예제의

### 예제 1: 서비스에 대 한 역할 목록 가져오기
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production"
```

이 명령은 MySvc01 서비스에서 실행 되는 모든 프로덕션 역할에 대 한 세부 정보가 포함 된 개체를 반환 합니다.

### 예제 2: 서비스에서 실행 되는 역할에 대 한 세부 정보 가져오기
```
PS C:\> Get-AzureRole -ServiceName "MySvc1" -Slot "Staging" -RoleName "MyTestVM3"
```

이 명령은 MyTestVM3 역할에 대 한 세부 정보가 포함 된 개체를 반환 하며, MySvc01 서비스의 스테이징 환경에서 실행 됩니다.

### 예제 3: 서비스에서 실행 되는 역할의 인스턴스에 대 한 인스턴스 정보 가져오기
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -RoleName "MyTestVM02" -InstanceDetails
```

이 명령은 MySvc01 서비스의 프로덕션 환경에서 실행 되는 MyTestVM02 역할의 인스턴스에 대 한 세부 정보가 포함 된 개체를 반환 합니다.

### 예제 4: 서비스와 연결 된 역할 인스턴스의 테이블 가져오기
```
PS C:\> Get-AzureRole -ServiceName "MySvc01" -Slot "Production" -InstanceDetails | Format-Table -Auto "InstanceName", "InstanceSize", "InstanceStatus"
```

이 명령은 MySvc01 서비스의 프로덕션 환경에서 실행 되는 모든 역할 인스턴스의 인스턴스 이름, 크기, 상태 테이블을 반환 합니다.

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

### -InstanceDetails
이 cmdlet이 각 역할의 인스턴스에 대 한 세부 정보를 반환 하도록 지정 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
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

### -RoleName
가져올 역할의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceName
Azure 서비스의 이름을 지정 합니다.

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
Azure 배포 환경을 지정 합니다.
이 매개 변수에 허용 되는 값은 프로덕션 또는 스테이징입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
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


