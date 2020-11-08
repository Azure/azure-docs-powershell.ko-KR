---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 931BC75D-B8EF-463D-8FCE-A822093CB05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: bbc1963dbf56d0ef7f31d2174ab352dcc36af619
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046204"
---
# New-AzureStorageAccount

## SYNOPSIS
Azure 구독에서 새 저장소 계정을 만듭니다.

## 구문과

### ParameterSetAffinityGroup (기본값)
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -AffinityGroup <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### ParameterSetLocation
```
New-AzureStorageAccount [-StorageAccountName] <String> [-Label <String>] [-Description <String>]
 -Location <String> [-Type <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**새-AzureStorageAccount** Cmdlet은 Azure 저장소 서비스에 대 한 액세스를 제공 하는 계정을 만듭니다.
저장소 계정은 저장소 시스템 내의 전역적으로 고유한 리소스입니다.
계정은 Blob, 큐 및 테이블 서비스의 상위 네임 스페이스입니다.

## 예제의

### 예제 1: 지정 된 선호도 그룹에 대 한 저장소 계정 만들기
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure01" -Label "AzureOne" -AffinityGroup "prodapps"
```

이 명령은 지정 된 선호도 그룹에 대 한 저장소 계정을 만듭니다.

### 예제 2: 지정 된 위치에 저장소 계정 만들기
```
PS C:\> New-AzureStorageAccount -StorageAccountName "azure02" -Label "AzureTwo" -Location "North Central US"
```

이 명령은 지정 된 위치에 저장소 계정을 만듭니다.

## 변수

### -AffinityGroup
현재 구독에 있는 기존 선호도 그룹의 이름을 지정 합니다.
*Location* 또는 *AffinityGroup* 매개 변수 중 하나만 지정할 수 있습니다.

```yaml
Type: String
Parameter Sets: ParameterSetAffinityGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -설명
저장소 계정에 대 한 설명을 지정 합니다.
설명은 최대 1024 자를 초과할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -레이블
저장소 계정에 대 한 레이블을 지정 합니다.
레이블은 최대 100 자를 초과할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
저장소 계정이 만들어지는 Azure 데이터 센터 위치를 지정 합니다.
*Location* 또는 *AffinityGroup* 매개 변수 중 하나만 포함할 수 있습니다.

```yaml
Type: String
Parameter Sets: ParameterSetLocation
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

### -StorageAccountName
저장소 계정의 이름을 지정 합니다.
저장소 계정 이름은 Azure에서 고유 해야 하며 3 ~ 24 자 사이 여야 하 고 소문자와 숫자만 사용 해야 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Type
저장소 계정의 유형을 지정 합니다.
유효한 값은 다음과 같습니다.

- Standard_LRS
- Standard_ZRS
- Standard_GRS
- Standard_RAGRS
- Premium_LRS

이 매개 변수를 지정 하지 않을 경우 기본값은 Standard_GRS입니다.

Standard_ZRS 또는 Premium_LRS 계정은 다른 계정 유형으로 변경 하거나 그 반대의 경우도 마찬가지입니다.

```yaml
Type: String
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

[Get-AzureStorageAccount](./Get-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


