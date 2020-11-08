---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045549"
---
# Get-AzureStorageAccount

## SYNOPSIS
현재 Azure 구독에 대 한 저장소 계정을 가져옵니다.

## 구문과

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**Get-AzureStorageAccount** cmdlet은 현재 구독의 저장소 계정에 대 한 정보를 포함 하는 개체를 반환 합니다.
*Storageaccountname* 매개 변수를 지정 하면 지정 된 저장소 계정에 대 한 정보만 반환 됩니다.

## 예제의

### 예제 1: 모든 저장소 계정 반환
```
PS C:\> Get-AzureStorageAccount
```

이 명령은 현재 구독과 연결 된 모든 저장소 계정이 포함 된 개체를 반환 합니다.

### 예제 2: 지정 된 계정에 대 한 계정 정보 반환
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

이 명령은 ContosoStore01 계정 정보만 포함 하는 개체를 반환 합니다.

### 예제 3: 저장소 계정 테이블 표시
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

이 명령은 현재 구독과 연결 된 모든 저장소 계정이 포함 된 개체를 반환 하 고, 계정 이름, 계정 레이블, 저장소 위치를 나타내는 테이블로 출력 합니다.

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

### -StorageAccountName
저장소 계정의 이름을 지정 합니다.
지정 된 경우이 cmdlet은 지정 된 저장소 계정 개체만 반환 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
* `help node-dev`Node.js 개발 관련 cmdlet에 대 한 도움말을 보려면 입력 합니다. `help php-dev`PHP 개발 관련 cmdlet에 대 한 도움말을 보려면 입력 하세요.

## 관련 링크

[새-AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


