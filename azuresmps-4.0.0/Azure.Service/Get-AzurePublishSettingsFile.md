---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045633"
---
# Get-AzurePublishSettingsFile

## SYNOPSIS
Azure 구독에 대 한 게시 설정 파일을 다운로드 합니다.

## 구문과

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**Get-azure게시 설정 파일** cmdlet은 사용자의 계정에 대 한 구독에 대 한 제작 설정 파일을 다운로드 합니다.
명령이 완료 되 면 **Import-module settingsfile** cmdlet을 사용 하 여 Windows PowerShell에서 파일의 설정을 사용할 수 있습니다.

Windows PowerShell에서 Azure 계정을 사용할 수 있도록 하려면 게시 설정 파일 또는 **추가-AzureAccount** cmdlet을 사용 하면 됩니다.
게시 설정 파일을 사용 하면 세션을 미리 준비 하 여 스크립트와 백그라운드 작업을 무인 모드로 실행할 수 있습니다.
그러나 모든 서비스에서 설정 파일 게시를 지원 하지는 않습니다.
예를 들어 **AzureResourceManager** 모듈은 게시 설정 파일을 지원 하지 않습니다.

**Get-Azure# settingsfile** 을 실행할 때 기본 브라우저가 열리고 Azure 계정에 로그인 하 라는 메시지가 표시 되 면 구독을 선택 하 고 게시 설정 파일에 대 한 파일 시스템 위치를 선택 합니다.
그런 다음 구독에 대 한 게시 설정 파일을 선택한 파일에 다운로드 합니다.

"게시 설정 파일"은 확장명이 publishsettings 인 XML 파일입니다.
파일에는 Azure 구독에 대 한 관리 자격 증명을 제공 하는 인코딩된 인증서가 포함 되어 있습니다.

**보안 참고 사항:** 게시 설정 파일에는 Azure 구독 및 서비스를 관리 하는 데 사용 되는 자격 증명이 포함 되어 있습니다.
악의적인 사용자가 게시 설정 파일에 액세스 하는 경우 Azure 서비스를 편집, 만들기, 삭제할 수 있습니다.
최상의 보안을 위해 파일을 다운로드 또는 문서 폴더의 위치에 저장 한 다음 **가져오기-Azure# settingsfile** cmdlet을 사용 하 여 설정을 가져와 삭제 합니다.

이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.
사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.

## 예제의

### 예제 1: 게시 설정 파일 다운로드
```
PS C:\> Get-AzurePublishSettingsFile
```

이 명령은 기본 브라우저를 열고 Windows Azure 계정에 연결한 다음 계정에 대 한 publishsettings 파일을 다운로드 합니다.

### 예제 2: 영역 지정
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

이 명령은 contoso.com 도메인의 계정에 대 한 게시 설정 파일을 다운로드 합니다.
Microsoft 계정 대신 조직 계정으로 Azure에 로그인 하는 경우에는 **Realm** 매개 변수와 함께 명령을 사용 합니다.

## 변수

### -환경
Azure 환경을 지정 합니다.

Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.
Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.
자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

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

### -PassThru
명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.
기본적으로이 cmdlet은 출력을 반환 하지 않습니다.

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

### -영역
조직을 조직 ID로 지정 합니다.
예를 들어 Azure에 로그인 하는 경우 admin@contoso.com **Realm** 매개 변수 값은 contoso.com입니다.
조직 ID를 사용 하 여 Azure 포털에 로그인 하는 경우이 매개 변수를 사용 합니다.
Outlook.com 또는 live.com 계정 등의 Microsoft 계정을 사용 하는 경우이 매개 변수는 필요 하지 않습니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야
속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.

## 출력

### 없음 또는 시스템 부울
*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.
그렇지 않으면이 cmdlet은 출력을 반환 하지 않습니다.

## 상속자

## 관련 링크

[추가-AzureAccount](./Add-AzureAccount.md)

[가져오기-Azure# settingsfile](./Import-AzurePublishSettingsFile.md)


