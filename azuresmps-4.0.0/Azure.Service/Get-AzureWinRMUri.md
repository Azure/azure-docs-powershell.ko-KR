---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 5F827BFB-492E-48A2-9610-0CB5FBDD1F9E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0c66043fa36620c2879e88b7dbf82ba251aa4fbc
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046505"
---
# Get-AzureWinRMUri

## SYNOPSIS
가상 컴퓨터 또는 호스팅된 서비스의 가상 컴퓨터 목록에 대 한 WinRM https 수신기의 URI를 가져옵니다.

## 구문과

```
Get-AzureWinRMUri [-ServiceName] <String> [[-Name] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureWinRMUri** cmdlet은 가상 컴퓨터 또는 호스팅된 서비스의 가상 컴퓨터 목록에 대 한 WinRM (Windows Remote Management) https 수신기의 URI를 가져옵니다.

## 예제의

### 예제 1: 가상 컴퓨터에 대 한 WinRM https 수신기의 URI 가져오기
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService -Name MyVM
```

이 명령은 가상 컴퓨터에 대 한 WinRM https 수신기의 UIR을 가져옵니다.

### 예제 2: WinRM https 수신기의 URI를 특정 서비스의 가상 컴퓨터로 가져오기
```
PS C:\> Get-AzureWinRMUri -ServiceName MyService
```

이 명령은 가상 컴퓨터에 대 한 WinRM https 수신기의 UIR을 가져옵니다.

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

### -이름
WinRM URI가 생성 되는 가상 컴퓨터의 이름을 지정 합니다.

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
가상 컴퓨터를 호스트 하는 Microsoft Azure 서비스의 이름을 지정 합니다.

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

## 상속자

## 관련 링크

[뉴욕](./New-AzureVM.md)

[새로운 AzureQuickVM](./New-AzureQuickVM.md)


