---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 32BC6CE6-60EF-4A46-912B-8FE4FCCDF7CC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b91906a25d2f2d7c40f96ed07a4fd7463722023
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045537"
---
# Get-AzureSubscription

## SYNOPSIS
Azure 계정에서 Azure 구독을 가져옵니다.

## 구문과

### ByName (기본값)
```
Get-AzureSubscription [-SubscriptionName <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ById
```
Get-AzureSubscription [-SubscriptionId <String>] [-ExtendedDetails] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### 기본값
```
Get-AzureSubscription [-Default] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### 전류
```
Get-AzureSubscription [-Current] [-ExtendedDetails] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSubscription** Cmdlet은 Azure 계정에서 구독을 가져옵니다.
이 cmdlet을 사용 하 여 구독에 대 한 정보를 가져오고 구독을 다른 cmdlet에 파이프 할 수 있습니다.

**Get-AzureSubscription** 에는 Azure 계정에 대 한 액세스가 필요 합니다.
**AzureSubscription** 를 실행 하기 전에 게시 설정 파일을 다운로드 하 고 설치 하는 Cmdlet 또는 **추가-azureaccount** **cmdlet을 실행 해야 합니다 (가져오기** - **azureaccount settingsfile** ).

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 모든 구독 가져오기
```
C:\PS>Get-AzureSubscription
```

이 명령은 계정에 있는 모든 구독을 가져옵니다.

### 예제 2: 이름으로 구독 가져오기
```
C:\PS>Get-AzureSubscription -SubscriptionName "MyProdSubscription"
```

이 명령은 "MyProdSubsciption" 구독만 가져옵니다.

### 예제 3: 기본 구독 가져오기
```
C:\PS>(Get-AzureSubscription -Default).SubscriptionName
```

이 명령은 기본 구독의 이름만 가져옵니다.
이 명령은 먼저 구독을 가져온 다음 도트 메서드를 사용 하 여 구독의 **SubscriptionName** 속성을 가져옵니다.

### 예제 4: 선택한 구독 속성 가져오기
```
C:\PS>Get-AzureSubscription -Current | Format-List -Property SubscriptionName, Certificate
```

이 명령은 현재 구독의 이름 및 인증서를 포함 하는 목록을 반환 합니다.
**Get-AzureSubscription** 명령을 사용 하 여 현재 구독을 가져옵니다.
그런 다음 구독을 목록에서 선택 된 속성을 표시 하는 **형식 목록** 명령으로 파이프 합니다.

### 예제 5: 대체 구독 데이터 파일 사용
```
C:\PS>Get-AzureSubscription -SubscriptionDataFile "C:\Temp\MySubscriptions.xml"
```

이 명령은 C:\Temp\MySubscriptions.xml 구독 데이터 파일에서 구독을 가져옵니다.
**추가-AzureAccount** 또는 **가져오기-게시 파일** cmdlet을 실행할 때 대체 구독 데이터 파일을 지정한 경우에는 **subscriptiondatafile** 정보 매개 변수를 사용 합니다.

## 변수

### -현재
현재 구독, 즉 "current"로 지정 된 구독만 가져옵니다. 기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.
구독을 "current"로 지정 하려면 **AzureSubscription** Cmdlet의 **현재** 매개 변수를 사용 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Current
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -기본
기본 구독, 즉 "default"로 지정 된 구독만 가져옵니다. 기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.
구독을 "default"로 지정 하려면 **AzureSubscription** Cmdlet의 **기본** 매개 변수를 사용 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: Default
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtendedDetails
표준 설정 외에도 구독에 대 한 할당량 정보를 반환 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: ById
Aliases: Id

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
지정 된 구독만 가져옵니다.
구독 이름을 입력 합니다.
값은 대/소문자를 구분 합니다.
와일드 카드 문자는 지원 되지 않습니다.
기본적으로 **Get-AzureSubscription** 는 Azure 계정의 모든 구독을 가져옵니다.

```yaml
Type: String
Parameter Sets: ByName
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
**SubscriptionName** 속성에는 이름을 기준으로 입력할 수 있지만 값으로는 파이프 하 여 입력 하지 않아도 됩니다.

## 출력

### WindowsAzure. 유틸리티. WindowsAzureSubscription

## 상속자
* Get-AzureSubscription 구독 데이터 파일에서 **-AzureAccount** 및 **가져오기-** 추가 작업 파일 cmdlet이 생성 하는 데이터를 가져옵니다.

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[Get-Azure도움말 파일](./Get-AzurePublishSettingsFile.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)

[제거-AzureSubscription](./Remove-AzureSubscription.md)

[Set-AzureSubscription](./Set-AzureSubscription.md)


